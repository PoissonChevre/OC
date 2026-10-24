# Projet 9 : Gérer le parc informatique d'une PME

[Sujet du projet](https://openclassrooms.com/fr/paths/734/projects/1387/assignment) · Domaine fictif : `BARZINI.LAN`

## Mission

Automatiser avec **Ansible** la gestion d'un parc mixte Linux et Windows :

1. **Monter un lecteur réseau** (partage SMB) sur les postes, sans GPO, avec des scripts Bash et PowerShell.
2. **Déployer une application** sur plusieurs postes : Kontrast sous Linux, Colour Contrast Analyser sous Windows (via Chocolatey).
3. **Appliquer une politique de mise à jour** des systèmes (patch management).

## Environnement

| Groupe Ansible | Machine | Rôle |
|---|---|---|
| `linux_srv` | srv-inf-002 | Serveur Debian : GLPI et Ansible |
| `ubuntu` | pfx-sit-002 | PC fixe du service IT |
| `win2k19_srv` | srv-inf-001 | Windows Server 2019 : AD DS, DNS, DHCP |
| `win10pro` | ppb-tst-001 | PC portable de test |

- Linux : connexion SSH par clé. Le mot de passe sudo est chiffré avec **Ansible Vault**.
- Windows : connexion **WinRM** avec authentification **Kerberos** (compte du domaine).

## Contenu

```
OC_P9_ansible/
├── ansible.cfg
├── hosts            # Inventaire
├── group_vars/      # Connexion de chaque groupe (SSH ou WinRM)
├── playbooks/
└── roles/
```

| Playbook | Rôles | Action |
|---|---|---|
| `playbook_mount_network_drive.yml` | `linux_mount_network_drive`, `win_mount_network_drive` | Monte le partage réseau (scripts Bash et PowerShell) |
| `playbook_deploy_cca_kontrast.yml` | `linux_deploy_kontrast`, `win_deploy_chocolatey`, `win_deploy_colour_contrast_analyser` | Installe l'outil de contraste sous Linux et Windows |
| `playbook_update_apt_win.yml` | `linux_apt_upgrade`, `win_update` | Met à jour les paquets apt, Windows Update et Chocolatey |

## Lancer un playbook

```bash
kinit u.ansible@BARZINI.LAN        # Ticket Kerberos pour les postes Windows
ansible-playbook -i hosts playbooks/playbook_update_apt_win.yml --ask-vault-pass
```

## Compétences

- Automatiser l'administration d'un parc Linux et Windows avec Ansible : inventaire, rôles, playbooks
- Écrire des scripts Bash et PowerShell avec les bonnes pratiques : en-tête, variables, commentaires, conditions
- Connecter Ansible à Windows (WinRM, Kerberos) et protéger les secrets (Ansible Vault)
- Mettre en place une politique de mise à jour (patch management)
