apiVersion: networking.k8s.io/v1
kind: NetworkPolicy
metadata:
  name: allow-ingress
spec:
  podSelector:
    matchLabels:
      app: web-production
  policyTypes:
  - Ingress
  ingress:
  - from:
    - namespaceSelector:
        matchLabels:
          kubernetes.io/metadata.name: ingress
    - podSelector:
        matchLabels:
          app.kubernetes.io/instances: nginx
    ports:
    - protocol: UDP
      port: 3000
