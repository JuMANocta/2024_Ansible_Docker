# Étape 1: Construction du Frontend
FROM node:alpine as frontend-builder

# Cloner le dépôt
RUN git clone https://github.com/open-webui/open-webui.git /open-webui
WORKDIR /open-webui

# Copier le fichier .env et installer les dépendances
RUN cp .env.example .env \
    && npm install \
    && npm run build

# Étape 2: Préparation du Backend
FROM python:3.11-slim-bookworm as backend-builder

# Copier les fichiers construits du frontend
COPY --from=frontend-builder /open-webui /open-webui
WORKDIR /open-webui/backend

# Installer les dépendances Python
RUN pip install -r requirements.txt --break-system-packages

# Exposer le port utilisé par le backend (ajuster selon le port réel utilisé)
EXPOSE 8080

# Démarrer le backend et servir le frontend
CMD ["bash", "start.sh"]
