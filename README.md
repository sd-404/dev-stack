# Dev Stack

Dev stack is a PHP dev environment based on Docker.

## Requirements

* [Docker](https://docs.docker.com/engine/install/)
* [Docker Compose](https://docs.docker.com/compose/install/)

## Structure

```
project
│
└───app
│   │   file
│   │   ...
│   └───subfolder1
│       │   file
│       │   file
│       │   ...
│   
└───utils
    │
    └───docker
        └───nginx
        │   │   file
        │   │   ...
        └───php
        │   │   file
        │   │   ...
        │   docker-compose.yml
        │   Makefile
         

```
In the app directory lives our application source code.

The utils directory contains all devop tools, such Docker, Ansible, Shell's scripts ...

## Docker Services

* Nginx
* MySQL 8.0
* PHP 7.4
* RabbitMQ
* PHPMyAdmin
* MailHog

## Installation

After cloning the repository.

```bash
cd utils/docker
```
Build 
```bash
docker-compose build
```
You can use the Makefile to build :
```bash
make build
```

## Usage

### Start
```bash
docker-compose up -d

# same thing here you can use the Makefile
make up
```

### Stop
```bash
docker-compose down --remove-orphans

# same thing here you can use the Makefile
make down
```

## License
[MIT](https://choosealicense.com/licenses/mit/)
