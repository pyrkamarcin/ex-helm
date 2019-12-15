# Install Helm packages

```
helm install --values fluentd-values.yml fluentd kiwigrid/fluentd-elasticsearch
```

```
helm install --values elasticsearch-values.yml elasticsearch elastic/elasticsearch
```

```
helm install kibana elastic/kibana
```

# Generate manifests

```
helm template --values fluentd-values.yml fluentd kiwigrid/fluentd-elasticsearch > k8s/fluentd.yaml
```

```
helm template --values elasticsearch-values.yml elasticsearch elastic/elasticsearch > k8s/elastic.yaml
```

```
helm template kibana elastic/kibana > k8s/kibana.yaml
```