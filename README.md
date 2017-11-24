<img align="right" width="175px" src="http://i.imgur.com/mdZ8Ktf.png" />

# Dspot Phalcon Docker

## Getting started

Install <b>docker</b> and <b>docker-compose</b>

Put your application into `www` folder

Create a new virtual host configuration to `conf/apache/sites-enabled`.

Add the url to your local hosts file: `127.0.0.1		your.app.url`

Run `docker-compose up -d`

## Useful shortcuts

Remove all docker containers
```docker rm -f $(docker ps -aq)```

Tail logs
```docker logs --follow phalcondocker_app_1```

SSH into container
```winpty docker exec -it phalcondocker_app_1 bash```