# Publier

Cette partie présente une démarche qui vous permettra de publier sur le Web depuis un dépôt GitHub tout ou partie des notes contenues dans votre coffre Obsidian via MkDocs avec le thème Material.

## Mise en place
### Coté GitHub

#### Créer un dépot GitHub

1. Créer un compte sur GitHub (Sign up) depuis un navigateur à l'adresse [https://github.com/](https://github.com/) ;

    <img class="center" src="https://ericecmorlaix.github.io/img/GitHub00a.png" width=55% alt="inscription GitHub">
 
Ou identifier vous (Sign in) si vous avez déjà un compte :

   <img class="center" src="https://ericecmorlaix.github.io/img/GitHub00b.png" width=45% alt="identification GitHub" >

2. **Créer** un nouveau dépôt GitHub à partir du modèle [simple_template_obsidian_mkdocs](https://github.com/ericECmorlaix/simple_template_obsidian_mkdocs)  en cliquant sur le bouton "==Use this template==" ou tout simplement en cliquant sur [ce lien](https://github.com/ericECmorlaix/simple_template_obsidian_mkdocs/generate) ;

![[Use_this_template.png]]

3. **Donner** un nom à votre dépôt public sachant que par défaut vos notes seront publiées à une adresse au format <https://votre-pseudo-github.github.io/nom-depot/> :
	- **ajouter** une description ;
	-  **ne copier que** la branche `main` du dépôt template ;
	- enfin cliquer sur le bouton "==Create repository from template==".
 
 >[!success] Voilà, vous faites maintenant parti d'un autre [réseau social mondial celui des développeurs de code](https://medium.com/coding-days/focus-sur-github-le-r%C3%A9seau-social-des-d%C3%A9veloppeurs-165a2978ea9e)...  

#### Modifier le fichier `README.md`  

> Le fichier `README` est la vitrine de votre dépôt GitHub, il a pour extension `.md` pour [**MarkDown**](https://fr.wikipedia.org/wiki/Markdown), qui, à quelques spécificités près, est le même que celui que vous utilisez pour rédiger vos `notes.md` dans Obsidian qui seront bientôt aussi vos futures pages web. 
 
4. **Cliquer** sur le crayon pour ouvrir le fichier `README.md`dans l'éditeur en ligne :
 <img class="center" src="https://ericecmorlaix.github.io/img/GitHub02bis.png" alt="editer README" width=75%>
  
5. **Modifier** son contenu en utilisant la syntaxe [MarkDown à la sauce GitHub](https://guides.github.com/features/mastering-markdown/) :
<img class="center" src="https://ericecmorlaix.github.io/img/GitHub03bis.png" alt="modifier README" width=75%>

> l'onglet `Preview` permet de visualiser le résultat avant sa publication...

6. **Publier** la nouvelle version du fichier `README.md` en décrivant vos modifications dans un message et puis en cliquant sur le bouton `Commit changes` :
<img class="center" src="https://ericecmorlaix.github.io/img/GitHub04bis.png" alt="publier README" width=75%>

> [!success] **Waouh !** vous venez de faire votre premier [**Commit**](https://fr.wikipedia.org/wiki/Commit) **!**

> [!note] Remarque
> Nous allons bientôt voir que nous aurions tout aussi bien pu éditer ce fichier `README.md` dans Obsidian mais, cependant, cela se limitera aux fichiers ayant l'extension `.md`.
> Il est donc intéressant de savoir faire cela directement dans GitHub pour éditer depuis n'importe quel navigateur les fichiers MarkDown mais aussi d'autres...

#### Déployer votre site

> [!success] Au bout d'un moment, si tout se passe bien, le "bot" de GitHub devrait générer à partir de votre branche `main`, une seconde branche nommée `gh-pages` :
><img class="center" src="https://ericecmorlaix.github.io/img/GitHub07bis.png" alt="branche" width=40%>

7. **Cliquer** sur les onglets `Settings` (1) puis `Pages` (2), **sélectionner** la branche `gh-pages` (3) enfin **cliquer** sur le bouton `Save` (4) :
 <img class="center" src="https://ericecmorlaix.github.io/img/GitHub08bis.png" alt="Déploiement" width=90%>

> [!success]  Au bout d'un moment, si tout se passe bien, votre site devrait être visible sur le web à une adresse au format <https://votre-pseudo-github.github.io/nom-depot/>...

#### Configurer de votre site

Les fichiers de configuration du site `mkdocs.yml` et `ci.yml` sont écrits en [YAML](https://fr.wikipedia.org/wiki/YAML), un langage avec une syntaxe la plus lisible possible par des humains pour représenter des données.

Obsidian ne permet pas d'éditer ces fichiers. Il vous faudra les ouvrir dans votre éditeur de texte favori ou directement les éditer dans GitHub pour les modifier afin de les personnaliser :

- Sauf à vouloir ajouter de nouvelles fonctionnalités, le fichier [`CI.yml`](https://ericecmorlaix.github.io/adn-Tutoriel_site_web/Yaml/#le-fichier-ciyml) peut rester inchangé ;
- En revanche, il sera nécessaire de modifier le fichier `mkdocs.yml` en s'aidant des explications laissées en commentaires ou encore de celles ce [tutoriel de configuration d'un site web avec MkDocs](https://ericecmorlaix.github.io/adn-Tutoriel_site_web/Yaml/#le-fichier-mkdocsyml)

#### Personnaliser les pages de votre site

Le texte en MarkDown de la page `index.md` du dossier `/docs` devient la page d'accueil en HTML de votre site.

Les dossiers présents dans `/docs` apparaissent comme sections principales de la barre de navigation. De même pour le titre de niveau 1 `# Accueil` écrit au début du fichier `index.md`.

Chaque note, `fichier.md` écrit en MarkDown, devient une nouvelle page du site dans leur section respective. Le noms de ces fichiers sont visible dans la barre d'URL. Les titres et sous-titres de la table des matières apparaissent dans des sous-sections d'un menu secondaire.

> En l'absence de titre de niveau 1 au début d'une note, c'est le nom du fichier qui apparaitra en tête de la sous-section.

Il est donc préférable d'attribuer aux dossiers et fichiers des noms significatifs, sans caractère accentué ni espace et, de même que pour les titres et sous-titres, le mieux est de les choisir courts. 

> Ce nommage automatique peut-être modifié en définissant manuellement la rubrique `nav` dans le fichier `mkdocs.yml`, ce qui devient cependant vite fastidieux...

> [!note] Toutes ces fichiers en MarkDown, futures page de votre site, sont éditables soit directement dans GitHub ou soit dans Obsidian...

8. **Générer** une [clé d'identification sur GitHub](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)  pour paramétrer la synchronisation avec Obsidian sur votre iPad :
	- **Renseigner** les champs :
		- `Note` = préciser à quel usage est destinée votre clé pour l'identifier par la suite ;
		- `Expiration` = choisir `Custom` puis une date allant jusque la fin de l'année scolaire par exemple ;
		- `Select scope` = cocher `repo`, `admin:repo_hook`,  `gist` ;
	- **Cliquer** sur le bouton "==Generate token==" ;
	- **Copier** le code de votre clé pour pouvoir la réutiliser car elle ne sera plus visible ensuite...


### Coté Obsidian
9. Dans Obsidian, **Ouvrir** ou **Créer** un coffre ;
1. **Créer** un nouveau dossier nommé `Site` pour recevoir le contenu cloné de votre dépôt GitHub ;
1. **Installer** puis **Activer** le module complémentaire ["==Obsidian Git=="](https://github.com/denolehov/obsidian-git) ;
1. Depuis la palette de commande, **saisir** le mot `Init` puis **choisir** `Obsidian Git: Initialize a new repo` ;
1. Dans les options d'"==Obsidian Git==", **renseigner** les champs :
	- `Username on your git`  =  saisir votre pseudo GitHub ;
	- `Personal access token` = copier/coller la clé d'identification que vous venez de créer ;
	- `Author name for commit`  = saisir votre pseudo GitHub ;
	- `Author email for commit`  =  saisir votre email GitHub ;
	- `Custom base path` = `Site` par exemple,  si vous ne souhaitez pas que tous les dossiers et fichiers de votre dépôt se retrouvent à la racine de votre coffre ;
1. Depuis la palette de commande, **saisir** le mot `Clone` puis **choisir** `Obsidian Git: Clone an existing remote repo` et suivre les instructions :
	- `Enter remote URL` = L'adresse de votre dépôt GitHub à cloner ;
	- `Enter directory for clone` = `Site` ;
1. **Editer** le fichier MarkDown `index.md` du dossier `/docs` pour qu'il produise la page d'accueil en HTML que vous souhaitez pour votre site.
1. **Glisser/déposer** toutes les notes que vous souhaitez publier et leurs pièces jointes dans le dossier `docs` ;
1. Depuis la palette de commande, **saisir** le mot `Source` puis **choisir** `Obsidian Git: Open source control view` ;
1. Appuyer sur les + pour mettre sur l'étagère d'expédition les modification que vous voulez publier.
1. **Commiter** puis **pousser** les changements avec Obsidian Git ;

<!--
3. GitHub Action va alors prendre en charge automatiquement la conversion de vos fichiers MarkDown d'Obsidian vers [MkDocs](https://www.mkdocs.org/) avec le thème [Material](https://squidfunk.github.io/mkdocs-material/) pour générer les fichiers au format HTML de votre site Web dans une branche `gh-page` ;
7. Depuis la page de votre dépôt sur GitHub, **Cliquer** sur les onglets `Settings` (1) puis `Pages` (2), **sélectionner** la branche `gh-pages` (3) enfin **cliquer** sur le bouton `Save` (4) :
![](gh-pages.png)
> Au bout d'un moment, si tout se passe bien, votre site devrait être visible sur le web à l'adresse <https://votre-pseudo-github.github.io/nom-depot/>



1. **Cloner** le dépôt que vous venez de générer dans votre dossier/coffre d'Obsidian.  Soit avec le plugin Obsidian Git installé et activé dans votre coffre, ou directement en ligne de commande : 
```sh
cd votre_dossier-coffre
git clone url_du_depot`
```











8. Si cela ne fonctionne vraiment pas pour vous, ouvrez une [issue](https://github.com/ericECmorlaix/simple_template_obsidian_mkdocs/issues/new/choose) et expliquez moi votre problème...


Ce site est généré à partir du template <https://github.com/ericECmorlaix/simple_template_obsidian_mkdocs>, un simple modèle de dépôt GitHub pour publier des notes d'Obsidian via MkDocs avec le thème Material qui présente la marche à suivre et montre quelques solutions permettant plus ou moins la transition de la syntaxe d'Obsidian vers celle de MkDocs.

Ce site est un exemple simple de publication sur le Web, avec MkDocs et le thème Material, de notes écrites dans Obsidian et hébergées sur GitHub. Il montre quelques solutions permettant plus ou moins la transition de la syntaxe d'Obsidian vers celle de MkDocs.



![[undraw_informed_decision_p2lh.svg]]

## Degemer Mat !

Le texte en MarkDown de la page `index.md` du dossier `/docs` devient la page d'accueil en HTML que vous voyez ici.

Les dossiers présents dans `/docs` apparaissent comme sections principales de la barre de navigation. De même pour le titre de niveau 1 `# Accueil` écrit au début du fichier `index.md`.

Chaque note, `fichier.md` écrit en MarkDown, devient une nouvelle page du site dans leur section respective. Le noms de ces fichiers sont visible dans la barre d'URL. Les titres et sous-titres de la table des matières apparaissent dans des sous-sections d'un menu secondaire.

> En l'absence de titre de niveau 1 au début d'une note, c'est le nom du fichier qui apparaitra en tête de la sous-section.

Il est donc préférable dans Obsidian d'attribuer aux dossiers et fichiers des noms significatifs, sans caractère accentué ni espace et, de même que pour les titres et sous-titres, le mieux est de les choisir courts. 

> Ce nommage automatique peut-être modifié en définissant manuellement la rubrique `nav` dans le fichier `mkdocs.yml`, ce qui devient cependant vite fastidieux... 






Un simple modèle de dépôt GitHub pour publier des notes d'Obsidian via MkDocs avec le thème Material.

Le site ainsi produit est visible à l'adresse : <https://ericecmorlaix.github.io/simple_template_obsidian_mkdocs/>. Il montre quelques solutions permettant plus ou moins la transition de la syntaxe d'Obsidian vers celle de MkDocs.

Ce site est adossé à un [tutoriel (en construction)](https://ericecmorlaix.github.io/adn-Tutoriel_Obsidian/) qui présente la prise en main et quelques fonctionnalités d'Obisidian.

Ce template est basé sur <https://github.com/jobindjohn/obsidian-publish-mkdocs> et s'inspire également de <https://github.com/ObsidianPublisher/obsidian-mkdocs-publisher-template>




## Autres projets à regarder

- <https://github.com/ObsidianPublisher/obsidian-mkdocs-publisher-template> La solution de [Lisandra Simonetti](https://github.com/Lisandra-dev), beaucoup plus évoluée et associée à un plugin d'Obsidian.
- <https://github.com/mr-karan/notes>
- <https://github.com/jimbrig/obsidian_published>
- <https://github.com/Jackiexiao/foam-mkdocs-template>
- <https://github.com/foambubble/foam-template>
- <https://sarthaknarayan.tech/projects/obsidian-publish-github-action/>
- <https://github.com/mathieudutour/gatsby-digital-garden>
- <https://github.com/TuanManhCao/digital-garden>
- <https://forum.obsidian.md/t/my-obsidian-mkdocs-workflow/24424> | <https://tarekshehata.github.io/alkashi/>
-->