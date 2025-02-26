# Vagrantfile pour la création d'une VM avec les outils CI/CD nécessaires
Vagrant.configure("2") do |config|
  
  # Définition de la VM avec le nom "serveur-cicd"
  config.vm.define "serveur-cicd" do |vm|
    # Utilisation de l'image bento/ubuntu-22.04
    vm.vm.box = "bento/ubuntu-22.04"
    vm.vm.box_check_update = false

    # Redirection du port 8080 de la VM vers le port 8082 de l'hôte
    vm.vm.network "forwarded_port", guest: 8080, host: 8082

    # Configuration du réseau privé avec une nouvelle IP statique
    vm.vm.network "private_network", type: "static", ip: "192.168.56.10"

    # Dossier synchronisé entre l'hôte et la VM (modifiez le chemin si nécessaire)
    vm.vm.synced_folder "./data", "/home/vagrant/data"

    # Configuration des ressources de la VM
    vm.vm.provider "virtualbox" do |vb|
      vb.gui = false
      vb.name = "serveur-cicd"
      vb.memory = "4096" # 4 Go de RAM
      vb.cpus = 2       # 2 CPUs
    end

    # Provisionnement de la VM avec les installations nécessaires
    vm.vm.provision "shell", inline: <<-SHELL
      # Mise à jour des paquets
      sudo apt update && sudo apt upgrade -y

      # Installation des utilitaires nécessaires
      sudo apt install -y apt-transport-https ca-certificates curl software-properties-common

      # Installation de Docker
      sudo apt install -y docker.io
      sudo systemctl enable docker
      sudo systemctl start docker
      sudo usermod -aG docker vagrant

      # Installation de kubectl
      curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
      sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

      # Installation de Helm
      curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash

      # Installation de Git
      sudo apt install -y git

      # Installation de Minikube
      curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
      sudo install minikube-linux-amd64 /usr/local/bin/minikube
    SHELL
  end
end
