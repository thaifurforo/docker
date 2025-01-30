# Imagem do node
FROM node:16

# cd para a pasta
WORKDIR /usr/src/app

RUN apt-get update && apt-get install -y wget

# copiar tudo da pasta local onde está o Dockerfile para a pasta acessada no workdir
COPY . .

# informacional que a porta 3000 deve ser exposta para acessar o container
EXPOSE 3000

# comando (pode ser alterado na execução do container) para rodar o arquivo index.js com o node
# CMD ["node", "index.js"]