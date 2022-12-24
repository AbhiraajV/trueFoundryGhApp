FROM node:lts-alpine

WORKDIR /app/emailservice

COPY package.json .

RUN npm install

COPY . .

EXPOSE 8082

CMD ["node","index.js"]