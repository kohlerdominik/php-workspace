# php-workspace
My personal php workspace. Feel free to use or fork

### PHP 7.4
```sh
docker build -t php-workspace:7 74
docker run -it -v ${PWD}:/app php-workspace:7
```

### PHP 8.0
```sh
docker build -t php-workspace:8 80
docker run -it -v ${PWD}:/app php-workspace:8
```