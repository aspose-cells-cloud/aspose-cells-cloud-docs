---
title: Option de sauvegarde paginée
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : PaginatedSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, PaginatedSaveOptions
weight: 50
---
## **Options de sauvegarde paginées**

 Représente les options de pagination.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Police par défaut| Chaîne| Vrai| FAUX|| Lorsque les caractères du Excel sont Unicode et ne sont pas définis avec la police correcte dans le style de cellule, ils peuvent apparaître sous forme de bloc dans le pdf, l'image. Définissez la police par défaut telle que MingLiu ou MS Gothic pour afficher ces caractères. Si cette propriété n'est pas définie, Aspose.Cells utilisera la police par défaut du système pour afficher ces caractères Unicode.|
| CheckWorkbookDefaultFont| Booléen| Vrai| FAUX|| Lorsque les caractères du Excel sont Unicode et ne sont pas définis avec la police correcte dans le style de cellule, ils peuvent apparaître sous forme de bloc dans le pdf, l'image. Définissez ceci sur true pour essayer d'utiliser la police par défaut du classeur pour afficher ces caractères en premier.|
| Vérifier la compatibilité des polices| Booléen| Vrai| FAUX|| Indique s’il faut vérifier la compatibilité des polices pour chaque caractère du texte.|
| IsFontSubstitutionCharGranularity| Booléen| Vrai| FAUX||Indique s'il convient de remplacer la police de caractère uniquement lorsque la police de la cellule n'est pas compatible avec celui-ci.|
| Une page par feuille| Booléen| Vrai| FAUX|| Si OnePagePerSheet est true , tout le contenu d'une feuille sera affiché sur une seule page. Le format de papier de la mise en page sera invalide et les autres paramètres de la mise en page prendront toujours effet.|
| Toutes les colonnes dans une page par feuille| Booléen| Vrai| FAUX|| Si AllColumnsInOnePagePerSheet est true , tout le contenu des colonnes d'une feuille sera affiché sur une seule page. La largeur du format de papier de la mise en page sera ignorée et les autres paramètres de la mise en page prendront toujours effet.|
| IgnorerErreur| Booléen| Vrai| FAUX|| Indique si vous devez masquer l'erreur lors du rendu. L'erreur peut être une erreur de forme, d'image, de rendu de graphique, etc.|
| SortieBlankPageWhenNothingToPrint| Booléen| Vrai| FAUX|| Indique s’il faut imprimer une page vierge lorsqu’il n’y a rien à imprimer.|
| Index des pages| Entier| Vrai| FAUX|| Obtient ou définit l'index de base 0 de la première page à enregistrer.|
| Nombre de pages| Entier| Vrai| FAUX|| Obtient ou définit le nombre de pages à enregistrer.|
| Type de page d'impression| Chaîne| Vrai| FAUX|| Indique quelles pages ne seront pas imprimées.|
| Type de quadrillage| Chaîne| Vrai| FAUX|| Obtient ou définit le type de quadrillage.|
| TextCrossType| Chaîne| Vrai| FAUX|| Obtient ou définit l'affichage du type de texte lorsque la largeur du texte est supérieure à la largeur de la cellule.|
| Langue d'édition par défaut| Chaîne| Vrai| FAUX|| Obtient ou définit la langue d'édition par défaut.|
| EmfRenderSetting| Chaîne| Vrai| FAUX|||
| Fusionner les zones| Booléen| Vrai| FAUX|||
| Trier les noms externes| Booléen| Vrai| FAUX|||
| Mettre à jourSmartArt| Booléen| Vrai| FAUX|||
| EnregistrerFormat| Chaîne| Vrai| FAUX|||
| Dossier de fichiers mis en cache| Chaîne| Vrai| FAUX|||
| Effacer les données| Booléen| Vrai| FAUX|||
| Créer le répertoire| Booléen| Vrai| FAUX|||
| Activer la compression HTTP| Booléen| Vrai| FAUX|||
| Actualiser le cache de graphiques| Booléen| Vrai| FAUX|||
| Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : [Options d'enregistrement](/specification/model/saveoptions)

**Nom des enfants** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSaveOptions](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
