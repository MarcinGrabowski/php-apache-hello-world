# php-apache-hello-world
Starts Apache which supports a simple "hello world" page in PHP 8.1 

1. Create docker-compose.yml with

version: '3'
services:
    www:
        image: modostudio/php-apache-hello-world:latest
        ports: 
            - 8080:80
        volumes:
            - .:/var/www
            - ./public:/var/www/public
            - ./logs:/var/www/logs
        networks:
            - default
        restart: always

2. docker-compose up -d
3. In the browser: http://localhost:8080
4. Good luck ;)
