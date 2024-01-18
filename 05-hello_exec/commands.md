On build l'image puis on lance un conteneur le nom postgredb et on map le port 5432 sur l'hôte et le conteneur.
```bash
docker build -t 05-hello_exec:v1 .
docker run -d --name postgredb -p 5432:5432 05-hello_exec:v1 # -d pour lancer en tâche de fond
```

On intéragit avec le conteneur pour lancer la commande et se connecter à la db
```bash
docker exec -it postgredb psql -U db -h localhost -p 5432 db
```

Puis on exécute le script suivant
```sql
SELECT id, nom FROM personnes WHERE age > 30;
```
