Docker-Compose Configuration for invoice ninja (https://www.invoiceninja.com/)

This image is based on `php:7.0-fpm` official version.

Your data is persistently stored in `./data/invoiceninja-storage` and `./data/invoiceninja-logo`.


### Usage

To run it:

```Bash
cp ./.env.example ./.env
nano ./.env
# Edit variables to match your environment
docker-compose up -d
# Wait >30 seconds while the database initializes and the cron scheduler starts, then open https://localhost:8000 in a browser
```

A list of environment variables can be found [here](https://github.com/invoiceninja/invoiceninja/blob/master/.env.example)

### Know issue

Phantomjs doesn't work on linux alpine https://github.com/ariya/phantomjs/issues/14186
