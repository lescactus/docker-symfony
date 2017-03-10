# docker-symfony
Set up a Symfony instance with Nginx, PHP-FPM 7 and MariaDB using docker-compose 


----------


About
-------------

Put your Symfony app in code/ 


```
# Build and pull images 
docker-compose build
docker-compose pull
```

``` 
# Run in background
docker-compose up -d
```

``` 
# Check running services
docker-compose ps

         Name                        Command              State               Ports
----------------------------------------------------------------------------------------------
dockersymfony_mariadb_1   docker-entrypoint.sh mysqld     Up       3306/tcp
dockersymfony_nginx_1     nginx -g daemon off;            Up       443/tcp, 0.0.0.0:80->80/tcp
dockersymfony_php-fpm_1   docker-php-entrypoint php-fpm   Up       9000/tcp
dockersymfony_storage_1   /bin/true                       Exit 0
```
