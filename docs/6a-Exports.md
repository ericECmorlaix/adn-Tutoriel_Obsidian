# Exporter

## Partages

Les notes d'Obsidian sont de simples fichiers de texte brut avec l'extension `.md` qui sont stockés dans le dossier du coffre Obsidian sur votre appareil. On peut donc y accéder directement depuis l'explorateur ou l'application de gestion de fichiers et les partager de là vers d'autres destinations iCloud, OneDrive, ou les espaces de stockage physique d'autres appareils via AirDrop par exemple, ou encore par mails...

Si la note ne fait référence qu'à des liens absolus, il suffit de partager une copie du fichier `note.md`.
En revanche, si la note intègre des pièces jointes du coffre, le plus simple alors est de les rassembler dans un même sous-dossier du coffre puis de compresser son contenu dans une `archive.zip` avant de la partager.

Si la note ou le dossier à partager se trouve sur iCloud, il est alors possible de les partager en **mode collaboratif**....

## PDF & Cie

Obsidian peut nativement exporter en `note.pdf` un fichier Markdown `note.md`.

Depuis la palette de commande, saisir `pdf` puis choisir `Exporter en PDF`.
Dans la fenêtre qui s'ouvre, régler les paramètres puis cliquer sur le bouton `Exporter au format PDF`.
![[Exporter_en_PDF.png]]
Choisir le nom et l'emplacement pour enregistrer votre PDF et vérifier si le résultat convient...

>[!question]- Comment ajouter des sauts de page ?
>Pour ajouter des sauts de page, une solution consiste à insérer, à l'endroit où vous souhaitez changer de page dans votre sortie PDF, le bout de code HTML suivant  en laissant un saut de ligne avant et après.
>```html
>
><div style="page-break-after: always;"></div>
>
>```
>>Si vous pensez avoir besoin d'insérer ce bout de code régulièrement, c'est l'occasion de faire un [[7-Options_Plugins#Snippets|Snippet]]...

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

Pour réaliser une présentation plus évoluée avec beaucoup plus de fonctionnalités, il faut activer dans les paramètres d'Obsidian le modules complémentaire `obsidian-advanced-slides` (cf : [la documentation du plugin](https://mszturc.github.io/obsidian-advanced-slides/))

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

### iCloud

