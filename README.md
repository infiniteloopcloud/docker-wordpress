# PHP based docker configuration for WordPress

## docker-compose

```yml
php:
  image: TODO
  volumes:
    - ./:/var/www/html
```

## xdebug

Copy the contents of the `xdebug.ini.example` file in this repo to an `xdebug.ini` file in your project (edit according to your OS), then mount it to the right place in your `docker-compose.yml` file:

```yml
php:
  image: TODO
  environment:
    PHP_IDE_CONFIG: "serverName=PHPSTORM"
  volumes:
    - ./:/var/www/html
    - ./xdebug.ini:/usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
```

For usage with PhpStorm, view the [official documentation](https://www.jetbrains.com/help/phpstorm/debugging-a-php-cli-script.html).
