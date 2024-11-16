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

## 1- Lancement et vérification des pods et du service nodeport
### a-1- Lancement du pod simple-webapp-color-blue
````
kubectl apply -nproduction -f pod-blue.yml
````
### a-2- Vérification du pod simple-webapp-color-blue
````
kubectl get po  -n production -o wide
````
