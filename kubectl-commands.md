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
List all resources in specific namespace
```bash
kubectl get all -n <namespace>
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
kubectl get pods --namespace=<namespace>
```
List all pods and show all labels
```bash
kubectl get pods --show-labels
```
List all pods in all namespaces
```bash
kubectl get pods --all-namespaces
```
List all pods with specific labels
```bash
kubectl get pods -l environment=production,tier=frontend
```
List all pods with labels, node info, etc.
```bash
kubectl get pods -o wide --show-labels
```
Get the raw json or yaml for a pod
```bash
kubectl get pods/<podname> -o yaml
kubectl get pods/<podname> -o json
```
Get logs from pod
```bash
kubectl logs <podname>
```
Delete a pod or pods
```bash
kubectl delete pods <podname>
kubectl delete pods -l <labelname>=<labelvalue>
```
Edit a pod (Opens Pod manifest in vim)
```bash
kubectl edit pod <podname>
```
Describe replicaset
```bash
kubectl describe rs/<replicasetname>
```
Scale a deployment
```bash
kubectl scale deploy core-financial --replicas=0
```
List all service accounts
```bash
kubectl get serviceaccounts
```
<i>Some of the above commands assume the resources are in the default namespace. You have to specify the namespace otherwise.</i>

## Resources Short Names
```bash
namespaces / ns
pods / po
replicaset / rs
deployment / deploy
statefulset / sts
services / svc
serviceaccounts / sa
persistentvolumeclaims / pvc
endpoints / ep
daemonsets / ds
persistentvolumes / pv
ingresses / ing
customresourcedefinitions / crd
```

## kubectl help commands

Complete list of supported resources
```bash
kubectl api-resources
```
Get detailed description of that resource
```bash
kubectl explain pods
```