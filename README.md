# Easy to start dev env with odoo and docker

Run the service

``` bash
docker-compose up -d
```

First time starting, need to force rebase database while containers are running

``` bash
docker compose run --rm ${odoo-instance} bash
odoo -i base -d ${db-name} --db_host ${db-instance} -r ${db-user} -w ${db-password}
```

The odoo server is now started at the default `localhost:8069`

Develop custom apps on `custom_addons/` and restart docker-compose to take effect
