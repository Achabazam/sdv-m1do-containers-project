# Sup de Vinci - Containers module project

*Tested with `rust v1.82.0` et `node 23.0.0`.*

### Prerequisite

Install docker and docker: https://docs.docker.com/engine/install/

## Development

### API

#### Basics

Use `cargo run` to start the dev environment.

You can also install [cargo-watch](https://crates.io/crates/cargo-watch) to watche over your project's source for changes, and runs Cargo commands when they occur : `cargo-watch -x run`.

#### Using Docker

Connect to the api pod with docker exec -it <contener-name> /bin/bash

After making some dev stuff on the api, you can build a new dev image with this commande from the root directory with this command:

docker build -t <image_name> -f sdv-api/Dockerfile .

to destroy previous conteners run docker compose up

edit docker-compose_dev.yml and change the image_name of the api_dev service

run docker compose -f docker-compose_dev.yml up to see the change

### Web

#### Basics

Use `npm install` to install all dependancies, and `npm run dev` to start the dev environment.

#### Using Docker

Connect to the web pod with docker exec -it <contener-name> /bin/bash

After making some dev stuff on the web application, you can build a new dev image with this commande from the root directory with this command:

docker build -t <image_name> -f sdv-web/Dockerfile .

to destroy previous conteners run docker compose up

edit docker-compose_dev.yml and change the image_name of the web_dev service

run docker compose -f docker-compose_dev.yml up to see the change

## Production

### Production usage

Push the change before lauching the docker compose up

### API

#### Basics

Run `cargo build --release` to build and compile the app. This will create an executable in `/target/release/sdv-api`.

#### Using Docker

run docker compose up

### Web

#### Basics

Run `npm run build` to build the application, and run `npm run start` to start the Node.js server. 

#### Using Docker

run docker compose up

#### Access application

http://localhost:3333

#### Image link Database 

https://hub.docker.com/repositories/achabazam
