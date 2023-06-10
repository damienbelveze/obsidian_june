
# 1. Résumé

logiciel libre pour réaliser de la gestion de références. 
Les références de Zotero sont formatées en bibtex. 
Pour faire fonctionner Zotero avec Obsidian, il faut :

- télécharger le plugin communautaire Citation de Jon Gauthier pour Obsidian (et le paramétrer)
- télécharger le plugin Betterbibtex pour Zotero. 

# 2. Détail


## le plugin betterbibtex

[disponible sur Github](https://github.com/retorquere/zotero-better-bibtex/releases/tag/v6.7.79)

Pour l'installation, suivre la vidéo (en sourdine)

<iframe width="560" height="315" src="https://www.youtube.com/embed/qz9YvHC25-E?start=382" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>


## module Citations de Jon Gautier

Prérequis : disposer de Zotero avec le plugin BetterBibTeX chargé. 
Avoir téléchargé Pandoc et un éditeur LaTeX sur sa machine.
Si la version de Pandoc dont on dispose n'inclue pas le plugin pandoc-citeproc, charger ce plugin. 

1. Charger dans Obsidian le [plugin](https://github.com/hans/obsidian-citation-plugin/tree/0.1.3) **Citations** qui permet d'importer des données dans Zotero

2. Comment charger un plugin dans Obsidian ? 
    -Paramètres > Plugins Tiers > désactiver le mode sans échec
	-Pour ce plugin, chercher avec "Citations"
	-installer ce plugin
	
3. Créer dans Obsidian votre espace de travail 
    - créer un dossier (intitulé Article)
    - créer une note (qui deviendra le futur article à publier)
    
 4. Dans Zotero exporter la collection qui correspond aux références de l'article en la tenant à jour (appelons ce fichier references.bib). Enregistrer le fichier dans le dossier article sous un répertoire qu'on crée à l'occasion (par exemple en l'intitulant 'references')
 
 5. Dans les options du plugin, indiquer le nom du répertoire ('références') qui contient le fichier .bib provenant de Zotero. Indiquer le chemin relatif vers le fichier bib : /espacedetravail/references/references.bib
     Si le chemin est le bon, le nombre d'enregistrements du fichier bib devrait apparaître. 
	 Il faut également définir un dossier où iront les références bibliographiques issues de Zotero (notes précédées d'un \@). Si on souhaite que celles-ci aillent à la racine du coffre, on supprimer le texte qui est par défaut. Si on souhaite les ranger dans un dossier particulier, créer ce dossier (par exemple sous .obsisian) et indiquer au plugin le chemin vers ce dossier.
	 
6. Dans les Paramètres d'Obsidian > raccourcis clavier, paramétrer un raccourci clavier pour insérer une citation en format markdown (Citations: insert markdown citation). Saisissons à cet endroit par exemple la combinaison de chiffres suivante : **Shift + Ctrl + E**. Cette combinaison de touches permettra d'insérer un appel de citation à l'endroit du texte où on cela sera pertinent. 
