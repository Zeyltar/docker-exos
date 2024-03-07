On créee le réseau "appnetwork" et on l'assigne au conteneur de la db au lancement.
```bash
docker network create appnetwork
docker run -d --name postgredb --network appnetwork -p 5432:5432 05-hello_exec:v1
```

Puis on modifie l'hôte dans le script du server, ici étant "postgredb"
```js
const pool = new Pool({
  user: 'db',
  host: 'postgredb',
  database: 'db',
  password: 'db',
  port: 5432,
});
```
On build l'image et on lance le conteneur sur le bon réseau
```bash
cd ../05-hello_exec
docker build -t 05-hello_exec:v1 .
docker run -d --name postgredb --network appnetwork -p 5432:5432 05-hello_exec:v1
cd ../06-hello_multiples
docker build -t 06-hello_multiples:v1 .
docker run -d --name nodeapp --network appnetwork -p 3000:3000 06-hello_multiples:v1
```