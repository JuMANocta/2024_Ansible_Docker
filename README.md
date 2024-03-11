# Ansible Docker

Ceci est un simple exemple de déploiement d'une application web avec Ansible et Docker.

L'exemple sera basé sur une application WEB OpenWebUI.
Deux containers seront créés:
- Un container pour Ollama
- Un container pour OpenWebUI

## Prérequis WSL2
### Installation de Ansible
```bash
sudo apt-get install ansible
ansible-galaxy collection install community.docker
```
### Installation de Docker Desktop pour Windows
[Docker Desktop](https://www.docker.com/products/docker-desktop/)

Puis activer WSL2 dans les paramètres de Docker Desktop
et ativer le partage de Docker pour la distro WSL2 souhaitée.

## Créer les images Dockers pour Ollama et OpenWebUI
cf Ollam/Dockerfile

cf Open-WebUI/Dockerfile

## Créer le fichier de configuration Ansible
cf playbook.yml

## Exécution du Playbook
```bash
ansible-playbook playbook.yml
```