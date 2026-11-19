# SIGMA Sonar Serveur · téléchargement

Installateur du **serveur Sonar** pour le PC admin d'un labo : le dashboard (retrouver le PC d'un élève
et le faire sonner), la base de données et les sauvegardes, tout compris.

## Télécharger

**[⬇ SIGMA-Sonar-Serveur-Setup.exe : dernière version](https://github.com/Nels-G/SIGMA-Sonar-Serveur/releases/latest/download/SIGMA-Sonar-Serveur-Setup.exe)**

Toutes les versions : [Releases](https://github.com/Nels-G/SIGMA-Sonar-Serveur/releases) ·
Page de téléchargement : [nels-g.github.io/SIGMA-Sonar](https://nels-g.github.io/SIGMA-Sonar/#serveur)

## Installer

1. Sur le PC admin du labo, lancer **`SIGMA-Sonar-Serveur-Setup.exe`** (droits administrateur) :
   Suivant, J'accepte, dossier, **dossier des sauvegardes**, Installer.
2. Sonar s'ouvre dans sa propre fenêtre (raccourci **Sonar** sur le Bureau) : créer le compte administrateur, puis le nom et le logo du labo.
3. Installer le programme **SIGMA** sur les PC du labo : ils trouvent ce serveur tout seuls.

Depuis un autre PC ou un téléphone du réseau : **`http://nom-du-pc`** (ou son adresse, ex. `http://192.168.1.10`).

## Ce qui est installé

- Le serveur Sonar et son dashboard, qui **démarrent avec le PC** (même sans session ouverte) et se relancent s'ils s'arrêtent.
- Une base **PostgreSQL 17** réservée à ce PC (port 5433, aucune connexion depuis le réseau).
- Une **sauvegarde quotidienne** dans le dossier choisi (les 30 dernières sont gardées), et avant chaque mise à jour.
  Pour les avoir aussi en ligne : un dossier Google Drive (mode « Mettre en miroir les fichiers ») ou OneDrive.
- Les **mises à jour automatiques** (chaque nuit et au démarrage du PC), sans perte de données.
- Une règle du pare-feu Windows pour le port web (80 ; 8000 seulement si le port 80 est déjà pris sur ce PC).
- Le dashboard installable comme application, avec des notifications Windows quand un nouveau PC attend d'être accepté.

La désinstallation garde les données (`C:\ProgramData\SigmaSonarServeur`) pour pouvoir réinstaller sans rien perdre.

**Prérequis** : Windows 10 ou 11, 64 bits, avec Microsoft Edge (déjà présent sur Windows).

En cas de problème : `C:\ProgramData\SigmaSonarServeur\journaux\installation.log`.

---

Ce dépôt ne contient que les versions publiées. Le code source est privé.
