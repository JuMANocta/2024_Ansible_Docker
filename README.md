# Ansible Docker

## Aperçu
Ce projet démontre le déploiement d'une application web OpenWebUI en utilisant Ansible et Docker, illustrant une architecture moderne basée sur conteneurs. L'application OpenWebUI offre une interface utilisateur ChatGPT like pour interagir avec Ollama, un modèle de langage naturel local (LLM) qui peut être utilisé pour générer du texte en fonction de l'entrée utilisateur.

## Architecture
L'application se compose de deux conteneurs principaux : Ollama, qui agit comme LLM local, et OpenWebUI, qui fournit une interface graphique pour interagir avec Ollama like ChatGPT.

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
- Ollam/Dockerfile
- Open-WebUI/Dockerfile

## Créer le fichier de configuration Ansible
- playbook.yml

## Exécution du Playbook
```bash
ansible-playbook playbook.yml
```