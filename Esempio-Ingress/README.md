- minikube start

- minikube addons enable ingress

- kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v2.7.0/aio/deploy/recommended.yaml
```
# Dashboard Ingress 
apiVersion: networking.k8s.io/v1
kind: Ingress
metadata:
  name: dashboard-ingress
  annotations:
    nginx.ingress.kubernetes.io/backend-protocol: "HTTPS"
  namespace: kubernetes-dashboard
spec:
  rules:
  - host: dashboard.com
    http:
      paths:
        - pathType: Prefix
          path: "/"
          backend:
            service:
              name: kubernetes-dashboard
              port:
                number: 443   
```


- kubectl apply -f dashboard-ingress.yaml

- kubectl get ingress -n kubernetes-dashboard

- echo "$(minikube ip) dashboard.com" | sudo tee -a /etc/hosts

- dashboard.com