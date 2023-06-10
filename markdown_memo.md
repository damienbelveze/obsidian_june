# 3. Rédiger ses notes en [[markdown]]

## 3.1 Qu'est-ce que Markdown ?

### une syntaxe très représentée dans l'écriture web

Markdown (avec une majuscule) est une syntaxe mise au point par John Gruber en 2004 et qui devait simplifier l'écriture web. Les développeurs l'utilisaient (et l'utilisent toujours) pour rédiger plus simplement du HTML en ayant recours à une syntaxe simplifiée par rapport au balisage du HTML. 
L'usage du Markdown a fini par se répandre au delà du cercle des développeurs web, et des auteurs, notamment académiques, s'en sont emparés pour écrire des textes convertibles non seulement en HTML mais également dans d'autres formats comme LaTeX ou PDF. 
Markdown permet d'utiliser des éditeurs de texte simple compatibles avec un nombre grandissant d'applications (Obsidian en fait partie). L'écriture en texte simple (plain text) a pour intérêt de pouvoir mêler du texte et du code et de se passer de formats propriétaires (par exemple word). 

### différentes saveurs de Markdown

John Gruber a fait en sorte de ne pas limiter l'usage de sa syntaxe, ce qui fait que beaucoup d'éditeurs se la sont appropriée pour monter leur propre éditeur Markdown. C'est pour cela que d'un outil à l'autre, on peut être confronté à des saveurs (flavors) différentes de Markdown. Par exemple, un lien ne se formate par exactement de la même manière sur Slackmarkdown et sur Atom. 

Le principe de Gruber était d'inciter l'utilisateur à avoir recours directement au HTML chaque fois que rien n'était prévu dans Markdown pour éditer tel ou tel élément du texte (par exemple les notes de bas de page ou les tableaux): 

>For any markup that is not covered by Markdown’s syntax, you simply use HTML itself. There’s no need to preface it or delimit it to indicate that you’re switching from Markdown to HTML; you just use the tags.

([John Gruber](https://daringfireball.net/projects/markdown/syntax#html))

Pourtant, comme le rappelle Knut Malvaer, les éditeurs ont eu tendance à adapter Markdown et à augmenter ses capacités pour satisfaire leurs usagers parmi lesquels la proportion des auteurs non développeurs n'a cessé de croître, ce qui fait que la syntaxe Markdown n'est plus entièrement unifiée d'un éditeur à l'autre[[@MelvaerThoughtsMarkdown2022]]. 
[Commonmark](https://commonmark.org/) a été créé pour fixer une syntaxe en markdown minimale, transposable d'un outil à l'autre, ce qui aide dans une certaine mesure les développeurs à gérer cette hétérogénéité dans le formatage en markdown (car le markdown est devenu depuis 2004 la *lingua franca* de l'écriture web). Cela n'empêche toujours pas un éditeur d'ajouter les fonctionnalités qu'il souhaite à cette base que constitue Commonmark. Ainsi Rmarkdown continue d'avoir une syntaxe markdown un peu différente de github sur des fonctions spécifiques même si à la base ces deux services utilisent Commonmark.

## 3.2 niveaux de titre, listes à puces

### niveaux de titre

Le titre de la note est distinct du nom du fichier. Le nom du fichier est la première chose qui est créée de la note. 
Dans une note, entourer un mot avec un double crochet (\[\[mot\]\]) crée automatiquement une note comportant mot.md dans le coffre. 
Une option des paramètres intitulée "toujours mettre à jour les liens internes" permet de maintenir le lien entre la note 1 comportant \\\[mot\]\] et la note rebaptisée par exemple word.md

Si on configure un titre dans le pavé Yaml, celui-ci apparaîtra comme titre du document exporté (par exemple en PDF). Voir la partie concernant [[Mode d'emploi d'Obsidian#5 2 YAML|YAML]]

| MD | niveau de titre | HTML |
|:---:|:---:|:---:|
| \# titre 1 | titre de niveau 1 | \<h1\> |
| \#\# titre 2 | titre de niveau 2 | \<h2\> |
| \#\#\# titre 3 | titre de niveau 3 | \<h3\> |
| \#\#\#\# titre 4 | titre de niveau 4 | \<h4\> |

### numérotation automatique des titres

Il est possible de numéroter automatiquement les entêtes de paragraphe de la manière suivante : 
- installer et activer le plugin communautaire *number heading plugins* pour Obsidian
- définir les raccourcis clavier nécessaires pour commander la numérotation des entêtes (ou la supprimer)

### liste à puces

le tiret ( - ) en début de phrase permet de faire une liste à puces : 

\- pommes  
\- poires  
\- bananes  

permet d'éditer

- pommes  
- poires  
- bananes  

Attention : la conversion de la note en markdown vers un autre format (ODT ou PDF notamment) peut mettre à mal les listes à puces si chaque élément qui les constitue n'est pas suivi de deux espaces en fin de ligne. 

sous liste à puces

- pommes



+ golden
+ pink lady

Pour éviter d'obtenir :

\- pommes \- poires \- bananes

dans le texte convertir en open document ou en PDF, ajouter systématiquement deux espaces dans le texte en markdown après pommes, poires et bananes.

## 3.3 tableaux, indentation, épigraphes


### éditer un tableau

**Code :** 

\| colonne A \| colonne B \| colonne C \|
\|\:\-\-\-\:\|\:\-\-\-\|\-\-\-\:\|
\|centre\|aligné gauche \|aligné droite 

**résultat :**

| colonne A | colonne B | colonne C |
|:---:|:---|---:|
| centre | aligné gauche | aligné droite |


Pour fusionner des cellules, il est actuellement nécessaire de recourir au HTML, car le markdown ne gère que des cellules équivalentes en taille (voir [[Mode d'emploi d'Obsidian#utilisation du HTML#pour faire des tableaux avec des colonnes ou des lignes fusionnées]])

````
|             |          Grouping           ||
First Header  | Second Header | Third Header |
 ------------ | :-----------: | -----------: |
Content       |          *Long Cell*        ||
Content       |   **Cell**    |         Cell |
 section   |     More      |         Data |
And more      | With an escaped '\|'         ||  
[Prototype table]
````



Si on dispose d'un tableau en format exel ou calc et qu'on veut le transposer en format markdown, on peut utiliser des ressources en ligne pour cela comme [*Table to Markdown*](https://tabletomarkdown.com/convert-spreadsheet-to-markdown/)

Le *pipe* (\|) qui sert à faire des tableaux peut aussi permettre de prendre en compte les espaces en début de phrase (pour une conversion en pdf avec Pandoc)

**code :** 

![respect des espaces en début de ligne](images/adonis.png)


**résultat : **

| Crépuscule
|     La nature est en extase de crépuscule
| Et son ode, 
|                              mon sang, 
| Un océan brûlant s'enroule, recommençant ses vagues
|                  jusqu'à moi

|                         (Adonis, *Ismaël*)




## 3.3 caractères

| MD | niveau de titre | HTML |
|:---:|:---:|:---:|
| \* | *italiques* | \<i\> |
| \*\*| **gras** | \<b\> |
| \~\~ | ~~barré~~ | \<s\> |
| \` | `code` | \<code\> |
| \=\= | ==surlignage== | \<mark> |

Pour "échapper" un caractère qui fait partie de la syntaxe du markdown (\*,\#, \~ par exemple), il faut faire précéder le caractère en question d'un antislash (\\) 


## 3.4  Liens, images, tags

### liens internes

Comme on l'a vu plus haut, pour faire un lien interne vers une note existante ou bien en créer une, il suffit de mettre entre double-crochets le mot ou l'expression qui correspond au nom de la note en question. 

Si l'on veut pointer vers une section de cette note, rajouter un dièze et sélectionner la partie de la note vers laquelle on veut pointer. 

Voici comment se formate par exemple un lien direct vers la partie de ce guide correspondant aux [[Mode d'emploi d'Obsidian#Les rétroliens|rétroliens]] :

Voici comment se formate par exemple un lien direct vers la partie de ce guide correspondant aux **\[\[Mode d'emploi d'Obsidian\#Les rétroliens\|rétroliens\]\]**

syntaxe du lien : 
\[\[nom de la note\#nom du header|texte du lien\]\]

Si on veut lier sur un bloc plutôt qu'un header, remplacer le \# par un \^ 

### notes de bas de page

\[\^\1\] permet de créer une note de bas de page portant le numéro 1. Exemple: 
première note de bas de page[^1]

[^1]:cette note de bas de page peut être placée n'importe où, elle apparaîtra forcément à la fin du document. Attention : dans la note de bas de page, ne pas utiliser les deux points (:) après les crochets.

### transclusion

Avec Obsidian, on la possibilité de faire un lien vers un document de la base de notes (une image, un PDF) de telle sorte qu'en mode lecture, si on passe la souris sur le lien, une prévisualisation du document s'affiche (pour y accéder, il suffit de cliquer) ou bien on peut aussi inclure le document dans la note, de telle sorte que celui-ci soit visible et déroulable. 
On peut le faire notamment pour un PDF : 

!\[\[document.pdf\]\]

Voir par exemple :

![[shortcuts.pdf]]

## 3.5 Les codes de bloc

```python
name = input("What's your name? ")
print("Hello " + name + ", have a good day!")
```

Possibilité d'éxécuter ce code avec le plugin communautaire *execute_code*