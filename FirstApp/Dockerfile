
FROM node:22.3.0


WORKDIR /app


COPY package*.json ./


RUN npm install


COPY . .


EXPOSE 3600


CMD ["npm", "start"]