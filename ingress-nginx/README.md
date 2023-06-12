# NGINX

Votre proxy qui controlera l'accés à vos application ! 
J'ai rajouté dans controller.config la configuration suivante permettant de proteger l'accès à mes services interne : 
```
whitelist-source-range: 192.168.65.0/24,176.151.84.188/32
```

A vous de changer par rapport à votre infra, vous pouvez même le retirer si ca vous gène.
Il faut adapter le values.yaml avec votre configuration.