# PHP-based application with docker

This docker composition contains:
- PHP driver for your application, version in use by default is `7.4`
- Apache 2.4 server (optional)
- MySQL server (default to `8.4`)

## How to?
### Run with its actual setup (basic)

This will run all the 3 services and bind `./public` folder as root apache folder

```shell
docker compose up -d
```

### Run with a specific folder
To to so, you need to tweak a bit the `docker-compose.yml` file, in `volume` section to point your public folder to the volume `application-data`.