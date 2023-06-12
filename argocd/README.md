# ARGOCD
ArgoCD est un élément essentiel de UJMS, il permet de gérer la synchonisation automatique de nos différentes applications et son maintien à jours.

Le fichier values.yaml doit dans un premier temps être configuré afin de l'adapter à votre infra, par example, il vas être nécessaire de changer le FQDN des domaines, le mot de passe et pas mal d'autre chose afin de répondre à vos particularité.

## Deploiement :
Une fois votre configuration validée, pour le déployer, c'est assez simple, on utilise la chart helm de bitnami : 
```helm upgrade -i argocd oci://registry-1.docker.io/bitnamicharts/argo-cd -f values.yaml -n argocd```

## Deploiement des applications : 
Avant de déployer les applications, il faudra bien s'assurer que chacun d'entre elle est configuré comme vous le souhaitez !
N'hésitez pas à changer la configuration selon vos besoins et particularité.

Sinon, il suffit de lancer la commande suivante : 
```kubectl apply -f applciation.yaml```