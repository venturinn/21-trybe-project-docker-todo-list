# O Dockerfile deve rodar a imagem mjgargani/puppeteer:trybe1.0 para que os testes funcionem
FROM mjgargani/puppeteer:trybe1.0 AS build

# Definindo um diretório de trabalho
WORKDIR /app

# Copiar todos os arquivos da pasta tests para a imagem ("COPY source dest")
COPY . ./

# Deve adicionar o arquivo node_modules.tar.gz a imagem
ADD ./node_modules.tar.gz ./

# `FRONT_HOST`: padrão `localhost`;
# *(Docker)* Aqui você deve indicar o nome do container do `front-end`;
ENV FRONT_HOST todofrontend

# `FRONT_PORT`: padrão `3000`
# *(Docker)* Aqui você deve indicar a porta que você definiu internamente no container do `front-end`;
ENV FRONT_PORT 3000

# Instalar a aplicação utilizando o comando `npm install`
RUN npm install

#Ao iniciar a imagem deve rodar o comando npm test
CMD ["npm test"]
