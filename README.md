# EPAM DevOps Course Final project.

## 1. About me.

## 2. Project requirements.

- host with git (Linux, MacOS, Windows: [possible on a virtual machine]);
- as a semantic part, you can choose an html page (index.html) with content of your choice.
- a cloud repository (GitHub, GitLab, BitBucket) where you will commit/push;
- CI/CD framework (Jenkins). The main purpose of Jenkis is to download the updated project from github and assemble it (build), and then place it in the artifact repository (delivery) or deploy it on the target server (deploy);
- configuration management tool (Ansible) – can be used to set up machines and initial setup of your project environment;
- it is necessary that the Jenkins Master redirects jobs to its nodes (Slaves). In the case of a web page, this item can be omitted and immediately deployed to the target server.
- Docker and containerization can be used as follows - organize the launch of Jenkins and its nodes in containers and the target server also in the container.

## 3. About project.

Project schema:
![screen]()

## 4. Project realisation.

4.1. The technologies used in project:
- Azure cloud
- Azure devops (git)
- Ansible (create in configure env in azure cloud) https://dev.azure.com/savchukdmitriy/Final_project/_git/ansible 
- Jenkins (Master: trigger build, Slave: CI/CD - build and deploy app in container) 
- Web App (Docker container) https://dev.azure.com/savchukdmitriy/Final_project/_git/Final_project 

4.2. Step by step realisation:

## 5. Proof of work.

