# Microservices Deployment on Minikube

## 1️⃣ Minikube Setup
- `minikube start`
- `minikube addons enable ingress`
- `minikube tunnel`

## 2️⃣ Build & Load Images
- `docker build -t user-service:latest .`
- `minikube image load user-service:latest`
- Same for other services.

## 3️⃣ Deploy
- `kubectl apply -f deployments/`
- `kubectl apply -f services/`
- `kubectl apply -f ingress/`

## 4️⃣ Test
- `kubectl port-forward svc/user-service 8080:3000`
- Or test via Ingress: `curl http://<Ingress-IP>/api/users`

## Troubleshooting
- Use `kubectl describe` for pods and services.
- Check logs: `kubectl logs <pod>`
- Use `minikube dashboard` for visual check.
