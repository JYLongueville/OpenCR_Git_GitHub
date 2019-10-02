# OpenCR_Git_GitHub

Le projet contient
* un Readme créé à l'inistialisation du projet sur GitHub
* Fichier_01.txt deplace sous repert_01 créé via Gihub
* Fichier_02.txt créé sous repert_01 créé via Gihub
* Depuis le PC :  creation copie de repert/fichier_01.txt à la racine
* Git_p2_activité au format d'origine et zippé

GIT cmd
* 1ere tentative de git commit -am ==> failed
* 2eme tentitve avec git commit -a -m
* 3eme tentative avec git add puis git commit, l'option -a -m ne prenant en compte que ce qui est déjà dans l'index du precedent commit, donc pas lses nouveaux fichiers non encore commités.

Note destinée à l'auteur du cours  
Bon cours, il faudrait ajouter sur les fins de chapitre un recap des commandes vues.

## Antiseche
### Installation
Windows : https://msysgit.github.io/  
Configuration de l'accés:
```
git config --global user.name "Votre nom ou pseudo"  
git config --global user.email "votre@email.com"  
```


### Commandes locales
| Command       | Comment           |
| ------------- |:-------------:| 
| git init      | Active un dossier comme repository GIT <br>  Creer le dossier puis se placer dedans|  
| git add \<fichier> <br> git -a \<fichier> | Ajout du dossier dans l'index|   
| git commit -m "message" | Enregistrement des modifications      |   
| git commit -- amend -m "message" | Modification du message précédemment saisi  |   
| git commit -a -m "message" | Ajoute à l'index et enregistre les modifications      |    
| git status | Affiche l'état des fichiers du dossier non encore commités      |
| git log | Affiche l'hitorique des modifications enregistrées      |    
| git checkout \<commitSHA> | Recharge l'etat de l'enregistrement associé au SHA  |    
| git checkout master | Recharge le dernier enregistrement de la branche master  |  
| git revert \<commitSHA>  | Recharge à l'état précédent l'enregistrement associé au SHA + commit (inscrit à l'historoique)le dernier enregistrement de la branche master  |    
| git reset --hard  | Annule toute modification non encore enregistrée (commitée) |    

### Commandes distantes
| Command       | Comment      |
| ------------- |:-------------:|
| git clone \<gitWebURL>      | Copie integrale du repository distant localement |
| git push origin master      | remonte les modification enregistrées localement vers la branche master du repo distant |
| git pull origin master      | descend  les modification enregistrées de la branche master du repo distant vers le systeme local |

### Commandes de branches
| Command       | Comment      |
| ------------- |:-------------:|
| git branch \<nouvelleBranche>      | creation d'une nouvelle branche localement |
| git branch      | Liste les branches (* devant la branche active) |
| git checkout \<uneBranche>      | Position sur une branche, au dernier enregistrement |
| git checkout -b \<nouvelleBranche>      | creation d'une nouvelle branche et positionement dessus |
| git merge \<brancheCible>      | Fusion de la branche cible sur la branche courante |

NB: si le merge genere un conflit:
* editer le fichier poure resoudre les conflits
* git add  \<leFichierMergéCorrigé>
* git commit (sans commentaire)
