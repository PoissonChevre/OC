# Projet 10 : Mettre en place une nouvelle solution de sauvegarde

## Objectif

Tester deux stratégies de sauvegarde, puis choisir la politique à mettre en production :

- **Stratégie 1** : sauvegarder les **données** de chaque machine (sources d'un site web, répertoires utilisateurs d'un partage réseau…).
- **Stratégie 2** : sauvegarder les **machines virtuelles** entières, sans tenir compte des données qu'elles contiennent.

## Solution

Des scripts Bash basés sur **rsync**, qui envoient les sauvegardes par SSH (clé sans mot de passe) vers le serveur `backup-srv`.

Un répertoire par type de données : `FICHIERS`, `MAILS`, `MACHINES`, `RH`, `SITE`, `TICKETS`. Les journaux sont écrits dans `/var/log/rsync/`.

| Script | Rôle | Exemple |
|---|---|---|
| `incr_backup.sh` | Sauvegarde incrémentale, avec une sauvegarde complète un jour fixe | `./incr_backup.sh TICKETS 7 7` : complète le dimanche, rétention 7 jours |
| `incr-backup_2.sh` | Variante incrémentale : garde toujours au moins les deux dernières sauvegardes | `./incr-backup_2.sh TICKETS 7` |
| `diff_backup.sh` | Sauvegarde différentielle : les changements depuis la dernière complète | `./diff_backup.sh MACHINES 7 7` |
| `restore.sh` | Restauration interactive d'un fichier ou d'un répertoire complet | `./restore.sh` |

## Compétences

- Définir une stratégie de sauvegarde : complète, incrémentale, différentielle, rétention
- Automatiser des sauvegardes avec rsync et des scripts Bash
- Restaurer des données
