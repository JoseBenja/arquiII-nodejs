
FROM node:20-alpine3.17

# Instalar un servidor Http
RUN npm install -h http-server

# Abri la carpeta "app"
WORKDIR /app

# Copia del "package.json" a la ruta principal del proyecto
COPY package*.json ./app

# Instalar las dependencias
RUN npm install

# Copiar los archivos
COPY . ./app 