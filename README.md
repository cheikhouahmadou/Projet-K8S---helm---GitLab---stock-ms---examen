"# Projet-K8S---helm---GitLab---stock-ms---examen" 

 Configuration de la VM avec Vagrant, incluant le réseau, les ressources et le dossier synchronisé.

 
![A01](https://github.com/user-attachments/assets/8e1febca-d484-4256-b956-64a7fced2638)

Provisionnement de la VM avec l'installation de Docker, kubectl, Helm, Git et Minikube.

![A02](https://github.com/user-attachments/assets/9dbc2418-d421-4c12-935b-e78338702558)

Vérification des versions de Docker, kubectl, Helm, Minikube et Git installées avec succès.


![A03](https://github.com/user-attachments/assets/ea45f01a-e742-4261-b500-d63e508502e8)


Connexion à la VM avec Vagrant SSH pour vérifier les installations.


![A04](https://github.com/user-attachments/assets/00bffb37-5468-47e7-8556-f41c0bf2d729)

Docker ps -a

![A05](https://github.com/user-attachments/assets/3c246edf-df91-42bf-a0b1-1bde5beb8ae0)

minikube start --driver=docker

![A06](https://github.com/user-attachments/assets/096c51ec-6209-42f3-b573-69bb4f2695fa)

creation fichier config.yaml


![A07](https://github.com/user-attachments/assets/2f05dc27-b8dc-4f59-8a6f-3758d9d618d7)

Connect a kubernetes cluster :L'image montre la création réussie d'une connexion Kubernetes (k8s-connection) 
avec GitLab, accompagnée d'un jeton d'accès pour l'agent. Elle fournit également des instructions pour installer 
et configurer l'agent GitLab sur Kubernetes en utilisant Helm.

![A08](https://github.com/user-attachments/assets/c607d3a3-89e9-4162-8f6f-c45dbcf5bb66)


déploiement réussi de l'agent GitLab (k8s-connection) dans l'espace de
noms gitlab-agent-k8s-connection avec Helm. 


![A09](https://github.com/user-attachments/assets/ba563635-7fb6-4107-a8e6-fa564d7169f2)


L'image montre que l'agent Kubernetes "k8s-connection" est connecté à GitLab avec succès

![A10](https://github.com/user-attachments/assets/d1a30120-5005-4384-a60c-8fef1fb25649)

 pipeline nommée "Add new file" a échoué avec le statut "Failed"
 
![A11](https://github.com/user-attachments/assets/4e6eb4a3-7a15-4e63-97d5-cd199252001b)

![A12](https://github.com/user-attachments/assets/5d64a488-6c13-495a-91b4-2f67ec5a3071)

d'intégration continue/déploiement continu (CI/CD)

![A13](https://github.com/user-attachments/assets/c00c06fd-eafe-45ad-ab0a-f6cda2823ac1)


![A14](https://github.com/user-attachments/assets/61cee78b-324a-435a-83ee-553a16cf697d)

CI/CD sur la branche main.  Le premier pipeline, déclenché par une mise à jour du fichier 
.gitlab-ci.yml, a réussi.


![A15](https://github.com/user-attachments/assets/f50b7d46-5184-4d3c-9a66-8ee80b9fb586)


git clone 

![A16](https://github.com/user-attachments/assets/ccddf4e4-588f-4752-b601-172fb0f9dd5d)


![A17](https://github.com/user-attachments/assets/7ed6ee33-57ff-4c20-997d-661940f5b16c)


![A18](https://github.com/user-attachments/assets/c5baa0d4-24d5-42b0-8fa4-d3d6e7a3d410)


![A19](https://github.com/user-attachments/assets/55040824-c854-4868-a8d1-917faf19612d)


![A20](https://github.com/user-attachments/assets/d4cbc765-dc6f-4a10-928c-93fcc44e229f)

danied : Pour pousser votre image Docker sur GitLab Container Registry

![A0](https://github.com/user-attachments/assets/bf636605-c76c-4f12-8b23-48c798059dfc)

