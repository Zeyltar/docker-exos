On tag l'image locale avec notre nom d'utilisateur et le tag de la version.
Puis on la publie sur Docker Hub, 
```bash
docker tag 02-hello_dockerfile:v1 ynovzey/starwars:v1
docker push ynovzey/starwars:v1
```
Elle pourra être téléchargée avec la commande `docker pull ynovzey/starwars:v1`