
# Exercice 2

## Manuel

1. 	La commande which permet de donner le chemin qui va êter parcouru pour lancer le fichier. whatis which 

2. 	chercher le terme option dans le manuel : man which | grep -B 2 -A 2 option (-B line before/-A line After)
	man which -> /option

3. 	Pour quitter le manuel : q / CTRL+Z

4. man 6 which (marche pas car which n'a pas - section)
   ex : man 6 intro

## Navigation dans l'arborescence des fichiers

1. 	Aller dans /var/log : cd /var/log

2. 	Revenir dans le dossier parent avec chemin relatif: cd ..

3. 	Revenir dans le possier personnel : cd /home/cpe	|	cd ~

4. 	Revenir au dossier précedent sans utiliser de chemin : cd ..

5. 	Accéder à /root : Acces denied

6. 	Ca ne marche pas, cd est une commande et non un programme et le sudo est juste pendant l'execution, une fois l'éxecution l'user normal se trouve dans un dossier ou il n'a pas de droit
une erreur est donc visible.

7. 	Créer un dossier : mkdir Nom_Dossier
	Créer un fichier : touch Nom_fichier
   
8. 	Supprimer un fichier : rm dossier/fichier

9. 	Supprimer un dossier : rm -rf dossier/ (-R récursif supprime dossier et son contenue/ -F force le delete) | rmdir dossier/ (pour un dossier vide)

10. rmdir dossier_non_vide erreur car non vide

11. rm -rf dossier_non_vide

## Commandes importantes

	
1. 	Afficher date + heure : date
	Commande time : Permet de calculer le temps que mets le programme COMMAND à s'executer.
	
2.	Afficher les dossier : ls
	Afficher tous : la
	Les fichiers commencant par un . sont des dossiers ou des fichiers cachés
	
3. 	Trouver programme : which programme
	which ls = /usr/bin/ls
	
4. 	Afficher les allias : allias

5.	Afficher contenu dossier distant : ls /route

6. 	Afficher contenue dossier précedent : ls ..

7.	Afficher chemin d'accès courant : pwd

8.	Creer le fichier plop et écrit à l'intérieur en ecrasant le contenu : echo 'yo' > plop

9.	Creer le fichier plop et écrit à l'intérieur en ajoutant le contenu à la fin l'existant : echo 'yo' >> plop

10. Déterminer type du fichier : file nom_fichier

11.	Lier deux fichiers entre eux : ln fichier1 fichier2
	Si modif un des deux fichier, l'autre sera modifié. Si delete fichier1, fichier2 toujours présent avec contenu
	
12.	Créer lien symbolique entre 2 fichiers : ln -s fichier1 fichier2
	Si delete fichier1, fichier2 vide. Leur contenu est lié
	
13.	Afficher fichier : cat nom_fichier 
	ctrl + S pour stopper / ctrl + q pour reprendre

14.	Afficher 5 première lignes d'un fichier : head -n 5 fichier
	Afficher 15 dernières lignes d'un fichier : tail -n 15 fichier
	Afficher lignes 10 à 20 d'un fichier : head -n 20 fichier | tails -n 10
	
15.	Afficher tous les messages du kernel : dmesg
	Afficher un fichier page par page : less

16.	/etc/passwd contient les informations sur les comptes utilisateurs
	Afficher manuel de passwd : man passwd
	
17.	Afficher ordre inverse alphabétique et première colonne: sort -dr passwd | cur -d: -f1

18.	Afficher nombre d'utilisateur : wc -l passwd

19.	Compter nombre de mot dans le manuel : man -k mot | wc -l

20.	Trouver tous les fichiers ayant un nom précis : sudo find / -name "nom" 

21.	Met le résultat dans /list_passwd_file.txt et les erreurs dans /dev/null : sudo find / -name "nom" > ~/list_passwd_file.txt 2> /dev/null

22.	Comment et ou est défini l'allias "ll" : grep -r "ll="

23.	Localsier un fichier : locate fichier

24.	Car non présent dans la db de locate. Faire updatedb puis le locate marche

# Exercie 4

1. Faire une copie cp .bashrc .bashrc_bak

3. Recharger le fichier bashrc source : ~/.bashrc ou . ~/.bashrc 
