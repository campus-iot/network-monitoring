# LoRaWAN Network Monitoring Stack

## Web site
* https://lnsmonit.MYDOMAIN.ORG with admin MY_WEAK_SECRET_PASSWORD_TO_CHANGE
* https://lnsmonit-n.MYDOMAIN.ORG with admin MY_WEAK_SECRET_PASSWORD_TO_CHANGE
* http://localhost:3000 with admin MY_WEAK_SECRET_PASSWORD_TO_CHANGE
* http://localhost:1880 with admin MY_WEAK_SECRET_PASSWORD_TO_CHANGE

## Layout
* configuration: contains containers' configurations
* data: contains containers' data (rw)
* backups: contains backups of the databases and messages log
* docker: contains the build of the containers

## Passwords
Change the passwords into the YAML files

```bash
docker-compose exec nodered /data/set_password.sh MY_WEAK_SECRET_PASSWORD_TO_CHANGE MY_WEAK_SECRET_PASSWORD_TO_CHANGE
docker-compose stop nodered
docker-compose start nodered
```

## Dashboards
Dashboard should be imported by hand into Grafana.

The files to load are into configuration/grafana/dashboards

## Ports
* nodered : 1880
* grafana : 3000
* influxdb : 8086

## Database
The name is `lorawan`

## Operations

```
# launch the composition
docker-compose up -d

# list the containers of the composition
docker-compose ps

# follow the logs of the containers
docker-compose logs -f

# stop the composition
docker-compose stop

# start the composition
docker-compose start

# destroy all the containers of the composition
docker-compose down
```

## TODO
