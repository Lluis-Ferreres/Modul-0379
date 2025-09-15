### Ordres bàsiques de Git

Per utilitzar Git, els desenvolupadors utilitzen ordres específiques per copiar, crear, canviar i combinar codi. Aquestes ordres es poden executar directament des de la línia d'ordres o mitjançant una aplicació com GitHub Desktop. Aquí hi ha algunes ordres habituals per utilitzar Git:

- **git init** inicialitza un repositori Git nou i comença a fer un seguiment d’un directori existent. Afegeix una subcarpeta oculta dins del directori existent que allotja l'estructura de dades interna necessària per al control de versions.

- **git clone** crea una còpia local d’un projecte que ja existeix remotament. El clon inclou tots els fitxers, historial i branques del projecte.
  
- **git add** fa un canvi. Git fa un seguiment dels canvis a la base de codis d’un desenvolupador, però és necessari escenificar i fer una instantània dels canvis per incloure’ls a la història del projecte. Aquesta ordre realitza la posada en escena, la primera part d'aquest procés de dos passos. Qualsevol canvi que es realitzi es convertirà en una part de la següent instantània i en la història del projecte. Posar en marxa i comprometre’s per separat proporciona als desenvolupadors un control complet sobre la història del seu projecte sense canviar la manera de codificar i funcionar.
	
- **git commit** desa la instantània a l'historial del projecte i completa el procés de seguiment de canvis. En resum, un commit funciona com fer una foto. Tot el que s’hagi posat en escena git add passarà a formar part de la instantània git commit.
 
- **git status** mostra l'estat dels canvis com a no rastrejats, modificats o progressius.
	
- **git branch** mostra les branques que s’estan treballant localment.

- **git merge** combina línies de desenvolupament juntes. Aquesta ordre s'utilitza normalment per combinar els canvis fets en dues branques diferents. Per exemple, un desenvolupador es fusionaria quan volia combinar els canvis d'una branca de funcions a la branca principal per al desplegament.

*Obteniu més informació a una guia de referència completa sobre les ordres de Git .*

---------------------------------------------------------
### Exemples
1. Exemple: contribuir a un repositori existent  
;; download a repository on GitHub.com to our machine  
*git clone https://github.com/me/repo.git*  
;; change into the `repo` directory  
*cd repo*  
;; create a new branch to store any new changes  
*git branch my-branch*  
;; switch to that branch (line of development)  
*git checkout my-branch*  
;; make changes, for example, edit `file1.md` and `file2.md` using the text editor  
;; stage the changed files  
*git add file1.md file2.md*  
;; take a snapshot of the staging area (anything that's been added)  
*git commit -m "my snapshot"*  
;; push changes to github  
*git push --set-upstream origin my-branch*

2. Exemple: iniciar un repositori nou i publicar-lo a GitHub
En primer lloc, haureu de crear un nou dipòsit a GitHub. Podeu aprendre a crear un repositori nou a la nostra guia Hello World . No inicialitzeu el dipòsit amb README, .gitignore o License. Aquest dipòsit buit esperarà el vostre codi.  
;; create a new directory, and initialize it with git-specific functions  
*git init my-repo*  
;; change into the `my-repo` directory  
*cd my-repo*  
;; create the first file in the project  
*touch README.md*  
;; git isn't aware of the file, stage it  
*git add README.md*  
;; take a snapshot of the staging area  
*git commit -m "add README to initial commit"*
;; provide the path for the repository you created on github  
*git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git*  
;; push changes to github  
*git push --set-upstream origin main*

3. Exemple: contribuir a una branca existent a GitHub
;; assumption: a project called `repo` already exists on the machine,  
;; and a new branch has been pushed to GitHub.com since the last time changes were made locally  
;; change into the `repo` directory  
*cd repo*  
;; update all remote tracking branches, and the currently checked out branch  
*git pull*  
;; change into the existing branch called `feature-a`  
*git checkout feature-a*  
;; make changes, for example, edit `file1.md` using the text editor  
;; stage the changed file  
*git add file1.md*  
;; take a snapshot of the staging area  
*git commit -m "edit file1"*  
;; push changes to github  
*git push*

---------------------------------------------------------
### Webs d'interès
[Tutorial bàsic](https://www.freecodecamp.org/espanol/news/guia-para-principiantes-de-git-y-github)

