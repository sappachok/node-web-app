Node.js Web Application + Mongo Database Docker compose v1.0
=======================================================

Usage
-----

Simply copy Dockerfile and docker-compose.yml to your project and run docker-compose up.

Volume Configuration
--------------------

```volume config
version: '3'
services:
    app:
        image: sappachok/node-web-app
        container_name: node-web-app
	...
        volumes:
            - /var/hostdir/nodeapp:/nodeapp
            - /var/hostdir/nodeapp/logs:/root/.npm/_logs/

    mongo:
        image: mongo
        container_name: mongo
	...
        volumes:
            - /var/hostdir/mongodb/data:/data/db
            - /var/hostdir/mongodb/config:/data/configdb
```