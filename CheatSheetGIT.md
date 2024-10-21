# CheatSheet

## Historique
- Créateur de git : Linus Torvalds (créateur du noyau du système d'exploitation Linux)
- Pourquoi la création de git? Besoin => pas d'outils équivalent
- Prix de la licence git => Gratuit, il est Open Source

## Gestionnaire de version de code
Différence entre SVN et GIT => GIT n'st pas forcément adpaté pour la gestion de très gros fichiers

## Pourquoi apprendre Git ?
- Logiciel est de très le plus utilisé  
- Open Source
- Permet de travailler seul et/ou en groupe

## Linux = macOS != Windows
DEF Linux: Une commande Linux est un programme ou un utilitaire qui s'exécute sur la ligne de commande. Une ligne de commande est une interface qui accepte des lignes de texte et les transforme en instructions pour votre ordinateur.
Toute interface utilisateur graphique n'est qu'une abstraction de programmes en ligne de commande. Par exemple, lorsque vous fermez une fenêtre en cliquant sur le "X", il y a une commande qui s'exécute derrière cette action.
Un drapeau (flag) est un moyen de passer des options à la commande que vous exécutez. La plupart des commandes Linux ont une page d'aide que nous pouvons appeler avec le drapeau -h. La plupart du temps, les drapeaux sont optionnels.
Un argument ou paramètre est l'entrée que nous donnons à une commande pour qu'elle puisse s'exécuter correctement. Dans la plupart des cas, l'argument est un chemin de fichier, mais il peut être n'importe quoi que vous tapez dans le terminal.
Vous pouvez invoquer des drapeaux en utilisant des traits d'union (-) et des doubles traits d'union (--), tandis que l'exécution des arguments dépend de l'ordre dans lequel vous les passez à la fonction.

=> Linux et Windows peuvent fonctionner sur n'importe quel machine != macOS fonctionne uniquement sur le même matériel

Linux et Windows sont écrit en ARM

Powershell => ligne de commande windows

### Pourquoi apprendre à utiliser UNIX ?
DEF:  famille de systèmes d'exploitation multitâche et multi-utilisateur
- Mise en ligne d'un site ou d'une application web (server FTP => FileZilla)
- Outils de dev disponible
- Ligne de commande "propres"
- Gestionnaire de paquets

## Origin
GitHub, GitLab, GitServer (NAS / Rasberry) => logiciel
Origin: ressemble à OneDrive
Fonctionnalités => Server
2FA => 2 Facteurs d'authentification
Clé de sécurité (clé SSH) ⇒ permet une authentification entre 2 appareils

## Ligne de commande

``` bash 
/* Liste */

apt-get => installer ou supprimer une application

touch => créer des fichiers

ping => recevoir les données

mkdir => créer un dossier

ls => lister les infos dans le dossier select

-a => afficher les fichiers cachés

cd => permettre de se déplacer dans les dossiers

cd .. => remonter dans le dossier précédent

cd ~ => remonter dans home ( dossier principal)

cat => lire un dossier

pwd => connaitre le chemin du répertoir de travail

mv => déplacer / renommer un fichier

mv *.(nom extension fichier en commun) => déplacer les fichiers avec le même nom d’extension

cp => copier un fichier

cp -r => copier dossier

rm => supprimer un fichier

rm -r => supprimer un dossier

clear => nettoyer la ligne de commande

code . => ouvrir le dossier dans VSC

/* Create a new repository on the command line (projet vide) */

git init
git commit -m "first commit"
git branch -M main
git remote add origin (url du repositories)
git push -u origin main

/* Push an existing repository from the command line (projet existant) */

git remote add origin (url du repositories) branch -M main
git push -u origin main

/*Commande GIT*/

Si “fatal: not a git repository” => pas de .git → faire git init

git init => initialiser le repositories (en local)

git clone => cloner un projet de github sur ordi

git status => état actuel des fichiers

git log => listing
:q pour sortir

git branch => créer une nouvelle branch

git add => ajouter les modifs du fichier pour commit

git add . => Stage Seleted Ranges (ajouter toutes les modifs du fichiers pour commit)

git stash => permettre de côté le code

git stash  apply => permet de récupérer le code mis de côté

git push -u origin main => command pour dire qu’on push toujours sur origin main, sans avoir besoin de  le renoter

git reset => annuler un commit / permet de revenir en arrière en supprimant tous les commit après le commit visé

/*Code*/
git reset (+nom du commit select)
git push -f
(git stash)

git revert => annuler un commit  / créer un commit inverse en supprimant un commit précis

/*Code*/
git revert (+ nom du commit supprimer)
git commit (du revert)
git push


git commit -m "le message du commit" => ajouter un commit (-m => nom du commit)

git pull => mettre à jour la branch local par rapport à la branch origin

git push => mettre à jour la branch origin par rapport à la branch local

git checkout (+nom de la branche) => se déplacer sur une autres branch

git checkout -b => se déplacer et créer une autre branch

git merge => copier tous les commit assemblé d’une branch liée à local

git rebase main => mise à jour de la dernière version de main dans la nouvelle branch

git flow =>
    git checkout main
    git pull
    git checkout -b (nom de la nouvelle branch)

    /* Plusieurs répétitions (commit les modifs) */

    git add .
    git commit -m
    git rebase main
    git push

    => GitHub : créer merge request + reviewer 
	=> attendre probation / modification
	=> merge request : rebase and commit
	=> retour VSC
	
	git checkout main
	git pull

/* Branch rules (règles d’une nouvelle collaboration) */

    restrict deletions
    require linear history
    require deployments to succeed
    require a pull request befoore merging
        require approvals 1
        require review from code Owners
        dismiss state pull request approvals when new commits are pushed
    require statuts cheks to pass
    block force pushes


/*VSC*/

ctrl + ù/% => ouverture du terminal

```

## Sources
