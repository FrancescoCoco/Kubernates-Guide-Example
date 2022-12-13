# COMANDI KUBERNATES LOCAL 

## MINIKUBE 
- minikube start 
- minikube start --vm-driver= hyperkit
- minikube service "nome-external-service"
- minikube addon enable ingress
- minikube delete 


## KUBECTL 
- kubectl get all
- kubectl get all -n "nome_namespace"
- kubectl get pod
- kubectl get service
- kubectl get replicaSet
- kubectl create deployment "nome-depl"
- kubectl get deployment 
- kubectl edit deployment "nome-depl"
- kubectl describe pod "nome-pod"
- kubectl logs "nome-pod"
- kubectl exec -it "nome pod" --bin/bash
- kubectl delete deployment "nome-depl"
- kubectl apply -f "nome-file.yaml"
- kubectl get pod -o wide 
- kubectl get deployment "nome-depl" -o yaml  
- kubectl get deployment "nome-depl" -o yaml > "nome-file.yaml"
- kubectl delete -f "nomefile.yaml"
- kubectl get secret 
- kubectl get ns 
- kubectl create namespace "nome-namespace"
- kubectl "nome namespace" --namespaced==false
- brew install kubectx 
- kubectl get ingress 
- brew install helm 