dans les plugins communautaires, chercher "Pandoc Refernece List"

installer et activer le plugin

dans les paramètres du plugin, trouver le chemin vers votre installation de [[Pandoc]] (en effet, au préalable, il faut avoir installé Pandoc sur votre machine)

Pour trouver ce chemin : 
  - sur Windows, ouvrez un terminal (powershell pour Windows par exemple ; pour ouvrir powershell, la combinaison shift + click droit permet d'y arriver rapidement), puis entrer dans le terminal ```Get-Command pandoc```. 
  - Avec un terminal sous Linux ou sous MacOS, la commande pour trouver le chemin est ``ẁhich pandoc``` - Copier/coller le résultat. Pour copier un texte dans le terminal : Ctrl + **Maj** + C (pour coller : Ctrl + **Maj** +V

Dans le chemin vers le fichier biblio, entrez le chemin où se trouve le fichier .bib que vous avez exporté de Zotero, gràce au plugin Betterbibtex. 

Par exemple, si vous avez créé dans votre coffre Obsidian, un dossier biblio, le chemin (relatif) sera /biblio/fichier.bib ; si le chemin relatif ne fonctionne pas, indiquer le chemin depuis votre Home (si le coffre est sur le bureau ce chemin sera -sous Windows - : C:/user/votre_nom_utilisateur/Bureau/coffre_obsidian/biblio/fichier.bib

cliquer sur "tirer la référence depuis Zotero / pull bibliography from Zotero"
Laisser le port ouvert à 23119

Si la connexion à [[Zotero]] s'est bien effectuée, vous devriez voir la liste des collections de votre bibliothèque Zotero, sélectionner "ma bibliothèque". 

Sélectionner un style bibliographique, par exemple "American Psychological Association"

Laisser le reste des options par défaut

Ouvrir le menu des raccourcis ; créer un raccourci pour la fonction Pandoc Reference List : Show reference list

ouvrir une note, faire ce raccourci. Si une référence a déjà été intégrée à la note par le biais du plugin Citations ou du plugin Zotero intégration, la ou les références présentes dans le texte doivent s'afficher selon le style choisi (cf. APA ci-dessus) dans une colonne de droite.

Il est possible de copier en cliquant sur une icone en haut de cette colonne, pour copier depuis la colonne de droite toute la biblio relative à la note et la coller à la fin de la note. 