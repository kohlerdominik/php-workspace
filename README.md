# php-workspace
My personal php workspace. Feel free to use or fork

### Build

```sh
# Build all
docker compose build

# or one
docker compose build {VERSION}
```

### Use
```sh
# Recommended run
docker run -v ${PWD}:/app:cached --user $(id -u):$(id -g) -it --rm php-workspace:84
```

#### xdebug
```sh
# the xdebug folder has to exist in /app/xdebug with sufficient permission,
# otherwise xdebug will not write a profile file 
mkdir xdebug

# run your script with xdebug
XDEBUG_TRIGGER=1 php your-file.php
```