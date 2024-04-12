---
title: OoxmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/ooxmlsaveoptions/
description: "Aspose.Cells Spécification du modèle cloud : OoxmlSaveOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
weight: 50
---
## **ooxmlEnregistrerOptions**

 Représente les options d'enregistrement du fichier ooxml.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| ExporterCellName| Booléen| Vrai| FAUX||Indique si vous exportez le nom de la cellule vers un fichier Excel2007 .xlsx (.xlsm, .xltx, .xltm). Si le fichier de sortie est accessible par SQL Server DTS, cette valeur doit être vraie. Définir la valeur sur false augmentera considérablement les performances et réduira la taille du fichier lors de la création d'un fichier volumineux. La valeur par défaut est fausse.|
| Mise à jourZoom| Booléen| Vrai| FAUX|| Indique si le facteur de mise à l'échelle est mis à jour avant d'enregistrer le fichier si les propriétés PageSetup.FitToPagesWide et PageSetup.FitToPagesTall contrôlent la façon dont la feuille de calcul est mise à l'échelle.|
| ActiverZip64| Booléen| Vrai| FAUX|| Utilisez toujours les extensions ZIP64 lors de l'écriture d'archives zip, même lorsque cela n'est pas nécessaire.|
| EmbedOoxmlAsOleObject| Booléen| Vrai| FAUX|| Indique si l'intégration des fichiers Ooxml d'OleObject en tant qu'objet ole.|
| Type de compression| Chaîne| Vrai| FAUX|| Obtient et définit le type de compression du fichier ooxml.|
| EnregistrerFormat| Chaîne| Vrai| FAUX|||
| Dossier de fichiers mis en cache| Chaîne| Vrai| FAUX|||
| Effacer les données| Booléen| Vrai| FAUX|||
| Créer le répertoire| Booléen| Vrai| FAUX|||
| Activer la compression HTTP| Booléen| Vrai| FAUX|||
| Actualiser le cache de graphiques| Booléen| Vrai| FAUX|||
|Trier les noms| Booléen| Vrai| FAUX|||
| ValidateMergedAreas| Booléen| Vrai| FAUX|||

**Nom du parent** : (EnregistrerOptions)[Enregistreroptions]