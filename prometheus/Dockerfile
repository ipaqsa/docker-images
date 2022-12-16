FROM registry.altlinux.org/alt/alt
RUN apt-get update && apt-get install -y prometheus && rm -f /var/cache/apt/archives/*.rpm \
          /var/cache/apt/*.bin \
          /var/lib/apt/lists/*.*
EXPOSE     9090
WORKDIR /promdata
VOLUME ["/promdata", "/etc/prometheus"]
CMD ["prometheus", "--config.file=/etc/prometheus/prometheus.yml"]
