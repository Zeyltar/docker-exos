FROM node:20

WORKDIR /app

# ça coule de source
COPY package*.json .
COPY server.js .

# installation des dépendances
RUN npm install

EXPOSE 3000

#On lance le script start dans package.json pour lancer le server node
CMD [ "npm", "start" ]