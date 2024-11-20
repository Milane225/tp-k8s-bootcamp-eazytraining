TP4: GESTION DU STOCKAGE (minikube et eazylabs)
VOLUME

````
kubectl apply -f mysql-volume.yml
````
````
kubectl get po -o wide
````
````
kubectl port-forward mysql-volume 3306:3306 --address 0.0.0.0
````

APPLY VOLUME

````
kubectl get po -o wide
````
````
kubectl delete  -f mysql-volume.yml
````
````
kubectl get po -o wide
````
PV

````
kubectl apply -f pv.yml
````
````
kubectl get pv -o wide
````
````
kubectl get pv pv -o wide
````
````
kubectl describe  pv pv
````
PVC

````
kubectl apply -f pvc.yml
````
````
kubectl get pvc pvc -o wide
````
````
kubectl describe  pv pv
````
APPLY PV AND PVC
````
kubectl apply -f mysql-pv.yml
````
````
kubectl describe  po mysql-pv
````
````
kubectl get po
````
