# sol-gash-labo-3

## Description :
 - Ma correction pour le jeu GameShell du labo3 du cours INF1070. 
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

`journal` devrait ouvrir nano, ici j'ai ajoute un peu de texte puis j'ai sauvegarde avec nano pour qu'un fichier soit cree ! 

## Mission 15 : 

_ATTENTION_ : il est possible que le nom du couloir ne soit pas le meme ! (ne pas simplement copier coller l'instruction 
```sh
cd ~/Chateau/Cave/.Long d1f23a269117cdbff471f6a68edd6aca4419d937 Couloir d0f81167efeb878d268a561644572f5431f476ce
```

## Mission 16 :
Rien a faire ! 
