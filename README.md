# Intro

Sample teste with istio using k3d to know how it works.

## Important links

- [k3d](https://k3d.io/)
- [Istio](https://istio.io/)

## Istio dashboard addons: Grafana, Jaeger, Kiali and Phometheus

### How to install

```sh
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/grafana.yaml
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/jaeger.yaml
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/kiali.yaml
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/prometheus.yaml
```

### How to run

```sh
istioctl dashboard grafana
istioctl dashboard jaeger
istioctl dashboard kiali
istioctl dashboard prometheus
```
