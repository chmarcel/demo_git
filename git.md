A faire dès qu'un depot github a été cloné en local (avant tout modif) :
- **git config core.sshCommand "ssh -i ~/.ssh/id_rsa_perso"**
- **git config user.name "chmarcel"**
- **git config user.email "mon email"**



activer un dossier comme repository Git :
- Dans le dossier, exécuter **git init**

Ajouter un fichier (après ajout ou modif) à l'index git avant un commit
- **git add <nom_fichier>**

Enregistrer les modifications
- **git commit -m "Un message parlant"**

Ou bien, les 2 opérations précédentes en simultané (si pas de fichier rajouté) :
- **git commit -am "Dernière modif"**

git status

git log : liste des commit
git log -p : liste des commit avec les détails des modifs



git checkout SHA2 : Se poistionner sur un commit donné
git checkout master (revient sur la branche principale)

annuler un commit (commit inverse)
git revert SHA2
Modifier le commit du dernier message
git commit --amend -m "Votre nouveau message"
Annuler les derniers changement (avant commit)
git reset --hard
ou
git checkout <nomfichier>

pull request : demande de modif faite à d'autres repo

copier un repo sur sa machine 
git clone URLREPO (https ou ssh)

Envoyer les modifs sur l'origine :
git push origin master (branche master)
git push origin ma-branche (branche ma-branche)
git push --all origin (toutes les branches)

Récupérer des modifs depuis l'origine
git pull origin master

## BRANCHES
### Liste des branches présentes en local :
git branch
### Créer une branche : 
git branch ma-branche
### Aller dans la branche : 
git checkout ma-branche
### Les 2 en même temps : 
git checkout -b ma-branche

### Fusionner les modifs de la branche B vers la branche A
- **git checkout brancheA** (on va dans la branche A)
- **git merge brancheB** (on fusionne la branche B dans la A)

### Effacer une branche
- **git branch -d <nom branche>** (branche locale)
- **git push origin --delete <nom branche>** (branche distante)

Reprendre les modifs effectuée sur master sur une branche X créée avant les modifs
Sur la branche x : git rebase master (uniquement si il n'y pas eu de push)

Qui a écrit cette ligne
git blame <nom fichier>

Détail d'un commit
git show SHA2

Fichier à ne pas versionner : .gitignore à la racine

Mettre de coté les modifs en cours (pour ne pas faire de commit superflus)
git stash
et pour revenir
git stash pop (supprime ce qu'il y avait dans la stash)
ou
git stash apply (pour garder ce qu'il y avait dans stash)


Pour voir ce qui a changé avant le commit
git diff
ou 
git diff <nomfichier>

POur contribuer à un projet github public
Aller sur le repo github
Faire un fork (bouton) (cela copie vers son propre repo)
clone en local
creer une branche
faire les modifs, commit et push de la branche
Sur le projet forké, faire compare et pull request



