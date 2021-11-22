# rand-microservices

# Istio Install

## Install the istio base and controller

Create the **istio-system** namespace

```
kubectl create namespace istio-system
```

Create the istio base deployment:
```
helm install istio-base ./deploy/kubernetes/helm-chart-istio/base -n istio-system
```
After that deploy the istio service discovery **istiod** chart
```
helm install istiod ./deploy/kubernetes/helm-chart-istio/istio-control/istio-discovery -n istio-system
```