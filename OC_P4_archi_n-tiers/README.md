# PROJET 4 ***["Déployez une architecture n-tiers pour une PME"](https://openclassrooms.com/fr/paths/734/projects/1382/assignment)***

## I. Missions

Je suis administrateur syst§me cheeBeeSafe, une starip d'assurance, 
Pour le projet chez BeeSafe, en tant qu'administrateur systèmes et réseaux, ma mission consiste à déployer trois serveurs distincts pour mettre en place une architecture N-tiers robuste :

    Configuration d'un serveur web avec Apache 2.4 et PHP 8.0 sur une machine dédiée.
    Installation et configuration de MySQL 8.0 sur un serveur dédié pour gérer la base de données.
    Configuration de Bind9 sur une troisième machine afin de mettre en place le service DNS pour référencer le site web à l'adresse www.beesafe.co.

## II. Méthodologie et Réalisations

- Déployer les 3 Vms
- Installer le serveur Web APACHE2 - SRVweb
- Installer le serveur de BDD - SRVsql
- Installer le serveur DNS - SRVsql
- créer la BDD
- créer le compte d'exploitation sur mysql
- Connexion SRVweb <==> SRVsql
- Connexion SRVdns
- Compiler les fichiers de configuration pour les livrables
- Script SQL
- Fichier de config SQL
- Schéma Architecture

- [x] fichiers de configuration DNS qui intègrent le nom de domaine, nommés au format txt
- [x] fichiers de configuration du service HTTPD (Apache) qui intègrent le virtual host hébergeant le site au format txt
- [x] script SQL qui a permis de créer le compte d’exploitation de la base de données
- [x] le fichier de configuration des sources du prototype modifié pour intégrer les identifiants de connexion à la base de données
- [x] le schéma de l’architecture 3-tiers au format pdf

## III. Compétences et technologies acquises

- Concevoir la cartographie d'un réseau
- Construire un réseau TCP-IP
- Formaliser les procédures via une documentation technique

## IV. ressources consultées pour la réalisation du projet

- ["Initiez-vous à Linux"](https://openclassrooms.com/fr/courses/7170491-initiez-vous-a-linux)
- ["Administrez un système Linux"](https://openclassrooms.com/fr/courses/7274161-administrez-un-systeme-linux)
- ["Gérez votre serveur Linux et ses services"](https://openclassrooms.com/fr/courses/1733551-gerez-votre-serveur-linux-et-ses-services)
- ["Virtualisez votre architecture et vos environnements de travail"](https://openclassrooms.com/fr/courses/2035806-virtualisez-votre-architecture-et-vos-environnements-de-travail)
- ["Implémentez vos bases de données relationnelles avec SQL"](https://openclassrooms.com/fr/courses/6971126-implementez-vos-bases-de-donnees-relationnelles-avec-sql)


### 3. Tâches

- [x] Déployer les 3 Vms
- [x] Installer le serveur Web APACHE2 - SRVweb
- [x] Installer le serveur de BDD - SRVsql
- [x] Installer le serveur DNS - SRVsql
- [x] créer la BDD
- [x] créer le compte d'exploitation sur mysql
- [x] Connexion SRVweb <==> SRVsql
- [x] Connexion SRVdns
- [x] Compiler les fichiers de configuration pour les livrables
- [x] Script SQL
- [x] Fichier de config SQL
- [x] Schéma Architecture

### 4. livrables

- [x] fichiers de configuration DNS qui intègrent le nom de domaine, nommés au format txt
- [x] fichiers de configuration du service HTTPD (Apache) qui intègrent le virtual host hébergeant le site au format txt
- [x] script SQL qui a permis de créer le compte d’exploitation de la base de données
- [x] le fichier de configuration des sources du prototype modifié pour intégrer les identifiants de connexion à la base de données
- [x] le schéma de l’architecture 3-tiers au format pdf

