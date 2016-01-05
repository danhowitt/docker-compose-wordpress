docker-compose-wordpress
========================

Quick script to get wordpress installed locally with out much faff. 

## Install docker-machine:

```bash
brew cask install virtualbox
brew install docker-machine
```

Create a docker machine:

```bash
docker-machine create default --driver virtualbox
```

Get the IP of the docker machine:

```bash
docker-machine ls

NAME      ACTIVE   DRIVER       STATE     URL                         SWARM   DOCKER   ERRORS
default   *        virtualbox   Running   tcp://192.168.99.100:2376           v1.9.1
```

Here the machine is 192.168.99.100.

## Run wordpress

Run docker-compose:

```bash
cd ~/dev
git clone https://github.com/danhowitt/docker-compose-wordpress.git
cd docker-compose-wordpress
cd ./docker-compose-wordpress
docker compose up
```

Head over to https://{your-docker-machine-ip}/ to start wordpress. 
Example: http://192.168.99.100/