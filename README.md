# ***minikube-demo***

### ***🎯 Objective:***  
Deploy and manage a containerized application using Kubernetes on a local cluster powered by Minikube.
***Clone the repository: git clone https://github.com/asmat72/minikube-demo.git***

### ***🛠️ Tools Required:***
 - [Docker Desktop]
 - [Minikube]
 - [kubectl]

### ***📦 Deliverables:***
   - "deployment.yaml" and "service.yaml" files
   - Screenshots of:
   - "kubectl get pods".
   - "kubectl get services".
   - "kubectl describe" output.

### ***🚀 Step-by-Step Instructions:***
- Install Minikube
  - "bash" 
   - choco install minikube   # Windows (via Chocolatey)
- Install kubectl
   - choco install kubernetes-cli
- Start Minikube Cluster
   - minikube start
- Creat a "deployment.yaml" file
   - This file defines how your app is deployed in Kubernetes.
- Explanation:
   - kind: Deployment — tells Kubernetes to manage app replicas.
   - replicas: 2 — runs two instances of the app.
   - image: nginx — uses the official Nginx container.
   - containerPort: 80 — exposes port 80 inside the container.
- Apply Deployment
   - kubectl apply -f deployment.yaml
- Creat a "service.yaml" file 
   - This file exposes your app so it can be accessed. 
- Explanation:
   - kind: Service — defines a network endpoint.
   - type: NodePort — exposes the app on a port accessible from your machine.
   - port: 80 — service port. 
   - targetPort: 80 — container port.
- Apply Service
   - kubectl apply -f service.yaml
- Verify & Manage
   - Check Pods: "kubectl get pods"
   - Check Services: "kubectl get services"
   - Scale Deployment: "kubectl scale deployment my-app --replicas=4"
   - Describe Resources: "kubectl describe pod <pod-name>"
                         "kubectl describe service my-service"

### ***✅ Summary:***
   - This task helps you understand how to:
   - Set up a local Kubernetes cluster.
   - Deploy and expose containerized apps.
   - Scale and inspect deployments using kubectl.
        
           
           
