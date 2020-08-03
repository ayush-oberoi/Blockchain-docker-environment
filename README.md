# Blockchain-docker-environment

A Docker containerized application which includes all the components for the deployment of smart contracts. 
The docker image includes truffle, go-ethereum, ganache-cli, nodejs, solidity compiler (solc) and all truffle packages.
The services are assigned - ganache and truffle in the docker-compose.yml file.

## Prerequisites

- Make sure you have installed docker CE and docker-compose on your local machine
- Remove any proxy on 8080 port


## How to clone it to your local machine

- clone the repository - `git clone https://github.com/ayush-oberoi/Blockchain-docker-environment`
- Pull the blockchain image - `docker pull docker.pkg.github.com/ayush-oberoi/Blockchain-docker-environment/blockchain:latest`
- Change the tag name for the image to `blockchain` - 
  Run `sudo docker tag docker.pkg.github.com/ayush-oberoi/blockchain-docker-environment/blockchain blockchain
- Run `cd Blockchain-docker-environment`

## Running the environment

- In the repo folder, Run `sudo docker-compose -f docker-compose.yml up -d` . This will run the services (containers) in the background
- it will create two services - truffle and ganache.
- Run - `sudo docker ps` to check the container name.
- Open two terminals use `sudo docker attach <ganache_container_name>` on first terminal and `sudo docker attach <truffle_container_name>` on second terminal.
- We get root shells of containers. 

### In truffle container, I have configured two projects - one with webpack truffle box and second with a simple smart contract deployment.
You can create your own project folders with smart contract - compile, migrate and deploy your own contract.
