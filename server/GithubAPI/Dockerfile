FROM node:lts-alpine

WORKDIR /app/githubapi

COPY package.json .

RUN npm install

COPY . .

EXPOSE 8081

CMD ["node","index.js"]