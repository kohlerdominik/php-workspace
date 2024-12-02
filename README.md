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
