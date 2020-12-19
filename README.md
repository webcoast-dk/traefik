# Træfik reverse proxy for local development with docker

## Pre-requisites
* Docker 18.09.7+
* docker-compose 1.21.0+

## Installation
1. Clone this repository
   ```bash
   git clone https://github.com/webcoast-dk/traefik.git traefik
   ```
2. Change into directory
   ```bash
   cd traefik
   ```
3. Create traefik network, if it does not exist
   ```bash
   docker network inspect traefik &> /dev/null || docker network create traefik
   ```
   
4. Start reverse proxy
   ```bash
   docker-compose up -d
   ```
   
The container is set to `restart: always`, so it should restart automatically
with your docker daemon.

## Dashbord
You can access the dashboard through http://localhost:8080. Replace `localhost` with the host's ip
address or hostname, if you do not use localhost.
