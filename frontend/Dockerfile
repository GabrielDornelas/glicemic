# Use uma imagem base oficial do Node.js
FROM node:23

# Defina o diretório de trabalho no container
WORKDIR /glicemic/frontend/

# Copie o package.json e o package-lock.json para o diretório de trabalho
COPY package*.json ./

# Instale as dependências do projeto
RUN npm install

# Copie todos os arquivos do projeto para o diretório de trabalho
COPY . .

# Construa o aplicativo para produção
RUN npm run build

# Exponha a porta que o servidor usará
EXPOSE 8080

# Comando para rodar o servidor Vue.js
CMD ["npm", "run", "serve"]
