FROM debian:latest
WORKDIR /app
RUN apt update && apt install -y git zip npm 
EXPOSE 3000
COPY ../sdv-web .
RUN npm install
RUN npm run build
CMD [ "npm", "start" ]

