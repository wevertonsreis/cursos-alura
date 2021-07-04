FROM node:latest
LABEL author="Weverton Santana Reis"
ENV PORT=3000
COPY . /var/www
WORKDIR /var/www
RUN npm install
ENTRYPOINT [ "npm", "start" ]
EXPOSE $PORT