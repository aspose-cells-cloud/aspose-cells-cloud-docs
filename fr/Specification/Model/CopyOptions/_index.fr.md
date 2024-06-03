---
title: Option de copie
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/specification/model/copyoptions/
description: "Aspose.Cells Spécification du modèle cloud : CopyOptions. Gérez sans effort Excel et d'autres feuilles de calcul avec des fonctionnalités telles que l'ouverture, la génération, l'édition, le fractionnement, la fusion, la comparaison et la conversion."
kwords: Excel, Office, feuille de calcul, Cloud REST API, options de copie
weight: 50
---
## **options de copie**

 Représente les options de copie.

| Nom de la propriété| Type de propriété| Nullable| Lecture seulement| Valeur par défaut| Description|
|:- |:- |:- |:- |:- |:- |
| Largeur de caractère de colonne| Booléen| Vrai| FAUX|| Indique si la largeur de colonne est copiée en unité de caractères.|
| CopierInvalidFormulasAsValues| Booléen| Vrai| FAUX|| Si la formule n'est pas valide pour la destination de destination, copiez uniquement les valeurs.|
| Copier les noms| Booléen| Vrai| FAUX||Indique si la copie des noms est effectuée.|
| ExtendToAdjacentRange| Booléen| Vrai| FAUX|| Indique si les plages sont étendues lors de la copie de la plage vers une plage adjacente.|
| Référer à la feuille de destination| Booléen| Vrai| FAUX|| Lors de la copie de la plage dans le même fichier et que le graphique fait référence à la feuille source, False signifie que la source de données du graphique copié ne sera pas modifiée. True signifie que la source de données du graphique copié fait référence à la feuille de destination.|
| ReferToSheetWithSameName| Booléen| Vrai| FAUX|| Dans MS Excel, lors de la copie de formules faisant référence à d'autres feuilles de calcul lors de la copie d'une feuille de calcul vers une autre, les formules copiées doivent faire référence au classeur source. Cependant, dans certaines situations, l'utilisateur peut avoir besoin que les formules copiées fassent référence à des feuilles de calcul portant le même nom dans le même classeur, par exemple lorsque ces feuilles de calcul ont été copiées avant cette opération de copie, cette propriété doit alors rester vraie.|

