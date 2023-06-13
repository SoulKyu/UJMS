# scaleway-ddns
Ce petit service permet de s'assurer que si mon IP public sur ma box venait à changer, mes records DNS restent bien à jours pour que mes utilisateurs puissent continuer d'utiliser mes services.
C'est un service très simple que vas récupèrer mon IP public sur l'API d'un service externe nommé api-ipv4.ip.sb et qui vas ensuite faire une requête API sur mon domain chez scaleway pour mettre à jours mon record.

Il faut configurer le fichier configmap pour renseigner vos différentes informations.
C'est tout légé, et c'est bien pratique.

/!\ Ne fonctionne qu'avec scaleway /!\