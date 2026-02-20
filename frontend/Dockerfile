FROM node:18
WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .
RUN npm run build
RUN npm install --global http-server

EXPOSE 8000

CMD ["http-server", "/app/build", "-p", "8000"]
