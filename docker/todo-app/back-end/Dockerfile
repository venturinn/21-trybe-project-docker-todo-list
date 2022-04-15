# O Dockerfile deve rodar uma imagem node utilizando a versão 14
FROM node:14-alpine AS build

# Definindo um diretório de trabalho
WORKDIR /app

# Copiar todos os arquivos da pasta back-end para a imagem ("COPY source dest")
COPY . ./

# Deve adicionar o arquivo node_modules.tar.gz a imagem
ADD ./node_modules.tar.gz ./

# Instalar a aplicação utilizando o comando `npm install`
RUN npm install

# Deve estar com a porta 3001 exposta
EXPOSE 3001

#Ao iniciar a imagem deve rodar o comando npm start
CMD npm start
