FROM node:13-alpine

ENV ME_CONFIG_MONGODB_ADMINUSERNAME=admin \
    ME_CONFIG_MONGODB_ADMINPASSWORD=password

RUN mkdir -p /home/app

#copiando todos os arquivos da pasta /app para home/app (o dot se refere a todos os arquivos dentro da pasta)
COPY ./app /home/app

# define o diretório padrão em que irão ocorrer os próximos comandos (nesse caso pro /home/app)
WORKDIR /home/app

RUN npm install

CMD ["node", "/home/app/server.js"]