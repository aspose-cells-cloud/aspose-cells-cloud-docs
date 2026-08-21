---
title: "Travail avec les plages Excel"
second_title: "Document"
linktitle: "Plage"
type: docs
url: /fr/ranges/
aliases: [  /fr/working-with-ranges/ ]
keywords: "Aspose.Cells, plage Excel, API REST, SDK, .NET, Java, Python, fusionner des cellules, copier une plage, définir la valeur d'une plage"
description: "Découvrez comment récupérer, modifier, styliser, fusionner, déplacer et copier des plages Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples de code SDK pour .NET, Java, Python et plus encore."
weight: 100
ArticleTitle: "Travail avec les plages Excel – Documentation Aspose.Cells Cloud"
---

Une **plage** représente une seule cellule, une ligne entière, une colonne entière, un bloc contigu de cellules ou une plage tridimensionnelle (3D) s’étendant sur plusieurs feuilles de calcul.

## Travail avec des plages dans un fichier Excel

L’API REST Aspose.Cells Cloud fournit des points de terminaison dédiés à chaque opération de plage. La liste suivante renvoie vers des exemples d’utilisation détaillés et inclut, pour référence rapide, la méthode HTTP et le point de terminaison correspondants.

- [Obtenir les plages nommées dans le classeur](/cells/get-named-ranges-inside-the-workbook/) – Récupère toutes les plages nommées définies dans un classeur, en retournant leurs adresses et leur portée. **API** : `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Obtenir les données des cellules selon une plage nommée](/cells/get-cells-data-based-on-named-range/) – Retourne les valeurs des cellules appartenant à une plage nommée spécifiée. **API** : `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Modifier les hauteurs des lignes dans la plage](/cells/cells/change-heights-of-rows-inside-the-range/) – Ajuste la hauteur de chaque ligne figurant dans la plage donnée. **API** : `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Modifier les largeurs des colonnes dans la plage](/cells/cells/change-widths-of-columns-inside-the-range/) – Modifie la largeur des colonnes intersectant la plage. **API** : `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Fusionner une plage de cellules en une seule cellule](/cells/combines-a-range-of-cells-into-a-single-cell/) – Fusionne les cellules sélectionnées en une seule cellule, en préservant la valeur située en haut à gauche. **API** : `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Copier une plage dans une feuille de calcul avec des options de collage](/cells/copy-range-in-a-worksheet-with-paste-options/) – Copie une plage source vers une plage de destination, avec des types de collage optionnels (valeurs, formats, formules, etc.). **API** : `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Définir le style de la plage](/cells/set-the-style-of-the-range/) – Applique les styles de police, de remplissage, de bordure et d’alignement à chaque cellule de la plage. **API** : `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Défusionner les cellules fusionnées de la plage](/cells/unmerge-merged-cells-of-the-range/) – Annule une opération de fusion précédente et restaure les cellules individuelles initiales. **API** : `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Déplacer une plage nommée avec une feuille de calcul Excel](/cells/move-a-named-ranged-with-a-excel-worksheet/) – Déplace une plage nommée vers une nouvelle adresse au sein de la même feuille de calcul ou vers une autre feuille de calcul. **API** : `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Définir la valeur d’une plage dans une feuille de calcul Excel](/cells/ranges/set-value/) – Écrit une valeur unique ou un tableau de valeurs dans la plage spécifiée. **API** : `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Toutes les demandes et réponses sont au format JSON. Incluez l’en-tête `Authorization` contenant votre jeton d’accès pour l’authentification.
---