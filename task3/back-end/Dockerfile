FROM ubuntu:latest

RUN apt-get update && apt-get upgrade -y

# Installer Python3, pip3 et Flask
RUN apt-get install -y python3 python3-pip

# Résoudre le problème de gestion d'environnement externe si nécessaire
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Installer Flask avec pip3
RUN pip3 install flask

# Définir le répertoire de travail
WORKDIR /app

# Copier le fichier api.py dans le conteneur
COPY ./api.py /app/api.py

# Exposer le port 5252
EXPOSE 5252

# Commande à exécuter lorsque le conteneur est lancé
CMD ["python3", "api.py"]
