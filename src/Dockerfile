#Especificar a tag na imagem base
FROM node:20.16.0
WORKDIR /app
#Copiar o package.json antes dos outros arquivos, pois qualquer alteração nos outros arquivo vai impossibilitar o Docker de usar o cache,
#ou seja, vai forçar a instalação das dependencias pela npm install novamente.
COPY package*.json .
RUN npm install
COPY . .
EXPOSE 8080
CMD ["node", "server.js"]