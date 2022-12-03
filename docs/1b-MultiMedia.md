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
- L'adresse est l'URL absolue qui permet d'atteindre le fichier lié sur le web, ou le chemin relatif vers un fichier

>[!example]+ Exemple
>Le code MarkDown `![Logo du site https://compresspng.com](https://compresspng.com/images/compresspng/logo.svg "Compresser vos images avec la force d'un éléphant !")`, affiche :
>
>![Logo du site https://compresspng.com](https://compresspng.com/images/compresspng/logo.svg "Compresser vos images avec la force d'un éléphant !")

>[!note]- Cette syntaxe fonctionne aussi avec une image du coffre...
>Le code MarkDown `![Logo du site https://compresspng.com](assets/compress_png.svg "Compresser vos images avec la force d'un éléphant !")`, affiche la même chose :
>
>![Logo du site https://compresspng.com](assets/compress_png.svg "Compresser vos images avec la force d'un éléphant !")
>> **Remarque** :
>> La mise à jour automatique du lien relatif peut poser problème en cas de changement de dossier...

### Images du coffre
Pour insérer l'affichage d'une image disponible dans le coffre d'Obsidian, il peut-être plus pratique d'utiliser le code MarkDown spécifique d'un lien interne, avec un `!` devant :
```md
![[nom_fichier_image]]
```
> Le plus simple pour obtenir ce code est alors de glisser/déposer un fichier image depuis l'explorateur dans le code MarkDown d'une note là ou l'on souhaite insérer l'image

>[!example] Exemple
>Le code MarkDown `![[compress_png.svg]]`, affiche :
>
>![[compress_png.svg]]


A venir...

>[!info]- En ligne ou en bloc

> taille des images

> Image support de lien

> Alignement
> https://github.com/SlRvb/Obsidian--ITS-Theme#image-positions

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


## $\LaTeX{}$

[Cf. documentation obsidian : Math](https://help.obsidian.md/How+to/Format+your+notes#Math)

[$\LaTeX$](https://fr.wikipedia.org/wiki/LaTeX), qu'on prononce "LaTèque", est un langage de description à balisage dédié à l'édition et la publication de rapports scientifiques avec une typographie irréprochable.  

Dans une `note.md` d'Obsidian, il est possible d'intégrer des instructions codées en $\LaTeX$ qui seront interprétées par la librairie JavaScript [Mathjax](https://www.mathjax.org/) embarquée pour afficher des équations et autres symboles scientifiques.


### Principe

Pour une formule en ligne, au fil du texte, telle que $f(x) = x^2$, il faut encadrer l'expression entre deux simples `$...$` comme ceci `$f(x) = x^2$`.

Pour une formule en bloc, dans un nouveau paragraphe centré, il faut encadrer l'expression entre deux doubles `$$...$$` comme cela :

```latex
$$
F(x) = \int^a_b \frac{1}{2}x^4
$$
```

ce qui produit :

$$
F(x) = \int^a_b \frac{1}{2}x^4
$$

### Exemples

|             Code             |          Résultat          |                Code                 |    Résultat    |
|:----------------------------:|:--------------------------:|:-----------------------------------:|:--------------:|
|          `$x + y$`           |          $x + y$           |              `$x - y$`              |    $x - y$     |
|        `$x \times y$`        |        $x \times y$        |            `$x \div y$`             |   $x \div y$   |
|           `$x^2$`            |           $x^2$            |            `$y^{(x-1)}$`            |  $y^{(x-1)}$   |
|   `$\pi \approx 3.14159$`    |   $\pi \approx 3.14159$    |            `$1 \neq 2$ `            |   $1 \neq 2$   |
|          `$0 < 1$`           |          $0 < 1$           |              `$2 > 1$`              |    $2 > 1$     |
|         `$x \leq 2$`         |         $x \leq 2$         |            `$x \geq 1$`             |   $x \geq 1$   |
|       `${3 \over 4}$`        |       ${3 \over 4}$        |          `$\dfrac{1}{2x}$`           | $\dfrac{1}{2x}$ |
| `$U_n = 3 \times U_{n-1}+2$` | $U_n = 3 \times U_{n-1}+2$ | `$f(x) = \sqrt[3]{2x} + \sqrt{x-2}$` | $f(x) = \sqrt[3]{2x} + \sqrt{x-2}$               |

|        | Code                                                           | Résultat                                                     |
| ------ | -------------------------------------------------------------- | ------------------------------------------------------------ |
| Boole  | `$a\oplus b=\bar{a}\cdot b+a\cdot\bar{b}$`                     | $a\oplus b=\bar{a}\cdot b+a\cdot\bar{b}$                     |
| Force  | $\overrightarrow{F_{(ext \to S)}}$                             | $\overrightarrow{F_{(ext \to S)}}$                           |
| Moment | `$\sum\overrightarrow{M_G(\overrightarrow{F_{(ext \to S)}})}$` | $\sum\overrightarrow{\mathscr M_G(\overrightarrow{F_{(ext \to S)}})}$ |
| Unité  | `$49,52\;\mathrm{N\!\cdot\!m}$`                                         | $\|\overrightarrow{C_\text{moteur}}\|=49,52\;\mathrm{N\!\cdot\!m}$                                                             |

| Nom     |     Code     |   Lettre   |     Code     |   Lettre   |      Code       | Lettre |
| ------- |:------------:|:----------:|:------------:|:----------:|:---------------:|:---:|
| alpha   |  `$\alpha$`  |  $\alpha$  |    `$A$`     |    $A$     |                 |     |
| beta    |  `$\beta$`   |  $\beta$   |    `$B$`     |    $B$     |                 |     |
| gamma   |  `$\gamma$`  |  $\gamma$  |  `$\Gamma$`  |  $\Gamma$  |                 |     |
| delta   |  `$\delta$`  |  $\delta$  |  `$\Delta$`  |  $\Delta$  |                 |     |
| epsilon | `$\epsilon$` | $\epsilon$ |    `$E$`     |    $E$     | `$\varepsilon$` |  $\varepsilon$   |
| zeta    |  `$\zeta$`   |  $\zeta$   |    `$Z$`     |    $Z$     |                 |     |
| eta     |   `$\eta$`   |   $\eta$   |    `$H$`     |    $H$     |                 |     |
| theta   |  `$\theta$`  |  $\theta$  |  `$\Theta$`  |  $\Theta$  |  `$\vartheta$`  |   $\vartheta$  |
| iota    |  `$\iota$`   |  $\iota$   |    `$I$`     |    $I$     |                 |     |
| kappa   |  `$\kappa$`  |  $\kappa$  |    `$K$`     |    $K$     |  `$\varkappa$`  |  $\varkappa$   |
| lambda  | `$\lambda$`  | $\lambda$  | `$\Lambda$`  | $\Lambda$  |                 |     |
| mu      |   `$\mu$`    |   $\mu$    |    `$M$`     |    $M$     |                 |     |
| nu      |   `$\nu$`    |   $\nu$    |    `$N$`     |    $N$     |                 |     |
| xi      |   `$\xi$`    |   $\xi$    |    `$Xi$`    |    $Xi$    |                 |     |
| omicron | `$\omicron$` | $\omicron$ |    `$O$`     |    $O$     |                 |     |
| pi      |   `$\pi$`    |   $\pi$    |   `$\Pi$`    |   $\Pi$    |   `$\varpi$`    | $\varpi$    |
| rho     |   `$\rho$`   |   $\rho$   |    `$P$`     |    $P$     |   `$\varrho$`   |  $\varrho$   |
| sigma   |  `$\sigma$`  |  $\sigma$  |  `$\Sigma$`  |  $\Sigma$  |  `$\varsigma$`  |   $\varsigma$  |
| tau     |   `$\tau$`   |   $\tau$   |    `$T$ `    |    $T$     |                 |     |
| upsilon | `$\upsilon$` | $\upsilon$ | `$\Upsilon$` | $\Upsilon$ |                 |     |
| phi     |   `$\phi$`   |   $\phi$   |   `$\Phi$`   |   $\Phi$   |   `$\varphi$`   |   $\varphi$  |
| chi     |   `$\chi$`   |   $\chi$   |    `$X$ `    |    $X$     |                 |     |
| psi     |   `$\psi$`   |   $\psi$   |   `$\Psi$`   |   $\Psi$   |                 |     |
| omega   |  `$\omega$`  |  $\omega$  |  `$\Omega$`  |  $\Omega$  |                 |     |

### Ressources
- La très précieuse et précise [Aide pour écrire des mathématiques simples](https://ens-fr.gitlab.io/mkdocs/maths/) par Franck CHAMBON  
- [Equation Sheet](http://www.equationsheet.com/)
- [Editeur d'équation en ligne](http://www.codecogs.com/eqnedit.php?latex=)
- L'ultime ressource : [LaTeX Wiki](http://en.wikibooks.org/wiki/LaTeX/Mathematics)
- Pour s'initier au vrai $\LaTeX$ :[Apprentissage LaTeX en ligne avec ShareLaTeX](http://tsi.si.lycee.ecmorlaix.fr/APprentissageLaTeX/)
- Sur le site de Didier MULLER https://www.apprendre-en-ligne.net/LaTeX/index.html :
  - [Introduction à LaTex, par Fabien Augsburger (pdf, 17 pages)](https://www.apprendre-en-ligne.net/LaTeX/IntroLaTeX.pdf) ;
  - [Apprends LaTeX, par Marc Baudoin (pdf, 112 pages)](https://www.apprendre-en-ligne.net/LaTeX/apprends-latex.pdf) ;
  - [Tout ce que vous avez toujours voulu savoir sur LATEX sans jamais oser le demander (pdf, 338 pages)](https://www.apprendre-en-ligne.net/LaTeX/framabook5_latex.pdf)
  - [LaTeX pour l'impatient, 4ème édition, Céline Chevalier, H&K, 2016](https://www.amazon.fr/LaTeX-pour-limpatient-Spiral-Bound/dp/235141327X/ref=as_li_ss_tl?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&keywords=latex%2Bpour%2Bl%27impatient&qid=1558529880&s=gateway&sr=8-1-fkmrnull&linkCode=ll1&tag=coyote-21&linkId=210710a1380df1e7df1910e0bc63f40a&language=fr_FR)


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








