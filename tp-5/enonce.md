# TP5: INTRODUCTION A HELM (minikube)

## Lien utile (étape d'installation de helm pour Kubernetes)
````
https://devopscube.com/install-configure-helm-kubernetes/
````

## Installation

### ==> Recuperation du script d'installation
````
curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/master/scripts/get-helm-3
````
### ==> Donnons les droits d'execution
````
chmod 700 get_helm.sh
````

### ==> Installation d'openssl
````
sudo yum install openssl
````

### Telechargeons helm
````
./get_helm.sh
````

### Verifions la version de helm
````
helm version
````
## ################################ Déploiement WordPress ################################

### Lien utile
````
https://devopscube.com/install-configure-helm-kubernetes/
````

### Recuperation des charts fournit par bitnami
````
helm repo add bitnami https://charts.bitnami.com/bitnami
````

### Redefinition des valeurs de deploiement de notre wordpress https://github.com/bitnami/charts/blob/main/bitnami/wordpress/values.yaml
````
vi values.yml
````

### Ajouter du contenu suivant

wordpressUsername: admin
wordpressPassword: password
service:
  type: NodePort
  nodePorts:
    http: "30008"
persistence:
  enabled: false
mariadb:
  primary:
    persistence:
      enabled: false

### Lançons le déploiement
````
helm install wordpress bitnami/wordpress -f values.yml
````

### Nettoyer l'environnement
````
helm uninstall wordpress
````
