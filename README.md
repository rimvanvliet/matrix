# Locale matrix server

## Opzetten server
start voor het `docker compose up -d`
```
docker run -it --rm \
    -v /path/to/synapse/config:/data \
    -e SYNAPSE_SERVER_NAME=chat.vliet.io \
    -e SYNAPSE_REPORT_STATS=yes \
    matrixdotorg/synapse:latest generate
```

start nu met `docker compose up -d` de stack

## setup gebruikers
start een shell in de synapse container
```docker exec -it synapse /bin/bash```


in de container
```register_new_matrix_user -c /data/homeserver.yaml http://localhost:8008```