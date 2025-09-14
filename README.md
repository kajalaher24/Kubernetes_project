Kubernetes Mini projects

ClickCounter Kubernetes Project

A simple web application deployed on Kubernetes that counts clicks using a Redis backend. 
This project demonstrates core DevOps skills including containerization, YAML configuration, service exposure, and namespace management.


##  Tech Stack

- **Frontend**: Python Flask
- **Backend**: Redis
- **Containerization**: Docker
- **Orchestration**: Kubernetes
- **Platform**:  Local Cluster

---

##  Folder Structure

clickcounter-k8s-mini-project/
 ├── namespace.yaml 
 ├── redis-deployment.yaml 
 ├── redis-service.yaml 
 ├── clickcounter-deployment.yaml 
 ├── clickcounter-service.yaml 
 ├── screenshots/ │
   ├── pods-status.png 
   │ └── curl-response.png
 
 
---

##  Kubernetes Setup

### 1. Create Namespace
kubectl apply -f namespace.yaml

2. Deploy Redis:

kubectl apply -f redis-deployment.yaml
kubectl apply -f redis-service.yaml

3. Deploy ClickCounter App: 

kubectl apply -f clickcounter-deployment.yaml
kubectl apply -f clickcounter-service.yaml

4.Test App with curl: 
curl http://<NodeIP>:<NodePort>

Some other Kubernetes commands:

kubectl describe Deployment -n clickapp -- To describe deployments
kubectl describe service  -- To describe services
kubectl get pods -n clickapp -- To check pods name and their status
