## docker-webserver-arm64
this docker config act as web server for local web development on arm64 machine

### origins of the story
I made this because I didn't want any libs like PHP, NPM, etc. installed on the main machine. so I tried to create a web server using docker engine and tried to isolate the necessary libs.

``feel free to modify it``

### History
``2024-03-04 change logs``
* nginx as proxy server
* php-fpm config as backend server (php7.1)
* node container to build react-app
* composer container to build php project

### Makefile [make] commands sample (you can use docker commands instead)
create image
```
make build-image image_name=IMAGE_NAME version=IMAGE_VERSION file=DOCKER_FILE_PATH
```

run docker-compose.yml (default)
```
make up
```

stop docker
```
make stop
```

remove container
```
make down
```

check nginx-config
```
make nginx-check
```

nginx reload
```
make nginx-reload
```