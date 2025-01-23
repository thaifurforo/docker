# Imagem do node
FROM node:16

# cd para a pasta
WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y wget

# instala o dockerize para poder verificar se o container do mysql está pronto antes de subir o container do node
ENV DOCKERIZE_VERSION v0.6.1
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz

# copiar tudo da pasta local onde está o Dockerfile para a pasta acessada no workdir
COPY . .

# informacional que a porta 3000 deve ser exposta para acessar o container
EXPOSE 3000

# comando (pode ser alterado na execução do container) para rodar o arquivo index.js com o node
# CMD ["node", "index.js"]