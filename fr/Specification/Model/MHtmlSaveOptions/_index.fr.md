---
title: MHtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : MHtmlSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **mHtmlSaveOptions**

 Représente les options d’enregistrement du fichier .mhtml.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Répertoire des fichiers joints| Chaîne| Vrai| FAUX|| Le répertoire dans lequel les fichiers joints seront enregistrés. Uniquement pour l'enregistrement dans un flux HTML.|
| AttachedFilesUrlPrefix| Chaîne| Vrai| FAUX||Spécifiez le préfixe Url des fichiers joints tels que l'image dans le fichier HTML. Uniquement pour l'enregistrement dans un flux HTML.|
| Codage| Chaîne| Vrai| FAUX|| S’il n’est pas défini, utilisez Encoding.UTF8 comme type d’encodage par défaut.|
| ExportActiveWorksheetOnly| Booléen| Vrai| FAUX|| Indique si vous exportez l’intégralité du classeur vers un fichier HTML.|
| ExporterChartImageFormat| Chaîne| Vrai| FAUX|| Obtenez ou définissez le format de l'image du graphique avant de l'exporter|
| ExporterImagesAsBase64| Booléen| Vrai| FAUX|| Spécifie si les images sont enregistrées au format Base64 au format HTML, MHTML ou EPUB.|
| HiddenColDisplayType| Chaîne| Vrai| FAUX|| Colonne masquée (la largeur de cette colonne est de 0) dans Excel, avant de l'enregistrer au format HTML, si HtmlHiddenColDisplayType est "Supprimer", la colonne masquée ne serait pas affichée, si la valeur est "Cachée", la colonne serait affichée, mais était masqué, la valeur par défaut est "Caché"|
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
|Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : (EnregistrerOptions)[Enregistreroptions]