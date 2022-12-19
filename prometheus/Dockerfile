FROM registry.altlinux.org/alt/alt
RUN apt-get update && apt-get install -y prometheus && rm -f /var/cache/apt/archives/*.rpm \
          /var/cache/apt/*.bin \
          /var/lib/apt/lists/*.*
          
WORKDIR /var/lib/prometheus       
USER prometheus
EXPOSE     9090
VOLUME     [ "/var/lib/prometheus" ]
ENTRYPOINT [ "/usr/bin/prometheus" ]
CMD        [ "--config.file=/etc/prometheus/prometheus.yml", \
             "--storage.tsdb.path=/var/lib/prometheus", \
             "--web.console.libraries=/usr/share/prometheus/console_libraries", \
             "--web.console.templates=/usr/share/prometheus/consoles" ]


