---
title: HtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/htmlsaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : HtmlSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, HtmlSaveOptions
weight: 50
---
## **htmlEnregistrerOptions**

 Représente les options d’enregistrement du fichier .html.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Exporter les en-têtes de page| Booléen| Vrai| FAUX|||
| Exporter les pieds de page| Booléen| Vrai| FAUX|||
| ExportRowColumnHeadings| Booléen| Vrai| FAUX|||
| Afficher toutes les feuilles| Booléen| Vrai| FAUX|||
| Options d'image| Classe : ImageOrPrintOptions| Vrai| FAUX|||
| Enregistrer en tant que fichier unique| Booléen| Vrai| FAUX|| Indique si vous enregistrez le code HTML sous forme de fichier unique. La valeur par défaut est fausse.|
| Exporter une feuille de travail masquée| Booléen| Vrai| FAUX|| Indique si vous enregistrez le code HTML sous forme de fichier unique. La valeur par défaut est fausse.|
| ExporterGridLines| Booléen| Vrai| FAUX|| Indique s'il faut exporter le quadrillage. La valeur par défaut est false.|
| PrésentationPréférence| Booléen| Vrai| FAUX|| Indiquer si le fichier HTML ou MHT est la préférence de présentation. La valeur par défaut est false. Si vous souhaitez obtenir une présentation plus belle, veuillez définir la valeur sur true.|
| Préfixe CellCss| Chaîne| Vrai| FAUX||Obtient et définit le préfixe du nom CSS, la valeur par défaut est "".|
| TableCssId| Chaîne| Vrai| FAUX|| Obtient et définit le préfixe du nom CSS du type tel que tr, col, td et ainsi de suite, ils sont contenus dans l'élément table qui a l'attribut spécifique TableCssId. La valeur par défaut est "".|
| EstFullPathLink| Booléen| Vrai| FAUX|| Indique si vous utilisez le lien de chemin complet dans sheet00x.htm, filelist.xml et tabstrip.htm. La valeur par défaut est fausse.|
| Exporter une feuille de travail CSS séparément| Booléen| Vrai| FAUX|| Indique si vous exportez la feuille de calcul CSS séparément. La valeur par défaut est false.|
| Exporter un style de bordure similaire| Booléen| Vrai| FAUX|||
| FusionnerVideTdForcely| Booléen| Vrai| FAUX||Indique si la fusion des éléments TD vides est forcée lors de l'exportation du fichier au format HTML. La taille du fichier HTML sera considérablement réduite après avoir défini la valeur sur true. La valeur par défaut est fausse. Si vous souhaitez importer le fichier HTML vers Excel ou exporter des lignes de grille parfaites lors de l'enregistrement du fichier au format HTML, veuillez conserver la valeur par défaut.|
| Exporter la coordonnée de cellule| Booléen| Vrai| FAUX|| Indique si l'exportation des coordonnées Excel des cellules non vides lors de l'enregistrement du fichier au format HTML. La valeur par défaut est fausse. Si vous souhaitez importer le code HTML de sortie vers Excel, veuillez conserver la valeur par défaut.|
| Exporter les titres supplémentaires| Booléen| Vrai| FAUX|| Indique si l'exportation de titres supplémentaires lorsque la longueur du texte est supérieure à la colonne d'affichage maximale. La valeur par défaut est fausse. Si vous souhaitez importer le fichier html vers Excel, veuillez conserver la valeur par défaut.|
| Exporter les titres| Booléen| Vrai| FAUX||Indique si les titres sont exportés lors de l'enregistrement du fichier au format HTML. La valeur par défaut est false. Si vous souhaitez importer le fichier html vers Excel, veuillez conserver la valeur par défaut.|
| ExporterFormule| Booléen| Vrai| FAUX|| Indique si l'exportation de la formule lors de l'enregistrement du fichier au format HTML. La valeur par défaut est vraie. Si vous souhaitez importer le code HTML de sortie vers Excel, veuillez conserver la valeur par défaut|
| Ajouter un texte d'info-bulle| Booléen| Vrai| FAUX|| Indique s'il faut ajouter du texte d'info-bulle lorsque les données ne peuvent pas être entièrement affichées.|
| ExporterBogusRowData| Booléen| Vrai| FAUX|| Indique si l'exportation de fausses données de la ligne inférieure est exportée. La valeur par défaut est true. Si vous souhaitez importer le fichier html ou mht vers Excel, veuillez conserver la valeur par défaut.|
| Exclure les styles inutilisés| Booléen| Vrai| FAUX|| Indique si les styles inutilisés sont exclus. La valeur par défaut est false. Si vous souhaitez importer le fichier html ou mht vers Excel, veuillez conserver la valeur par défaut.|
| Propriétés d'exportation du document| Booléen| Vrai| FAUX||Indique si vous exportez les propriétés du document. La valeur par défaut est vraie. Si vous souhaitez importer le fichier html ou mht vers Excel, veuillez conserver la valeur par défaut.|
| ExportWorksheetProperties| Booléen| Vrai| FAUX|| Indique si vous exportez les propriétés de la feuille de calcul. La valeur par défaut est vraie. Si vous souhaitez importer le fichier html ou mht vers Excel, veuillez conserver la valeur par défaut.|
| Exporter les propriétés du classeur| Booléen| Vrai| FAUX|| Indique si vous exportez les propriétés du classeur. La valeur par défaut est vraie. Si vous souhaitez importer le fichier html ou mht vers Excel, veuillez conserver la valeur par défaut.|
| ExportFrameScriptsAndProperties| Booléen| Vrai| FAUX|| Indique s'il faut exporter les scripts de frame et les propriétés du document. La valeur par défaut est true. Si vous souhaitez importer le fichier html ou mht vers Excel, veuillez conserver la valeur par défaut.|
| Répertoire des fichiers joints| Chaîne| Vrai| FAUX|| Le répertoire dans lequel les fichiers joints seront enregistrés. Uniquement pour l'enregistrement dans un flux HTML.|
| AttachedFilesUrlPrefix| Chaîne| Vrai| FAUX||Spécifiez le préfixe Url des fichiers joints tels que l'image dans le fichier HTML. Uniquement pour l'enregistrement dans un flux HTML.|
| Codage| Chaîne| Vrai| FAUX|||
| ExportActiveWorksheetOnly| Booléen| Vrai| FAUX|| Indique si vous exportez l’intégralité du classeur vers un fichier HTML.|
| ExporterChartImageFormat| Chaîne| Vrai| FAUX|| Obtenez ou définissez le format de l'image du graphique avant de l'exporter|
| ExporterImagesAsBase64| Booléen| Vrai| FAUX|||
| HiddenColDisplayType| Chaîne| Vrai| FAUX|| Colonne cachée (la largeur de cette colonne est de 0) dans Excel, avant de l'enregistrer au format HTML, si HtmlHiddenColDisplayType est "Supprimer", la colonne masquée ne sera pas affichée, si la valeur est "Cachée", la colonne sera affichée, mais était masqué, la valeur par défaut est "Caché"|
| HiddenRowDisplayType| Chaîne| Vrai| FAUX||Ligne cachée (la hauteur de cette ligne est 0) dans Excel, avant de l'enregistrer au format HTML, si HtmlHiddenRowDisplayType est "Supprimer", la ligne cachée ne serait pas affichée, si la valeur est "Cachée", la ligne serait affichée, mais était masqué, la valeur par défaut est "Caché"|
| HtmlCrossStringType| Chaîne| Vrai| FAUX|| Indique si une chaîne inter-cellules sera affichée de la même manière que MS Excel lors de l'enregistrement d'un fichier Excel au format html. Par défaut, la valeur est Default, donc pour les chaînes inter-cellules, il y a peu de différence entre les fichiers HTML créés par Aspose.Cells et MS Excel. Mais les performances de création de fichiers HTML volumineux, en définissant la valeur sur Cross, seraient plusieurs fois plus rapides que en le définissant sur Default ou Fit2Cell.|
| IsExpImageToTempDir| Booléen| Vrai| FAUX|| Indique si vous exportez les fichiers image vers le répertoire temporaire. Uniquement pour l'enregistrement dans un flux HTML.|
| Titre de la page| Chaîne| Vrai| FAUX||Le titre de la page html. Uniquement pour l'enregistrement dans un flux HTML.|
| ParseHtmlTagInCell| Booléen| Vrai| FAUX|| Analyser la balise HTML dans la cellule, comme, en tant que valeur de cellule, ou en tant que balise HTML, la valeur par défaut est vraie|
| EnregistrerFormat| Chaîne| Vrai| FAUX|||
| Dossier de fichiers mis en cache| Chaîne| Vrai| FAUX|||
| Effacer les données| Booléen| Vrai| FAUX|||
| Créer le répertoire| Booléen| Vrai| FAUX|||
| Activer la compression HTTP| Booléen| Vrai| FAUX|||
| Actualiser le cache de graphiques| Booléen| Vrai| FAUX|||
| Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : [Options d'enregistrement](/specification/model/saveoptions)

