# Observability stack

Repository contains compose file with grafana stack observability services:  

- prometheus
- pushgateway
- alertnamager
- loki
- tempo
- grafana

## Quickstart

```shell
docker compose up -d
```

## Services

### Prometheus 

Address: http://127.0.0.1:9090  
Configuration: `./prometheus/prometheus.yml`  

### Pushgateway

Address: http://127.0.0.1:9091  

### Alertnamager

Address: http://127.0.0.1:9093  
Configuration: `./alertmanager/config.yml` 

**Note**: there is no webhook service to receive alerts. Some example [can be found here](https://github.com/sa06/prometheus-pushgateway/tree/master/webhook).  

### Loki

Address: http://127.0.0.1:3100  
Metrics: http://127.0.0.1:3100/metrics  
Configuration: `./loki/loki-config.yaml`  

### Tempo

Address: http://127.0.0.1:3200  
Metrics: http://127.0.0.1:3200/metrics  
Configuration: `./tempo/tempo.yaml`  

### Grafana 

Address: http://127.0.0.1:3000  
Datasources provisioning configuration: `./grafana/datasources/datasource.yml`  
To automaticaly add dashboards place json-file to `./grafana/dashboards/source/`   
