# INF1070ETE2024-LAB3

## Installation de GASH :     
 - Télécharger le `gameshell-labo03.tar`     
 - Dans le terminal (déplacer vous dans les téléchargements) utiliser `tar -xf gameshell-labo03.tar` :   
   `tar` : commande qui sert à archiver ou dé-archiver des fichiers.   
   `-x` : pour extraire.     
   `-f gameshell-labo03.tar` : spécifier l'archive à extraire.     
   
## Description :
 - Ma correction pour le jeu GameShell du labo3 du cours INF1070.
 - Les informations données au début du jeu ne sont pas importantes. (C'était le TP d'une session entérieure).     
 - Je promets d'avoir testé sur une distribution Linux. Cependant, ayant moi-même été victime de bugs, je vous recommande de faire des `gash restart` de temps en temps, voire même de recommencer depuis le début.

## Mission 1 :

```sh
cd Chateau/
cd Donjon/
cd Premier_etage/
cd Deuxieme_etage/
cd Haut_donjon/
```

## Mission 2 :

```sh
cd
cd Chateau/
cd Cave/
```
## Mision 3 :

```sh
cd
cd Chateau/Batiment_principal/Salle_du_trone/
```

## Mision 4 :

```sh
cd
cd Foret/
mkdir -p Cabane/Coffre/ 
```
`-p` : option qui permet de créer les dossiers intermédiares s'ils n'existent pas (Ici, `Cabane/` est créé comme intermédiaire). 

## Mission 5 : 

```sh
cd
cd Chateau/Cave/
rm rat? 
```
## Mission 6 : 

Assumant que je suis dans la Cave :
```sh
mv piece_? ~/Foret/Cabane/Coffre/
```
## Mission 7 : 

Avec la meme assomption : 
```sh
mv .piece_* ~/Foret/Cabane/Coffre/
```

## Mission 8 :

De meme :
```sh
cd .Terrier/
rm *_rat
```

## Mission 9 :

```sh
cd ..
cd ..
cd Entree/
cp etendard_? ~/Foret/Cabane/
```
## Mission 10 :

```sh
cp *_ornement ~/Foret/Cabane
```

## Mission 11 :

```sh
cd ..
cd Donjon/
cd Premier_etage/
mv tableau ~/Foret/Cabane/Coffre/
cp ~/Foret/Cabane/Coffre/tableau .
```
`.` : indique que je veux faire une copie dans le dossier courrant. 

## Mission 12 : 

Ici, la date etant aleatoire, je ne peux pas donner de correction. 
Il suffit de bien lire le `gash show`. 

## Mission 13 : 

```sh
alias la='ls -A'
```

## Mission 14 : 

```sh
alias journal='nano ~/Foret/Cabane/Coffre/journal.txt'
journal
```

`journal` devrait ouvrir nano, ici j'ai ajoute un peu de texte puis j'ai sauvegarde avec nano pour qu'un fichier soit crée ! 

## Mission 15 : 

**_ATTENTION_** : il est possible que le nom du couloir ne soit pas le meme ! (ne pas simplement copier coller l'instruction 
```sh
cd ~/Chateau/Cave/.Long d1f23a269117cdbff471f6a68edd6aca4419d937\ Couloir\ d0f81167efeb878d268a561644572f5431f476ce
```

## Mission 16 :
Rien a faire ! 
Pour quitter, entrez `exit`.


# BANDIT :      
   
Même si je donne les commandes, je ne donne pas les mots de passe :)     
Pour quitter une mission : `exit` 
    
## Commencer :    

- Se connecter avec `ssh` :    
  ```sh
  ssh bandit0@bandit.labs.overthewire.org -p 2220
  ```    
  `ssh` : secure shell !    
  `-p` : permet d'indiquer un port (ici 2220)    
  `bandit0@bandit.labs.overthewire.org` : `bandit0` est le nom d'utilisateur ! (qui devra changer pour passer aux autres missions).

  Appuyer sur `Entrer` pour accepter le `fingerprint`.
  Le mot de passe est inscrit sur le site !  

## Mission 0 :
  
```sh
cat readme 
```   
Copiez le mot de passe (`ctrl-shift-v` ou avec un clique-droit !).     
Quittez la mission (`exit`).    
Lancer la mission suivante :
```sh
ssh bandit1@bandit.labs.overthewire.org -p 2220
```

## Mission 1 : 

```sh
cat ./-
```

## Mission 2 : 

```sh
cat spaces\ in\ this\ filename
```

## Mission 3 :

```sh
cat inhere/.hidden 
```

## Mission 4 : 

Dans le dossier `inhere/` : 
```sh
file ./-file0*
```

Le mot de passe se trouve dans le fichier ASCII ! 

## Mission 5: 

```sh
find . -type f -size 1033c
```
`find` : commande qui permet de trouver des fichiers   
`.` : dossier de départ 
`-type f` : spécifie qu'on cherche des fichiers 
`-size 1033c` : spécifie la taille (1033 bytes/octets)

## Mission 6 :

```sh
find / -type f -size 33c -group bandit6 -user bandit7 2> /dev/null
```

`-group bandit6` : spécifie le groupe d'appartenance 
`-user bandit7` : spécifie l'utilisateur d'appartenance 
`2> /dev/null` : redirige les sorties d'erreurs vers `/dev/null`  

## Mission 7 : 

```sh
grep "millionth" data.txt
```
`grep` : commande qui permet de chercher des patrons dans des fichiers textes 
`"millionth"` : patron à chercher 
`data.txt` : fichier dans lequel chercher 

## Mission 8 :

```sh
cat data.txt | sort | uniq -u
```

`cat data.txt` : affiche le contenu de `data.txt` dans la sortie standard
`| sort` : permet d'ordonner les lignes par ordre alphabétique
`| uniq -u ` : affiche la ligne unique du fichier

## Mission 9 : 

```sh
strings data.txt | grep "====="
```

`strings data.txt` : affiche de façon lisible le contenu du fichier 
`| grep "====="` : cherche les lignes qui contiennent `"====="`

## Mission 10 : 

```sh
base64 -d data.txt
```

`base64 -d data.txt` : permet de décoder le contenu de `data.txt`
