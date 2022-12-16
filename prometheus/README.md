# Prometheus image

Before starting container, create two dirs for data and config, they will be mounted.
```
mkdir promconf
mkdir promdata
```

Then create config file in promconf, for example, you can use example file from:
```
https://github.com/prometheus/prometheus/blob/main/documentation/examples/prometheus.yml
```
Command for run:
```
docker run -v promdata:/promdata -v promconf:/etc/prometheus IMAGENAME
```
*If you want to be able to view services on localhost then specify flag:
```
--network="host"
```

