# 1. Matin

## 1.1 installation

aller sur https://github.com/damienbelveze/obsidian_june
télécharger l'archive (zip) sur le bureau
dézipper
ouvrir Obsidian
Nouveau coffre à partir d'un dossier existant. 
Sélectionner le dossier Obsidian_June

### 1.2 Présentation d'Obsidian et de la journée avec la carte mentale

le présentateur ouvre la carte mentale avec Freeplane et commente les branches. 

Au niveau de Zettelkasten, montrer comment une note peut donner lieu à un diaporama
(faire activer le plugin par défaut "Diapositives")
Le présentateur explique les similarités et les différences entre la méthode Zettelkasten et l'usage d'Obsidian. 

Présentation de Markdown (cf note markdown et markdown_memo)

Notes capables de contenir du texte et du code mélangés dans un format globalement en markdown
Faire une démo de l'exécution d'un code avec le plugin Execute-code. 


## 1.3. Créer le graphe de notes


Les noeuds surlignés en orange indiquent comment les notes peuvent être liées entre elles. Pour chacun de ces noeuds surlignés existe une note. 

- Faire les liens internes avec des wikiliens.
- appliquer aux titres la bonne syntaxe selon leurs niveaux
- appliquer le style citation aux textes écrits entre guillemets
- restaurer les listes à puce
- restaurer les liens externes
- insérer le tableau PKM.ods dans la note "jardin_numérique"
- insérer une vidéo de Richard Stallman dans la note "logiciel_libre"
- télécharger depuis un site web une belle image de pierre d'obsidienne, enregistrer cette image dans le dossier images. Faites le lien de telle sorte que cette image s'affiche dans la note "Obsidian"

## 1.4. Modèles, tags et alias

### 1.4.1 tags et alias

réserver un entête pour quelques notes : plain_text, zotero, pandoc, obsidian

```yaml
---
title: 
tags: []
aliases: []
```

tagger les notes mentionnées ci-dessus avec le tag "logiciel_libre"
apporter comme alias à la note "plain_text" les ajouts suivants dans l'entête : 
title : trouver un autre titre que le nom de fichier
aliases : indiquer les alias possibles (texte brut, plain text, texte simple)

### 1.4.2 modèles


créer une note "Modèle A" comportant l'entête suivant : 

```yaml
---
title: {{title}}
date: {{date: DD/MM/YYYY}}
tags: []
aliases: []
```

déplacer cette note dans le dossier Modeles
Aller dans les paramètres, dans les paramètres du plugin modèle, indiquer le chemin relatif vers le "modèle A". 
Définir un raccourci-clavier pour l'inclusion du modèle dans une nouvelle fiche (par exemple Ctrl+maj+M)

# Après-midi

## 2.1 CSS

Sous Obsidian_June>.obsidian>snippets, créer un fichier texte. 
aller chercher un bout de code CSS dans [la galerie de Akashagarwal](https://github.com/Dmytro-Shulha/obsidian-css-snippets/tree/master/Snippets)
coller ce bout de code CSS ('snippet') dans le document texte
renommer ce document texte (nom de fichier + extension .css au lieu de .txt)
Aller dans Apparence (en bas de la fenêtre), recharger la liste des snippets CSS et activer le fichier qui apparaît. 

## 2.2 Lien avec Zotero

Expliquer avec un schéma comment les deux applications vont pouvoir dialoguer entre elles. 
Charger le plugin betterbibtex pour Zotero
Charger le plugin Citations de Jon Gauthier
S'il s'agit du premier plugin communautaire que l'on télécharge, expliquer ce qu'est un plugin communautaire et comment on les installe et on les active. 
Si le parefeu de la pièce où a lieu la formation gène le chargement du plugin, faire charger le plugin manuellement depuis Github. 

Demander aux étudiants d'entrer dans Zotero les sources mentionnées dans la note "markdown". 

| source | note |
|:---|:---:|
|  https://eveille.hypotheses.org/5990  | Eveille   | 
| https://eriac.hypotheses.org/80 | Julien Dehut |
| https://www.sudoc.abes.fr/cbs/DB=2.1/SRCH?IKT=12&TRM=260187429 | Julie Denouel |
| https://theconversation.com/les-chercheurs-en-shs-savent-ils-ecrire-93024 | Vitali-Rosati |

Créer une collection dans Zotero avec ces documents (vérifier que les références sont complètes)
Exporter la collection en biblatex en gardant un jour (synchronisant avec Zotero), envoyer le fichier bib (par exemple sous le nom de markdown.bib) dans le coffre sous le dossier *biblio*
Créer sous Biblio un dossier *references*
Indiquer dans les préférences du plugin Citations le lien vers le fichier bib.
Dans les préférences du plugin opter pour le format biblatex (et non Json)
Pointer vers le dossier references comme dossier de destination des notes biblio créées par l'utilisation du plugin Citations. 
Définier un raccourci-clavier pour l'insertion de notes biblio dans le texte (par exemple Ctrl + Maj + E)
Au moyen de ce raccourci-clavier, insérer les quatre appels de citation en lien et place des URL mentionnées ci-dessus. 

A la fin de la note Markdown, ajouter un titre *Références*


## 2.3 Export en PDF avec Pandoc

Si les étudiants n'ont pas pu ou souhaité télécharger la suite LaTeX indiquée, préciser qu'ils pourront tester Pandoc en lien avec LaTex au moyen des ordinateurs de la classe mobile
(préalable : vérifier avec la DSI que tous les logiciels nécessaires - pandoc, obsidian, suite LaTeX, Zotero- sont bien installés.)

Si ce n'est fait, faire installer Pandoc par les étudiants. 
Présenter Pandoc et la manière de passer des commandes en Shell. 
Faire une démo de démonstration simple (pandoc fichier_source.md -o fichier destination.htm)

### 2.3.1 markdown vers html


### 2.3.2 markdown vers pdf

rappeler qu'on peut faire un export en PDF d'une note depuis l'interface d'Obsidian mais que cet export ne pourra pas gérer les références héritées de Zotero. 



