# Projet 4 : Déployer une architecture n-tiers pour une PME

[Sujet du projet](https://openclassrooms.com/fr/paths/734/projects/1382/assignment) · Entreprise fictive : **BeeSafe**, une start-up d'assurance

## Mission

En tant qu'administrateur systèmes et réseaux de BeeSafe, déployer une architecture 3-tiers sur trois serveurs Linux :

| Serveur | Rôle | Logiciel |
|---|---|---|
| SRVweb | Serveur web | Apache 2.4 et PHP 8.0 |
| SRVsql | Base de données | MySQL 8.0 |
| SRVdns | DNS du site `www.beesafe.co` | Bind9 |

## Réalisation

1. Déployer les 3 machines virtuelles.
2. Installer Apache sur SRVweb, MySQL sur SRVsql et Bind9 sur SRVdns.
3. Créer la base de données et un compte d'exploitation MySQL dédié.
4. Connecter le site (SRVweb) à la base de données (SRVsql).
5. Configurer la zone DNS pour que `www.beesafe.co` pointe vers SRVweb.

## Livrables

- Fichiers de configuration DNS avec le nom de domaine
- Configuration Apache avec le virtual host du site
- Script SQL de création du compte d'exploitation
- Fichier de configuration du site, modifié avec les identifiants de la base de données
- Schéma de l'architecture 3-tiers (PDF)

Les livrables ne sont pas publiés dans ce dépôt.

## Compétences

- Installer et configurer des services Linux : Apache, MySQL, Bind9
- Séparer les rôles d'une application sur plusieurs serveurs (architecture n-tiers)
- Virtualiser un environnement de travail
- Documenter une architecture

## Ressources

- [Initiez-vous à Linux](https://openclassrooms.com/fr/courses/7170491-initiez-vous-a-linux)
- [Administrez un système Linux](https://openclassrooms.com/fr/courses/7274161-administrez-un-systeme-linux)
- [Gérez votre serveur Linux et ses services](https://openclassrooms.com/fr/courses/1733551-gerez-votre-serveur-linux-et-ses-services)
- [Virtualisez votre architecture et vos environnements de travail](https://openclassrooms.com/fr/courses/2035806-virtualisez-votre-architecture-et-vos-environnements-de-travail)
- [Implémentez vos bases de données relationnelles avec SQL](https://openclassrooms.com/fr/courses/6971126-implementez-vos-bases-de-donnees-relationnelles-avec-sql)
