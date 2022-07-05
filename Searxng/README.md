## VOLUMES
Um Dateien zu persistieren folgende Verzeichnisse anlegen:  
```
mkdir -p $HOME/searxng/caddy/data
mkdir -p $HOME/searxng/caddy/config
mkdir -p $HOME/searxng/srv
```

### Config File
Caddy-File downloaden: https://github.com/searxng/searxng-docker/blob/master/Caddyfile  
Caddy-File kopieren nach: $HOME/searxng/caddy
Caddy-File bei Bedarf editieren, genügt für FirstRun  

### Docker-Compose
Docker-Compose - File kopieren nach: $HOME/searxng  
Dann Compose-File bearbeiten:  
Line 14: IP-Adresse von Docker-Host  
Line 15: Deine Geschäftsadresse (EMail), oder vom WIndoof typen  
Line 47: IP-Adresse von Docker-Host (siehe Wert für Line 14)  

### Docker Network
Parameter checken: https://docs.docker.com/engine/reference/commandline/network_create/  
Folgender Parameter *sollte* funktionieren:
```
docker network create searxng
```
