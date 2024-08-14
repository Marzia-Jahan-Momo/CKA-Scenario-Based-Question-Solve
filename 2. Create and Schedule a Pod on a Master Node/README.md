### Questions:
1. **Create a Pod with Specific Image**  
   Create a single Pod named `pod1` with the image `httpd:2.4.41-alpine` in the `default` Namespace.

2. **Name the Container within the Pod**  
   Ensure the container inside the Pod is named `pod1-container`.

3. **Schedule Pod on a Master Node without Adding New Labels**  
   Configure the Pod to only be scheduled on a master node without adding any new labels to the nodes.


**Ans:**
```
kubectl get nodes   ### Copy the node name

kubectl run pod pod1 -image=httpd:2.4.41-alpine --namespace=default $d > mypod1.yaml

sudo vim mypod1.yaml
```
### Please check ```pod.yaml``` file

```
kubectl apply -f mypod1.yaml
```
```
kubectl get pod
```
```
kubectl describe pod pod1
```
```
kubectl get pod -o wide
```
