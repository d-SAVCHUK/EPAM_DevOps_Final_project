# EPAM DevOps Course Final project.

## 1. About me.

My name is Dmitry. I have over 10 years of experience in the financial sector. From February 2022, I entered the EPAM Univercity course for switchers - IT Fundamentals. Upon completion, I chose the DevOps L0 direction, after passing the tests I successfully moved to the L1 level. Articles that we studied:
- DevOps Essentials L1: Linux + Bash, Database Administration, Networks using Linux, Cloud Basic, CI/CD & IaC & Containerisation (Jenkins), Terraform, Docker, Ansible.
- DevOps Essentials L0: Hypervisor Essentials, Networking Essentials, ContOS Linux Essentials, Scripting: Bash Essentials, Vision control with Git, Python Essentials.
- IT Fundamentals: Basics of Computer Science, Programming, Front End, Vision control with Git, Math for IT, Introduction to SQL, Software Development Methodologies, Cloud Overview.

Now I present the final project of the course.

My Git with home tasks: https://github.com/d-SAVCHUK

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

![screen](https://github.com/d-SAVCHUK/EPAM_DevOps_Final_project/blob/main/project%20schema.jpg)

## 4. Project realisation.

4.1. The technologies used in project:
- Azure Cloud
- Azure DevOps (git)
- Ansible (create in configure env in azure cloud) https://dev.azure.com/savchukdmitriy/Final_project/_git/ansible 
- Jenkins (Master: trigger build, Slave: CI/CD - build and deploy app in container) 
- Web App (Docker container) https://dev.azure.com/savchukdmitriy/Final_project/_git/Final_project 

4.2. Step by step realisation:
1. Create free accounts at Azure Cloud and Azure DevOps.
2. Set up Ansible on Azure:
- Set up your Azure account credentials in your local terminal. This can be done by installing the Azure CLI and running "az login".
- Create an Azure resource group to contain your deployment. This can be done with the "az group create" command, specifying the resource group name, location, and any other desired parameters.
- Create an Ansible playbook to define your deployment. This playbook should contain the desired Azure resources you want to create or manage.
- Install Ansible on your local machine or on an Azure virtual machine.
- Use the "ansible-playbook" command to run your Ansible playbook and deploy your Azure resources. You will need to specify the path to your playbook, as well as any required variables or credentials.
```bash
az login
az group create
ansible-playbook
```
3. Create yaml files with instruction fro Ansible:
```bash
ansible-playbook main.yaml
ansible-playbook jenkins.yaml -i hosts
ansible-playbook jenkins-slave.yaml -i host
```
## 5. Proof of work.
...
