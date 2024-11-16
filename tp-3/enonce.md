# TP-3 ESTION DU RESEAU SUR EAZYLABS

## 1- Lancement et vérification du namespace
### a- Lancement du namespace
```
kubectl apply -f namespace.yml
```
### b- Vérification du namespace
```
kubectl get namespace
```

## 2- Lancement et vérification des pods et du service nodeport
### a-1- Lancement du pod simple-webapp-color-blue
````
kubectl apply -n production -f pod-blue.yml
````
### a-2- Vérification du pod simple-webapp-color-blue
````
kubectl get po  -n production -o wide
````
### b-1- Lancement du pod simple-webapp-color-red
````
kubectl apply -n production -f pod-red.yml
````
### b-2- Vérification du pod simple-webapp-color-red
````
kubectl get po  -n production -o wide
````
### C-1- Lancement du service nodeport
````
kubectl apply -n production -f service-nodeport-web.yml
````
### b-2- Vérification du service nodeport
````
kubectl get services -n production
kubectl get svc -n production
````

## 3- Suppression des pods, service nodeport et du namespace
### a- Suppression du pod simpe-webapp-color-blue
````kubectl delete -n production -f pod-blue.yml````
### b- Suppression du pod simpe-webapp-color-red
````kubectl delete -n production -f pod-red.yml````
### c- Suppression du service nodeport
````kubectl delete -n production -f service-nodeport-web.yml````
### d- Suppression du namespace
````kubectl delete -f namespace.yml````
