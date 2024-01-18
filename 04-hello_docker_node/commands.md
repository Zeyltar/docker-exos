On build avec le tag "v1".
Puis on run l'image avec le nom "neo" (t'as la réf?) en mappant le port 3000 sur le conteneur et la machine
```bash
docker build -t 04-hello_docker_node:v1 .
docker run --name neo -p 3000:3000 04-hello_docker_node:v1
```