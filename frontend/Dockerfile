FROM node:18
WORKDIR /app

COPY package*.json ./

RUN npm ci

COPY . .
RUN npm run build
RUN npm install --global http-server

EXPOSE 8000

CMD ["npx", "http-server", "/app/build", "-p", "8000", "-c-1"]
