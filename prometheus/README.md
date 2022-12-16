# Prometheus image

Before starting the container, 
create two directories for data and configuration, they will be mounted.
```
mkdir promconf
mkdir promdata
```

Then create a configuration file in promconf, for example, you can use an example file from:
```
https://github.com/prometheus/prometheus/blob/main/documentation/examples/prometheus.yml
```
Command for run:
```
docker run --network="host" -v promdata:/promdata -v promconf:/etc/prometheus IMAGENAME
```

