# Install Helm packages

```bash
helm install --values fluentd-values.yml fluentd kiwigrid/fluentd-elasticsearch --namespace logging
```

```bash
helm install --values elasticsearch-values.yml elasticsearch elastic/elasticsearch --namespace logging
```

```bash
helm install kibana elastic/kibana --namespace logging
```

```bash
helm install -n logging metricbeat elastic/metricbeat
```

# Generate manifests

```bash
helm template --values fluentd-values.yml fluentd kiwigrid/fluentd-elasticsearch > k8s/fluentd.yaml
```

```bash
helm template --values elasticsearch-values.yml elasticsearch elastic/elasticsearch > k8s/elastic.yaml
```

```bash
helm template kibana elastic/kibana > k8s/kibana.yaml
```