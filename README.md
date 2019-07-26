<p align="center">
  <img src="https://user-images.githubusercontent.com/28015011/59379922-95bbcb00-8d60-11e9-85c9-ebbae607a599.png" alt="Bookswap Auth"/>
</p>

# Backend Configuration
This repo contains the Docker and nginx configuration files for deploying to production and for building the backend for local development. 

## How it works:
Docker will create containers for the necessary services for the backend alongside a mongodb container and a nginx one. The `nginx.conf` file will be applied to nginx, thus making it act as a reverse proxy for our backend services. The backend services are never open to the internet, they are only exposed to the local Docker network where they communicate to eachother. Only nginx is exposed to the internet.

## Current backend services:
* [auth](https://github.com/book-swap/auth) - Authorization service
* [user](https://github.com/book-swap/user) - User CRUD service
