# Traitement de données

A venir...

## Liens Internes et Tags

>[!question] Qui entre Jon Favreau et Joss Whedon a réalisé le plus de films Marvel ? Qui entre Chris Evans, Robert Downey Jr., Chris Hemsworth, Scarlett Johansson et Mark Ruffalo a joué le plus dans des films Marvel ?
>Pour y répondre, faire l'activité présenté à la fin de l'article [Obsidian, bien plus qu’une prise de notes…](https://labonnedonne.fr/post/644122684651945984/obsidian-bien-plus-quune-prise-de-notes)



## Les métadonnées

Les métadonnées sont des informations complémentaires aux données contenues dans le corps d'un fichier `note.md` qui peuvent servir pour faire des recherches dans votre coffre par la suite.

Elles peuvent être définies en YAML dans l'entête, le "front matter" du fichier.
Le code à écrire alors au tout début du document est de la forme :

```YAML
---
# Clés personnalisées et leur valeur associée
cle1 : valeur
cle2 : [valeur1, valeur2, valeur3] # Pour déclarer une liste de valeurs
cle3 : # Autre solution pour déclarer une liste de valeurs
	- valeur1
	- valeur2
	- valeur3
# Clés définient nativement dans Obsidian
tags : valeur # liste de tags référencés dans le document
aliases : valeur # liste de noms alternatifs pour le document
cssclass :
publish : 
---
```
Les informations contenues dans ce bloc ne seront pas visible en mode affichage.

Il est également possible de déclarer dans le corps du document des métadonnées qui resteront visibles en mode affichage de la sorte :
```
tag:: valeur 
```


## Dataview

Il vous permet de gérer vos données (le contenu de vos fichiers Markdown et leurs métadonnées) comme une base de données.

Mises en bouche en attendant :

[nicolas.loeuillet.org/billets/2021/03/02/obsidian-mon-nouvel-outil-de-prise-de-notes/](https://nicolas.loeuillet.org/billets/2021/03/02/obsidian-mon-nouvel-outil-de-prise-de-notes/)

>[!quote]- [Nicole van der Hoeven](https://www.youtube.com/c/NicolevanderHoeven)
><center><figure><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/vS-b_RUtL1A" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure></center>
><center><figure><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/JTObSymEvWA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure></center>
>