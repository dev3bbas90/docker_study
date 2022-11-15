# select OS >>  alpine lunix use it as abase image for its small size
from alpine


WORKDIR /source


CMD [ "echo" ,"MY First Custom Docker Image !" ]

# Packages or dependancies
RUN apk add --update redis

CMD [ "redis-server"]


from bitnami/laravel
from composer
from php:7.4.33-fpm

COPY *.env.example .env

RUN composer update
RUN Artisan key:generate


#  Copy & publish distenation file
COPY . .
RUN Artisan serv --port=2030