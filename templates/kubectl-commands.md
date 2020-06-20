##   kubectl cheatsheet

Check current context
```bash
kubectl config current-context
```
List all nodes
```bash
kubectl get nodes
```
List all namespaces
```bash
kubectl get namespaces
```
Create resources from file 
```bash
kubectl apply -f https://kubernetes.io/examples/controllers/frontend.yaml
```
List all pods
```bash
kubectl get pods
```
List all pods in specific namespace
```bash
kubectl get pods --namespace=<INSERT_NAMESPACE_NAME_HERE>
kubectl get pods --namespace=streams
```
List all pods with specific labels
```bash
kubectl get pods -l environment=production,tier=frontend
```
List all service accounts
```bash
kubectl get serviceaccounts
```
Describe replicaset
```bash
kubectl describe rs/frontend
```