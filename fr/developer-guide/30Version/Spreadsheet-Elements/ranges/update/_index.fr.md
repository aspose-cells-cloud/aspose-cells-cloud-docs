---
title: "Comment mettre à jour le contenu d'une plage dans une feuille Excel"
second_title: "Document"
linktype: "Mise à jour"
type: docs
url: /fr/ranges/update/
keywords: "Excel, mise à jour de plage, Aspose.Cells Cloud, API REST, feuille de calcul, style de plage, valeurs de plage, hauteur de ligne, largeur de colonne"
description: "Mettre à jour le contenu d'une plage dans une feuille Excel à l'aide de l'API REST Aspose.Cells Cloud. Modifier les styles, les valeurs, les hauteurs de ligne et les largeurs de colonne via les SDK pris en charge."
weight: 20
ArticleTitle: "Comment mettre à jour le contenu d'une plage dans une feuille Excel – Documentation Aspose.Cells Cloud"
---

## Utilisation des opérations de mise à jour du contenu d'une plage dans une feuille Excel

Avant d'utiliser les opérations de mise à jour, assurez-vous de disposer d'un jeton d'API Aspose.Cells Cloud valide et que le classeur cible est stocké dans votre stockage cloud. L'API est accessible via des SDK pour Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift.

Un résumé concis des quatre principales actions de mise à jour est fourni ci-dessous. Ce tableau fournit aux développeurs une référence rapide concernant la méthode HTTP, le modèle d'endpoint, les paramètres clés et la réponse typique en cas de succès pour chaque opération.

| Action              | Méthode HTTP | Modèle d'endpoint                                                                                     | Paramètres clés                | Réponse 200‑OK               |
|---------------------|--------------|--------------------------------------------------------------------------------------------------------|--------------------------------|------------------------------|
| Définir le style    | PUT          | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | Objet `style`                  | Style de plage mis à jour    |
| Définir les valeurs | POST         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | Tableau `values`               | Valeurs de plage mises à jour|
| Hauteur de ligne    | PUT          | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | Nombre `height`                | Hauteur de ligne mise à jour |
| Largeur de colonne  | PUT          | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | Nombre `width`                 | Largeur de colonne mise à jour|

Cette page fournit un accès rapide aux quatre principales actions de mise à jour : définir le style d'une plage, définir les valeurs d'une plage, ajuster les hauteurs de ligne et ajuster les largeurs de colonne.

- [Comment définir le style d'une plage dans une feuille Excel.](/cells/ranges/update/style/) 
- [Comment définir les valeurs d'une plage dans une feuille Excel.](/cells/ranges/update/values/) 
- [Comment définir les hauteurs de ligne d'une plage dans une feuille Excel.](/cells/ranges/update/row-height/) 
- [Comment définir les largeurs de colonne d'une plage dans une feuille Excel.](/cells/ranges/update/column-width/)