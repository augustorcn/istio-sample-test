# Intro

Sample teste with istio to know how it works.

# Add istio addons: Grafana, Jaeger, Kiali and Phometheus

```sh
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/grafana.yaml
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/jaeger.yaml
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/kiali.yaml
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/prometheus.yaml
```
