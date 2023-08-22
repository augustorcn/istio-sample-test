# Intro

Content from Full Cycle course on Istio Service Mash module.
Sample teste with istio using k3d to know how it works.

## Important links

- [k3d](https://k3d.io/)
- [Istio](https://istio.io/)

## Create k8s cluster

```sh
k3d cluster create -p "8000:30000@loadbalancer" --agents 2
```

## Install Istio on cluster

```sh
istioctl install -y
```

## Run k8s manifests

```sh
kubectl apply -f .
```

## Istio dashboard addons: Grafana, Jaeger, Kiali and Phometheus

### How to install

```sh
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/kiali.yaml && \
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/grafana.yaml && \
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/jaeger.yaml && \
kubectl apply -f https://raw.githubusercontent.com/istio/istio/release-1.18/samples/addons/prometheus.yaml
```

### How to run

```sh
istioctl dashboard grafana
```

```sh
istioctl dashboard jaeger
```

```sh
istioctl dashboard kiali
```

```sh
istioctl dashboard prometheus
```

## Testing A and B deployments with load balance

### Run this script and access Kiali dashboard

```sh
while true
do      
    curl http://localhost:8000
    sleep 0.5
done
```
