# MarkDown

A venir...

Mises en bouche  en attendant d'autres développements mais qui peut être suffisante, surtout associé au "Coffre de test" que l'on peut ouvrir à partir du bouton d'aide en bas à gauche de l'interface d'Obsidian :
![[bouton_aide.png]]

## Exercices de MarkDown

Un tutoriel en ligne pour découvrir la syntaxe MarkDown et s'entrainer à l'écrire : <https://www.markdowntutorial.com/fr/>

## Un résumé extrait du [guide obsidian de Johackim](https://johackim.com/obsidian#syntaxe-markdown)

### Syntaxe Markdown

Obsidian utilise la syntaxe Markdown par défaut :

-   `[Link Text](URL)` : Créer un lien avec URL
-   `![Alt Text](URL)` : Créer une image
-   `- Bullet List` : Créer une liste
-   `1. Number List` : Créer une liste numérique
-   `**bold**` : Créer un texte en gras
-   `*italic*` : Créer un texte en italique
-   `**souligner**` : Créer un texte souligné
-   `~~Strikethrough~~` : Créer un texte barré
-   `> quote` : Créer une citation
-   `# Heading 1` : Créer un titre de niveau 1
-   `## Heading 2` : Créer un titre de niveau 2
-   `### Heading 3` : Créer un titre de niveau 3
-   `[ref1]` et `[ref1]: <url>` : Créer une référence
-   `[Link Text][ref1]` et `[ref1]: <url>` : Créer une référence avec un text personnalisé

### Syntaxe d'Obsidian

Mais il a quelques spécificités de syntaxes supplémentaires :

-   `[[Linking Note]]` : Créer un lien vers une autre note
-   `[[Linking Note|Link Name]]` : Créer un lien avec un nom personnalisé
-   `[[Linking Note#heading]]` : Créer un lien vers un titre d'une autre note
-   `![[Linking Note^]]` : Intégrer un bloc d'une autre note
-   `![[Filename]]` : Intégrer une autre note
-   `![250](https://johackim.com/soon?title=250 "Note bientôt disponible")` : Insérer une image embed de 250px de largeur
    
-   `![|250](https://site.xyz/image.png)` : Insérer une image de 250px de largeur
-   `#tag` : Créer un tag
-   `#nested/tag` : Créer un sous-tag
-   `[^Ref]` et `[^Ref]: Footnote text.` : Créer une note de bas de page
-   `^[Footnote text]` : Créer une note de bas de page en une ligne
-   `==highlight==` : Créer un texte surligné
-   `aliases: [Alias1, Alias2]` : Créer un alias (à ajouter dans le frontmatter)
-   `- [ ] Task list` : Créer une tâche
-   `- [x] Task list` : Cocher une tâche