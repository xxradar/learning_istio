## ISTIO Learning
- Create a Gateway (namespaced)
- Create a VirtualService (namespaced)

The example only works on /app1 and /app2 (because of prefix in VirtualService)
```
kubectl port-forward svc/kiali 20001:20001 -n istio-system
```
