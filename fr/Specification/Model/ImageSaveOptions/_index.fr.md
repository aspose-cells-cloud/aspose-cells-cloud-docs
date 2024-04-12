---
title: ImageSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/imagesaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : ImageSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **imageEnregistrerOptions**

 Représente les options d’enregistrement du fichier image.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Type d'image graphique| Chaîne| Vrai| FAUX|| Indiquez le type d'image du graphique lors de la conversion.|
| EmbededImageNameInSvg| Chaîne| Vrai| FAUX|| Indiquez le nom de fichier de l’image intégrée en svg. Il doit s'agir du chemin complet avec un répertoire comme "c:\\xpsEmbeded"|
| Résolution horizontale| Entier| Vrai| FAUX|| Obtient ou définit la résolution horizontale des images générées, en points par pouce. Applique la méthode de génération d'image à l'exception des images au format Emf. La valeur par défaut est 96.|
| Format d'image| Chaîne| Vrai| FAUX||Obtient ou définit le format des images générées. N'appliquez pas la méthode qui renvoie un objet Bitmap. La valeur par défaut est ImageFormat.Bmp. N'appliquez pas la méthode qui renvoie un objet Bitmap.|
| EstCellAutoFit| Booléen| Vrai| FAUX|| Indique si la largeur et la hauteur des cellules sont automatiquement ajustées en fonction de la valeur de la cellule. La valeur par défaut est fausse.|
| Une page par feuille| Booléen| Vrai| FAUX|| Si OnePagePerSheet est true , tout le contenu d’une feuille sera affiché sur une seule page. Le format de papier de la configuration de la page ne sera pas valide et les autres paramètres de la configuration de la page prendront toujours effet.|
| Zone uniquement| Booléen| Vrai| FAUX|| Si cette propriété est vraie, seule la zone sera affichée et aucune échelle ne prendra effet.|
| ImpressionPage| Chaîne| Vrai| FAUX|| Indique quelles pages ne seront pas imprimées.|
| ImprimerAvecStatusDialog| Booléen| Vrai| FAUX|| Si PrintWithStatusDialog = true , une boîte de dialogue affichera l'état actuel de l'impression. sinon, aucune boîte de dialogue de ce type ne s'affichera.|
|Qualité| Entier| Vrai| FAUX||Obtient ou définit une valeur déterminant la qualité des images générées à appliquer uniquement lors de l'enregistrement des pages au format Jpeg. N'a d'effet que lors de l'enregistrement sous JPEG. La valeur doit être comprise entre 0 et 100. La valeur par défaut est 100.|
| TiffCompression| Chaîne| Vrai| FAUX|| Obtient ou définit le type de compression à appliquer uniquement lors de l'enregistrement des pages au format Tiff. N'a d'effet que lors de l'enregistrement sous TIFF. La valeur par défaut est Lzw.|
| Résolution verticale| Entier| Vrai| FAUX|| Obtient ou définit la résolution verticale des images générées, en points par pouce. Applique la méthode de génération d'image sauf l'image au format Emf. La valeur par défaut est 96.|
| EnregistrerFormat| Chaîne| Vrai| FAUX|||
| Dossier de fichiers mis en cache| Chaîne| Vrai| FAUX|||
| Effacer les données| Booléen| Vrai| FAUX|||
| Créer le répertoire| Booléen| Vrai| FAUX|||
| Activer la compression HTTP| Booléen| Vrai| FAUX|||
| Actualiser le cache de graphiques| Booléen| Vrai| FAUX|||
|Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : (EnregistrerOptions)[Enregistreroptions]