# Ansible Docker

Ceci est un simple exemple de déploiement d'une application web avec Ansible et Docker.

L'exemple sera basé sur une application WEB OpenWebUI.
Deux containers seront créés:
- Un container pour Ollama
- Un container pour OpenWebUI

## Prérequis
Installation de Ansible
```bash
sudo apt-get install ansible
```
Installation de Docker
```bash
sudo apt-get install docker
```

## Créer les images Dockers pour Ollama et OpenWebUI
cf Ollam/Dockerfile
cf Open-WebUI/Dockerfile

## Créer le fichier de configuration Ansible
cd Playbook