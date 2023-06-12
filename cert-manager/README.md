# CERT-MANAGER
Pour cert-manager, j'utilise scaleway pour l'authentification auprès de let's encrypt et la validation de mon identité.
Vous pouvez utiliser le provider que vous souhaitez, il suffit d'utiliser la documentation de cert-manager : 
[Les différents webhook disponible](https://github.com/topics/cert-manager-webhook)
Si votre provider DNS n'est pas dispo, à vous de créer le votre !

## Scaleway Webhook
Pour l'installation du webhook de scaleway il faut dans un premier temps généré des accés API : 
[Comment créer des clefs API](https://www.scaleway.com/en/docs/identity-and-access-management/iam/how-to/create-api-keys/ce)
Ensuite, il faut configurer les différents fichiers présent dans scaleway-webhook.