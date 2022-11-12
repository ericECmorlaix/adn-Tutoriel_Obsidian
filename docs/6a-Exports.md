# Exporter

A venir...

## Pdf & Cie


---
## Diaporama

Obsidian permet de réaliser très rapidement un diaporama à partir d'un simple fichier MarkDown `note.md`. 

>[!note] Pour les diaporamas, Obsidian s'appuie sur le Framework de présentation HTML open source [`reveal.js`](https://revealjs.com/) qui peut être utilisé indépendamment par ailleurs...

### [Diaporama basique](https://help.obsidian.md/Plugins/Slides)

Pour réaliser une présentation très simple, il faut activer dans les paramètres d'Obsidian le plugin principal `Diapositives`et faire des traits horizontaux avec trois `---` pour séparer les diapositives. Il suffit alors depuis la palette de commande de saisir le mot `Diapo` puis de  choisir `Diapositives: Démarrer la présentation` ;

>[!example]- Exemple de code MarkDown pour tester
>```markdown
># Présentation Slides
>Une petite démonstration  
>pour tester le module  
>**Diapositives.**
>
>---
>## Formatage du texte
>
>On utilise la syntaxe MarkDown  
>pour formater le texte :
>- **gras**
>-  *italique*
>- ==surligné==
>- ~~barré~~
>
>---
>
>> [!warning] On peut mettre des avertissements
>>>[!example] Exemple :
>>>>[!tip] Truc à savoir :
>>>>*On peut définir une touche du clavier pour lancer la présentation ==ou un bouton sur mobile==...*
>
>---
>## Diapositives
>
>1. On met `---` entre deux diapositives ;  
>2) Et, **c'est tout !**
>>[!success] Suffisant pour un :
>>![[PechaKucha-min.jpg|200]] [Pecha Kucha](https://fr.wikipedia.org/wiki/Pecha_Kucha) 
>```

>[!failure] Obsidian n'offre pas de possibilité d'export de ses diaporamas basiques vers d'autre format.

>[!tip]+ Sur iPad, il suffit de capturer ou d'enregistrer l'écran lors d'une présentation...
>On peut ainsi produire une vidéo avec ou sans commentaire sonore.
>Puis utiliser un [[2-Imports#Raccourcis|Raccourcis de partage]] pour la convertir, l'ajouter au coffre et l'intégrer dans une note du jour.
>Ou encore la déposer sur [PeerTube](https://apps.education.fr/applications/peertube/) pour l'intégrer en [[1b-MultiMedia#iFrame|`<iframe>`]] tel que ci-dessous :
><center><figure><iframe title="Capture_Diaporama_Basique" width="560" height="410" src="https://tube-sciences-technologies.apps.education.fr/videos/embed/7be3d217-aff3-49f7-b3d5-51f8b7a28306?loop=1&amp;autoplay=1" frameborder="0" allowfullscreen="" sandbox="allow-same-origin allow-scripts allow-popups"></iframe></figure></center>
>
>Une autre solution plus éconologique en terme de poids du fichier, consiste à [[2-Imports#Raccourcis|produire un GIF à partir des captures d'écran des diapositives]] que l'on peut alors éventuellement annoter avant d'intégrer le fichier `image.gif`résultant comme ci-dessous :
>
><center><img class="center" src="https://ericecmorlaix.github.io/adn-Tutoriel_Obsidian/assets/Capture_Diaporama_Basique_GIF.gif" width=60% alt="Capture_Diaporama_Basique_GIF"></center>

>[!quote]- [João - Le MindMappeur](https://www.youtube.com/c/LeMindMappeur)
><center><figure><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/25mDwXZgwTM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></iframe></figure></center>

### [Diaporama avancé](https://mszturc.github.io/obsidian-advanced-slides/)

Pour réaliser une présentation plus évoluée avec beaucoup plus de fonctionnalités, il faut activer dans les paramètres d'Obsidian le modules complémentaire `obsidian-advanced-slides` (cf : [la documentation du plugin]())

>[!example]- Exemple de code MarkDown pour tester
>````markdown
># Présentation Slides
>Une petite démonstration  
>pour tester le module  
>**Advanced Slides.**
>
>---
>## Formatage du texte
>
>On utilise la syntaxe MarkDown  
>pour formater le texte :
>- **gras**
>+ *italique*
>+ ==surligné==
>+ ~~barré~~
>
>>[!warning] On peut mettre des [avertissements](https://mszturc.github.io/obsidian-advanced-slides/basic-syntax/callouts/)
>> + inclinés,
>> + mais pas imbriqués ;
><!-- element style="width:60%;font-size:24px" rotate="-5"-->
>
>---
>## Diapositives
>
>1. Il suffit de mettre `---` entre deux diapositives horizontales ;  
>2) Et  `--` entre deux diapositives verticales. 
>
>--
>## Fragments
>
>Les fragments précédents  
>sont obtenus avec les codes :
>
>```markdown
>- **gras**
>+ *italique*
>+ ==surligné==
>+ ~~barré~~
>```
>
>et 
>```markdown
>1. Il suffit de mettre `---` entre deux diapositives horizontales ;
>2} Et  `--` entre deux diapositives verticales. 
>```
>````

On peut alors exporter la présentation au format pdf mais aussi en HTML ce qui permet de l'intégrer comme ci-dessous ou de coller un [lien vers l'exemple de diaporama avancé en HTML](../assets/test-diaporama-avance/index.html)

<center><iframe width="800" height="480" src="../assets/test-diaporama-avance/#"></iframe></center>

>[!quote]- [Nicole van der Hoeven](https://www.youtube.com/c/NicolevanderHoeven)
><center><figure><iframe width="560" height="315" src="https://www.youtube-nocookie.com/embed/LtBK_iNcVEQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe></figure></center>
><center><iframe width="800" height="460" src="https://slides.nicolevanderhoeven.com/2022-use-it-or-lose-it/#/"></iframe></center>
---
## Synchroniser

Obsidian propose une solution payante, [Obsidian Sync](https://help.obsidian.md/Obsidian+Sync/Introduction+to+Obsidian+Sync) pour synchroniser les données d'un coffre entre différents appareils. Cependant, il est aussi possible de le faire différemment... 

### [iCloud](https://help.obsidian.md/Getting+started/Sync+your+notes+across+devices#iCloud+Drive)



### GitHub

Il est possible de synchroniser tout ou partie des données d'un coffre d'Obsidian entre différents appareils par l'intermédiaire de GitHub. 

#### Créer un dépôt GitHub

1. Créer un compte sur GitHub (Sign up) depuis un navigateur à l'adresse [https://github.com/](https://github.com/) ;

    <img class="center" src="https://ericecmorlaix.github.io/img/GitHub00a.png" width=55% alt="inscription GitHub">
 
Ou identifier vous (Sign in) si vous avez déjà un compte :

   <img class="center" src="https://ericecmorlaix.github.io/img/GitHub00b.png" width=45% alt="identification GitHub" >


---

### Air Drop

---


