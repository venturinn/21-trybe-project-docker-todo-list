# O Dockerfile deve rodar uma imagem node utilizando a versão 14
FROM node:14-alpine AS build

# Definindo um diretório de trabalho
WORKDIR /app

# Copiar todos os arquivos da pasta front-end para a imagem ("COPY source dest")
COPY . ./

# Deve adicionar o arquivo node_modules.tar.gz a imagem, de maneira que ele seja extraído dentro do container
ADD ./node_modules.tar.gz ./

# Instalar a aplicação utilizando o comando `npm install`
RUN npm install

# `REACT_APP_API_HOST`: padrão `localhost`
# *(Docker)* Aqui você deve indicar o nome do container do `back-end`
ENV REACT_APP_API_HOST todobackend

# `REACT_APP_API_PORT`: padrão `3001`
# *(Docker)* Aqui você deve indicar a porta que você definiu internamente no container do `back-end`
ENV REACT_APP_API_PORT 3001

# Deve estar com a porta 3000 exposta
EXPOSE 3000

#Ao iniciar a imagem deve rodar o comando npm start
CMD npm start