[Cf. documentation obsidian : iCloud](https://help.obsidian.md/Getting+started/Sync+your+notes+across+devices#iCloud+Drive)

Pour synchroniser un coffre d'Obsidian entre différents appareils à travers iCloud, il faut créer sur iPad un nouveau coffre en activant l'option  `Strore in iCloud`.

Les notes de ce coffre sont éditables hors connexion internet et les modifications seront automatiquement remontées vers iCloud Drive lorsque l'iPad sera connecté à nouveau.

### GitHub

Il est possible de synchroniser tout ou partie des données d'un coffre d'Obsidian entre différents appareils par l'intermédiaire de GitHub. 

#### Se connecter à GitHub

1. Créer un compte sur GitHub (Sign up) depuis un navigateur à l'adresse [https://github.com/](https://github.com/) ;

    <img class="center" src="https://ericecmorlaix.github.io/img/GitHub00a.png" width=55% alt="inscription GitHub">
 
Ou identifier vous (Sign in) si vous avez déjà un compte :

   <img class="center" src="https://ericecmorlaix.github.io/img/GitHub00b.png" width=45% alt="identification GitHub" >

#### Créer un nouveau dépôt GitHub

2. A l'adresse [https://github.com/new](https://github.com/new) **créer** un nouveau répertoire de dépôt privé nommé, par exemple `mon_carnet_Obsidian` et **ajouter** une description ;

   <img class="center" src="https://ericecmorlaix.github.io/img/GitHub01e.png" alt="nouveau repository GitHub">

3. Cocher la case **"Initialize this repository with a README"** puis cliquer sur le bouton **"Create repository"**.

   >[!success] Voilà, vous faites maintenant parti d'un autre [réseau social mondial celui des développeurs de code](https://medium.com/coding-days/focus-sur-github-le-r%C3%A9seau-social-des-d%C3%A9veloppeurs-165a2978ea9e)...

4. **Générer** une [clé d'identification sur GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)  pour paramétrer la synchronisation avec Obsidian sur votre iPad :
	- **Renseigner** les champs :
		- `Note` = préciser à quel usage est destinée votre clé pour l'identifier par la suite ;
		- `Expiration` = choisir `Custom` puis une date allant jusque la fin de l'année scolaire par exemple ;
		- `Select scope` = cocher `repo`, `admin:repo_hook`,  `gist` ;
	- **Cliquer** sur le bouton "==Generate token==" ;
	- **Copier** le code de votre clé pour pouvoir la réutiliser car elle ne sera plus visible ensuite...

#### Sur iPad
5. Dans Obsidian, **Ouvrir** ou **Créer** un coffre ;
  >[!note] Remarque :
  >*il peut être stocké sur iCloud ou juste en local sur votre iPad*.
1. **Créer** un nouveau dossier nommé `Mon_carnet` pour recevoir le contenu à synchroniser avec votre dépôt GitHub ;
  >[!note] Remarque :
  > *Cela permet que tous les dossiers et fichiers de votre coffre, y compris le dossier caché `.obsidian` ne se retrouvent pas inutilement copiés dans votre dépôt*.
1. **Installer** puis **Activer** le module complémentaire ["==Obsidian Git=="](https://github.com/denolehov/obsidian-git) ;
1. Depuis la palette de commande, **saisir** le mot `Init` puis **choisir** `Obsidian Git: Initialize a new repo` ;
1. Dans les options d'"==Obsidian Git==", **renseigner** les champs :
	- `Username on your git`  =  saisir votre pseudo GitHub ;
	- `Personal access token` = copier/coller la clé d'identification que vous venez de créer ;
	- `Author name for commit`  = saisir votre pseudo GitHub ;
	- `Author email for commit`  =  saisir votre email GitHub ;
	- `Custom base path` = `Mon_carnet` ;
1. Depuis la palette de commande, **saisir** le mot `Clone` puis **choisir** `Obsidian Git: Clone an existing remote repo` et suivre les instructions :
	- `Enter remote URL` = L'adresse de votre dépôt GitHub à cloner ;
	- `Enter directory for clone` = `Mon_carnet` ;
1. ==**Redémarrer** Obsidian ;==
1. **Editer** le fichier `README.md` qui sera la vitrine de votre dépôt GitHub.
  >[!note] Remarque :
  > *Il est préférable dans ce fichier, de se restreindre au [**MarkDown** à la sauce GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax), qui est différent de celui que vous utilisez pour rédiger vos `notes.md` dans Obsidian, notamment, il ne supporte pas les `[[liens internes]]`*.
1. **Glisser/déposer** toutes les notes de votre coffre que vous souhaitez synchroniser dans GitHub ainsi que leurs pièces jointes dans le dossier `Mon_carnet` ;
1. Depuis la palette de commande, **saisir** le mot `Source` puis **choisir** `Obsidian Git: Open source control view` ;
<img class="center" src="https://ericecmorlaix.github.io/adn-Tutoriel_Obsidian/assets/source_control_view.jpg" alt="source_control_view" width=60%>
1. Appuyer sur les `+` (1) en face des fichiers pour ajouter les modifications que vous voulez synchroniser à ce stade.
1. **Commiter** (2) puis **pousser** (3) les changements depuis Obsidian vers GitHub ;
1. **Vérifier** la mise à jour des vos fichiers sur GitHub...

#### Sur PC Windows

10. Installer si ce n'est pas déjà fait [git for windows](https://gitforwindows.org/)
<img class="center" src="https://github.com/gitobsidiantutorial/obsidian-git-tut-windows/raw/main/attachments/Pasted%20image%2020210325185111.png" alt="GitHub_Pages_Active" width=70%>
   > Assurez vous de permettre à Obsidian (3rd-party software) d'utiliser Git en ligne de commande...
1. Dans Obsidian, **Ouvrir** ou **Créer** un coffre ;
1. **Créer** un nouveau dossier nommé `Mon_carnet` pour recevoir le contenu à synchroniser avec votre dépôt GitHub ;
  >[!note] Remarque :
  > *Cela permet que tous les dossiers et fichiers de votre coffre, y compris le dossier caché `.obsidian` ne se retrouvent pas inutilement copiés dans votre dépôt*.
1. **Installer** puis **Activer** le module complémentaire ["==Obsidian Git=="](https://github.com/denolehov/obsidian-git) ;
1. Depuis la palette de commande, **saisir** le mot `Init` puis **choisir** `Obsidian Git: Initialize a new repo` ;
1. Dans les options d'"==Obsidian Git==", **renseigner** les champs :
	- *???* `Username on your git`  =  saisir votre pseudo GitHub ; *sauf si déjà défini globalement ???*
	- *???*`Personal access token` = copier/coller la clé d'identification que vous venez de créer ; *sauf si déjà défini globalement ???*
	- `Author name for commit`  = saisir votre pseudo GitHub ;
	- `Author email for commit`  =  saisir votre email GitHub ;
	- `Custom base path` = `Mon_carnet` ;
1. Depuis la palette de commande, **saisir** le mot `Clone` puis **choisir** `Obsidian Git: Clone an existing remote repo` et suivre les instructions :
	- `Enter remote URL` = L'adresse de votre dépôt GitHub à cloner ;
	- `Enter directory for clone` = `Mon_carnet` ;
1. ==**Redémarrer** Obsidian ;==
1. **Editer** le fichier `README.md` qui sera la vitrine de votre dépôt GitHub.
  >[!note] Remarque :
  > *Il est préférable dans ce fichier, de se restreindre au [**MarkDown** à la sauce GitHub](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax), qui est différent de celui que vous utilisez pour rédiger vos `notes.md` dans Obsidian, notamment, il ne supporte pas les `[[liens internes]]`*.
1. **Glisser/déposer** toutes les notes de votre coffre que vous souhaitez synchroniser dans GitHub ainsi que leurs pièces jointes dans le dossier `Mon_carnet` ;
1. Depuis la palette de commande, **saisir** le mot `Source` puis **choisir** `Obsidian Git: Open source control view` ;
<img class="center" src="https://ericecmorlaix.github.io/adn-Tutoriel_Obsidian/assets/source_control_view.jpg" alt="source_control_view" width=50%>
1. Appuyer sur les `+`  en face des fichiers (1) pour ajouter les modifications que vous voulez publier à ce stade.
1. **Commiter** (2) puis **pousser** (3) les changements depuis Obsidian vers GitHub ;
1. **Vérifier** la mise à jour des vos fichiers sur GitHub...
  
<!--
#### Créer un nouveau fichier

> [!note] Remarque
> L'objectif ici est de créer un fichier `.gitignore` pour exclure certains fichiers de la synchronisation avec GitHub notamment ceux de l'interface Obsidian qui resteront ainsi spécifiques à chaque machine...

4. **Cliquer** sur le bouton `Add file` depuis l'interface de votre dépôt GitHub et choisir `Create new files` :

5. Dans l'éditeur qui s'ouvre, **saisir** le nom du fichier `.gitignore` :
6. Dans la zone d'édition du fichier inscrire l'instruction `.obsidian/*`

> [!success] **Waouh !** vous venez de faire votre premier [**Commit**](https://fr.wikipedia.org/wiki/Commit) **!**  

<img  class="center" src="https://ericecmorlaix.github.io/img/GitHub05c.png" alt="créer dossier et fichier">
-->

---




