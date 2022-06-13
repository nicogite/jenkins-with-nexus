# Jenkins and sonarqube with a simple docker-compose file

## Etapes à suivre

- Installer le plugin sonarqube scanner (2.14)

- Aller dans "global tool configuration", et ajouter une installation Sonarqube dans l'onglet "Sonarqube Scanner"

- Aller dans "Configure System" et rentrer le "Server URL" : "http://<service-name>:9000"

- Accéder au site Sonarqube via "http://localhost:9000"

- Connectez vous sur le site, login:admin, mot de passe:admin. Choisissez un mot de passe.

- Une fois sur Sonarqube accéder à Administration>Security>users

- Sur la droite de notre User "Administrator", cliquer sur le menu défilant en dessous de "Tokens". Nommer notre token et cliquer sur "Generate"

- Copier ce token.

- Retourner sur Jenkins, dans "Configure System", l'onglet "Sonarqube servers"

- Cliquer sur le bouton "Add" en dessous de "Server Authentication token"

- Dans "Kind" Sélectionner "Secret Text"

- Coller notre token copié depuis sonarqube dans "Secret"


## Nexus

- Pour lancer Nexus, faire au préalable un chmod 777 sur les dossier Nexus