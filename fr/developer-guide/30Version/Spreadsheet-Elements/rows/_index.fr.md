---
title: "Travail avec les lignes Excel – API Cloud Aspose.Cells"
ArticleTitle: "Travail avec les lignes Excel – API Cloud Aspose.Cells"
second_title: "Document"
linktype: "docs"
url: /fr/rows/
aliases: [  /fr/working-with-rows/ ]
keywords: "Aspose.Cells, lignes Excel, API REST, manipulation de feuilles de calcul"
description: "Manipulez des lignes dans des fichiers Excel à l’aide de l’API REST Aspose.Cells Cloud. Prend en charge Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby et Swift."
weight: 100
---

## Travail avec les lignes dans un fichier Excel

**Dernière mise à jour : juillet 2026**

- [Comment obtenir les informations d'une ligne dans une feuille de calcul Excel.](/cells/rows/get/row/)
- [Comment ajouter une ligne vide dans une feuille de calcul Excel.](/cells/rows/add/row/)
- [Comment copier des lignes dans une feuille de calcul Excel.](/cells/rows/copy/)
- [Comment masquer des lignes dans une feuille de calcul Excel.](/cells/rows/hide/)
- [Comment afficher des lignes masquées dans une feuille de calcul Excel.](/cells/rows/unhide/)
- [Comment grouper des lignes dans une feuille de calcul Excel.](/cells/rows/group/)
- [Comment dissocier des lignes dans une feuille de calcul Excel.](/cells/rows/ungroup/)
- [Comment supprimer une ligne d'une feuille de calcul](/cells/rows/delete/)

Référence rapide de l'API pour les opérations courantes sur les lignes :

| Opération        | Méthode HTTP | Endpoint                                                               | Paramètres clés                        |
|------------------|--------------|------------------------------------------------------------------------|----------------------------------------|
| [Obtenir une ligne](https://docs.aspose.cloud/cells/rows/get/row/)     | GET          | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Ajouter une ligne](https://docs.aspose.cloud/cells/rows/add/row/)     | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows`                       | `rowIndex`, `height`                   |
| [Copier des lignes](https://docs.aspose.cloud/cells/rows/copy/)      | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/copy`                  | `sourceIndex`, `destinationIndex`, `rowCount` |
| [Supprimer une ligne](https://docs.aspose.cloud/cells/rows/delete/)   | DELETE       | `/cells/{fileName}/worksheets/{sheetName}/rows/{rowIndex}`            | `fileName`, `sheetName`, `rowIndex`    |
| [Masquer des lignes](https://docs.aspose.cloud/cells/rows/hide/)      | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/hide`                  | `startIndex`, `endIndex`               |
| [Afficher des lignes masquées](https://docs.aspose.cloud/cells/rows/unhide/)  | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/unhide`                | `startIndex`, `endIndex`               |
| [Grouper des lignes](https://docs.aspose.cloud/cells/rows/group/)    | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/group`                 | `startIndex`, `endIndex`               |
| [Dissocier des lignes](https://docs.aspose.cloud/cells/rows/ungroup/) | POST         | `/cells/{fileName}/worksheets/{sheetName}/rows/ungroup`               | `startIndex`, `endIndex`               |

**Détails des requêtes / réponses**

- **Obtenir une ligne**  
  *Requête* : Aucun corps requis.  
  *Réponse (200)* :  
  ```json
  {
    "RowIndex": 5,
    "Height": 15.0,
    "IsHidden": false,
    "Style": { ... }
  }
  ```  
  *Erreurs* : 400 Bad Request (index invalide), 404 Not Found (fichier ou feuille manquant(e)).

- **Ajouter une ligne**  
  *Corps de la requête (JSON)* :  
  ```json
  {
    "RowIndex": 10,
    "Height": 20.0
  }
  ```  
  *Réponse (201)* :  
  ```json
  { "Code": "Success", "Status": "Row added", "RowIndex": 10 }
  ```  
  *Erreurs* : 400 Bad Request (paramètres manquants ou invalides), 401 Unauthorized.

- **Copier des lignes**  
  *Corps de la requête (JSON)* :  
  ```json
  {
    "SourceIndex": 2,
    "DestinationIndex": 8,
    "RowCount": 3
  }
  ```  
  *Réponse (200)* :  
  ```json
  { "Code": "Success", "Status": "Rows copied" }
  ```  
  *Erreurs* : 400 Bad Request, 404 Not Found.

- **Supprimer une ligne**  
  *Requête* : Aucun corps.  
  *Réponse (200)* :  
  ```json
  { "Code": "Success", "Status": "Row deleted", "RowIndex": 7 }
  ```  
  *Erreurs* : 400 Bad Request, 404 Not Found.

- **Masquer des lignes**  
  *Corps de la requête (JSON)* :  
  ```json
  { "StartIndex": 3, "EndIndex": 5 }
  ```  
  *Réponse (200)* : `{ "Code": "Success", "Status": "Rows hidden" }`  
  *Erreurs* : 400 Bad Request.

- **Afficher des lignes masquées** – même charge utile que *Masquer des lignes* ; réponse identique, statut « Rows unhidden ».

- **Grouper des lignes** – même charge utile que *Masquer des lignes* ; statut de réponse « Rows grouped ».

- **Dissocier des lignes** – même charge utile que *Masquer des lignes* ; statut de réponse « Rows ungrouped ».

Toutes les opérations exigent un jeton d’accès OAuth 2.0/JWT valide ainsi qu’une version appropriée du SDK.