# JELLYFIN

Jellyfin est le serveur principale de notre stack, celle qui sera accessible par l'ensemble de nos utilisateurs.
La configuration est assez simple, il suffit d'avoir accés au même répertoire de films et de series que vos autres applications.
Jellyfin se chargera de faire l'import et le reste.
La configuration est sauvegardé dans le dossier /config du serveur.
Une annotation au niveau de l'ingress permet de la rendre accessible globalement sur internet, vous pouvez la commenter si vous êtes uniquement sur un lab interne.

Pour pouvoir le configurer : [Configuration Jellyfin](https://jellyfin.org/docs/general/administration/configuration)