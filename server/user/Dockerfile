# Base image
FROM node:18

# Create app directory
WORKDIR /app/userapi

# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./

# Install app dependencies
RUN yarn install
RUN npx prisma generate
# Bundle app source
COPY . .

# Creates a "dist" folder with the production build
RUN yarn run build
RUN npx prisma generate

EXPOSE 8080

# Start the server using the production build
CMD [ "node", "dist/main.js" ]
