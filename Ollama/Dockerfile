# Utiliser une image de base Debian ou Ubuntu, car les commandes sont basées sur apt
FROM debian:bullseye

# Installer curl
RUN apt-get update && apt-get install -y curl

# Télécharger le binaire Ollama et le rendre exécutable
RUN curl -L https://ollama.com/download/ollama-linux-amd64 -o /usr/bin/ollama \
    && chmod +x /usr/bin/ollama

# Ajouter l'utilisateur et le groupe ollama
RUN useradd -r -s /bin/false -m -d /usr/share/ollama ollama

# Passer à l'utilisateur ollama
USER ollama

# Définir le répertoire de travail
WORKDIR /usr/share/ollama

# Exposer le port 11434
EXPOSE 11434

# Commande pour exécuter Ollama (on utilise CMD ici car cela permet une certaine flexibilité)
CMD ["/usr/bin/ollama", "serve"]
