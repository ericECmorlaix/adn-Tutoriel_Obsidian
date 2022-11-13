# Multimédia

### Liens

#### Liens internes

Inscrire la syntaxe `[[nom_du_fichier]]` dans une note, permet de lier de façon bidirectionnelle celle-ci à un autre fichier du coffre.
C'est une spécificité d'Obsidian et des logiciels de son genre qui permet la navigation entre les notes et leurs pièces jointes contenues dans le dossier d'Obsidian.

>[!tip]+ Compléments
>- La syntaxe `[[nom_du_fichier|alias]]` utilise l'alias choisit à la place du nom du fichier comme texte de support du lien ;
>- La syntaxe `[[nom_du_fichier#un titre|alias]]` pointe vers un titre en particulier dans la note ;
>- La syntaxe `[[nom_du_fichier^|alias]]` pointe vers un bloc en particulier dans la note ;

Ces liens sont mis en évidence par la [[7-Options_Plugins#Vue graphique|Vue graphique]] et sont aussi utilisés dans les modules principaux [[7-Options_Plugins#Rétrolien|Rétrolien]] et [[7-Options_Plugins#Liens sortants|Liens sortants]].

>[!success]+ Autres avantages des liens bidirectionnels
> - Lorsque l'on modifie le nom du fichier dans le lien, Obsidian renomme automatiquement le fichier dans l'explorateur et inversement.
> - Si l'on déplace le fichier lié dans l'arborescence des dossiers du coffre, Obsidian met à jour automatiquement le chemin relatif du lien.

#### Liens externes

Le plus simple pour intégrer un lien hypertexte est de coller son adresse directement dans le MarkDown, par exemple le code `http://obsidian.md` produit http://obsidian.md ;
De cette façon on peut aussi indiquer une adresse mail,  par exemple le code `prenom.nom@ecmorlaix.fr` produit prenom.nom@ecmorlaix.fr.

La syntaxe `[texte](URL "info-bulle")` lie une adresse web à un texte support avec l'affichage optionnel d'une info-bulle au survol du lien,  par exemple le code `[Cf. documentation obsidian : Liens](https://help.obsidian.md/How+to/Format+your+notes#Links "Aide officielle sur les liens")` produit [Cf. documentation obsidian : Liens](https://help.obsidian.md/How+to/Format+your+notes#Links "Aide officielle sur les liens") ;

>[!question]- Comment alléger le code MarkDown de ses trop longues URL ?
> Parce que de longues adresses de liens dégradent la lisibilité du texte en mode édition de code, MarkDown permet de définir des liens par référence.
> Dans ce cas, on définit tous les liens à un endroit du document, en dehors du texte (généralement rassemblé), avec la syntaxe :
>```markdown
>[référence]: URL "infobulle"
>```
>et au fil du texte on lie cette adresse par sa référence à un texte support avec la syntaxe `[texte][référence]` ou encore tout simplement `[référence]`.
>Cette solution offre aussi l'avantage de pouvoir partager la même adresse par plusieurs liens en ne la définissant qu’une fois dans le document.
>> **Exemple** :
>>Le code MarkDown du paragraphe d'[[1a-MarkDown#Introduction|introduction]] comporte de nombreux liens de ce type, tous listés à la fin du texte...

>[!tip] Mettre l'URL entre deux chevrons `<URL>` si elle contient des espaces...

## Images

[Cf. documentation obsidian : Images](https://help.obsidian.md/How+to/Format+your+notes#Images "Aide officielle sur les images")

La syntaxe pour afficher des images dans une note est la même que celle pour les [[1b-MultiMedia#Liens|liens]],  mais avec un `!` devant.

### Images du web
Pour insérer l'affichage d'une image disponible sur le web on utilise le code MarkDown générique d'un lien externe, avec un `!` devant :
```md
![texte alternatif](adresse "infobulle")
```
- L'infobulle optionnelle s'affichera au survol de l'image.
- Il est important de bien choisir le [texte alternatif](http://www.pompage.net/traduction/Bien-utiliser-le-texte-alternatif) qui s'affichera lorsque l'image n'est pas disponible, car il permet aussi l'accessibilité pour les non-voyants et apporte de la sémantique pour les moteurs de recherche...
- L'adresse est l'URL absolue qui permet d'atteindre le fichier lié sur le web.

>[!example] Exemple
>Le code MarkDown `![Image SVG logo du site https://compresspng.com](https://compresspng.com/images/compresspng/logo.svg "Compresser vos images avec la force d'un éléphant !")`, affiche :
>![Image SVG logo du site https://compresspng.com](https://compresspng.com/images/compresspng/logo.svg "Compresser vos images avec la force d'un éléphant !")

### Images du coffre
Pour insérer l'affichage d'une image disponible dans le coffre d'Obsidian, on utilise le code MarkDown spécifique d'un lien interne, avec un `!` devant :
```md
![[nom_fichier_image]]
```

A venir...

>[!info]- En ligne ou en bloc

> taille des images

> Image support de lien

> Alignement
> https://github.com/SlRvb/Obsidian--ITS-Theme#image-positions

> format d'images

>[!question]- Quel format d'image pour le web ?
>- **JPEG**  (**J**oint **P**hotographic **E**xpert **G**roup)
> Parfait pour les photos et visuels colorés, c’est le format compressé le plus utilisé sur le web.
> - **PNG** (**P**ortable **N**etwork **G**raphics)
>  Idéal pour les images à fond transparent, graphique et logo.
>  - **SVG** (**G**raphics **I**nterchange **F**ormat)
>    Format adapté aux images vectorielles, permet de les déformer sans altérer la qualité.
>  - **GIF** (**G**raphics **I**nterchange **F**ormat)
>   Images animées idéale pour illustrer vos propos, fortement utilisé sur les réseaux sociaux.

>[!tip]+ Réduire le poids des images
>D'une manière générale, il est important pour accélérer le processus d'affichage et limiter l'impact environnementale produit par nos documents (transfert, stockage) de réduire la taille des fichiers intégrées et particulièrement celle des images.
> On gagne toujours en choisissant bien le format adaptés à l'utilisation finale du document :
> - une image vectorielle (.svg) offre généralement plus de qualité qu'une image matricielle pour du dessin ;
> - une image matricielle (`.png` dessin,  `.jpeg` photo, `.gif` animation) destinée à l'affichage n'a pas besoin d'autant de définition que pour une impression.
> 
> De plus on peut très avantageusement les compresser :
> 
> 12,3ko en `.svg` [![[compress_png.svg]]](https://compresspng.com/fr/)   à comparer en zoomant avec
> 14,0ko en `.png` [![[compress_png.png]]](https://compresspng.com/fr/) .
> 
> Cette dernière après une compression réglée sur 3 couleurs, réduit son poids de 85% ce qui donne seulement 2,1ko en `.png` qui suffisent ici à faire le job : [![[compress_png-min.png]]](https://compresspng.com/fr/) [![[compress_jpeg-min.png]]](https://compressjpeg.com/fr/) [![[compress_gif-min.png]]](https://compressgif.com/fr/)
> Après avoir Glisser/Déposer le fichier original, en cliquant sur la vignette du fichier réduit proposé au téléchargement, on accède à des réglages supplémentaires qui permettent d'accentuer encore la compression obtenue par défaut. Le volet horizontal montre alors la différence obtenu à l'affichage... il y a forcément des pertes, mais ==tant que l'information à transmettre reste visible et correcte, le jeu en vaut la chandelle car l'économie peut être très significative==...
> 

A venir...

## [Tableau](https://help.obsidian.md/How+to/Format+your+notes#Tables)


## [LaTeX](https://help.obsidian.md/How+to/Format+your+notes#Math)


## [Diagrammes](https://help.obsidian.md/How+to/Format+your+notes#Diagram)


## [Intégrations](https://help.obsidian.md/How+to/Embed+files)




### Notes

![[test]]
--8<-- "Inclus/test.md"

### Audio


### Vidéos


### iFrame

[iFrame](https://help.obsidian.md/How+to/Embed+files#iframe)


### Pdf


## En résumé

Inspiré du [guide obsidian de Johackim](https://johackim.com/obsidian#syntaxe-markdown)

### Syntaxe Markdown

Obsidian utilise la syntaxe Markdown par défaut :

-   `[Link Text](URL "infobulle")` : Créer un lien avec URL + infobulle
-   `![Alt Text](URL "infobulle")` : Créer une image + infobulle
-   `[ref1]` et `[ref1]: <url> "infobulle"` : Créer une référence + infobulle
-   `[Link Text][ref1]` et `[ref1]: <url> "infobulle"` : Créer une référence avec un texte personnalisé + infobulle

### Syntaxe d'Obsidian

Mais il a quelques spécificités de syntaxes supplémentaires :

-   `[[Linking Note]]` : Créer un lien vers une autre note
-   `[[Linking Note|Link Name]]` : Créer un lien avec un nom personnalisé
-   `[[Linking Note#heading]]` : Créer un lien vers un titre d'une note
-   `![[Linking Note^]]` : Intégrer un bloc d'une note
-   `![[Filename]]` : Intégrer une autre note
-   `![250](https://johackim.com/soon?title=250 "Note bientôt disponible")` : Insérer une image embed de 250px de largeur
    
-   `![|250](https://site.xyz/image.png)` : Insérer une image de 250px de largeur

-   `#tag` : Créer un tag
-   `#nested/tag` : Créer un sous-tag

-   `aliases: [Alias1, Alias2]` : Créer un alias (à ajouter dans le frontmatter)








