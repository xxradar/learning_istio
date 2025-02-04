## ISTIO Learning
### Deploy app
- Deploy app-routable-demo
- Label the namespace
```
kubectl label namespace app-routable-demo istio-injection=enabled
```
- Restart deployments
```
kubectl rollout restart deployment -n app-routable-demo echoserver-1-deployment echoserver-2-deployment nginx-zone1 nginx-zone2 nginx-zone3 nginx-zone4 nginx-zone5 siege-deployment
```
### Ingress
- Create a Gateway (namespaced)
- Create a VirtualService (namespaced)

The example only works on /app1 and /app2 (because of prefix in VirtualService)
```
kubectl port-forward svc/kiali 20001:20001 -n istio-system
```
