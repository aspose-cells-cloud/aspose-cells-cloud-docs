---
title: "Travail avec les objets OLE Excel"
second_title: "Document"
linktitle: "OleObjects"
type: docs
url: /oleobjects/
aliases: [/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "Utilisez l’API REST Aspose.Cells Cloud pour récupérer, ajouter, mettre à jour, supprimer et convertir des objets OLE dans les feuilles de calcul Excel. Les SDK sont disponibles pour Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift et Android."
weight: 100
ArticleTitle: "Travail avec les objets OLE Excel – Guide pour récupérer, ajouter, mettre à jour, supprimer et convertir des objets OLE"
---

**Comment travailler avec des objets OLE dans une feuille de calcul Excel**

L’API REST Aspose.Cells Cloud fournit un ensemble complet d’opérations pour gérer les objets OLE de manière programmatique. Ci-dessous figure un tableau de référence synthétique pour chaque opération, incluant la méthode HTTP, le modèle d’endpoint, les paramètres requis et un exemple de réponse.

- [Comment récupérer un objet OLE à partir d’une feuille de calcul Excel](/cells/oleobjects/get/)
  - **Méthode :** `GET`  
  - **Endpoint :** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Paramètres :** `fileName` (chaîne de caractères), `sheetName` (chaîne de caractères), `oleObjectIndex` (entier)  
  - **Exemple de réponse :**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Comment ajouter un objet OLE dans une feuille de calcul Excel](/cells/oleobjects/add/)
  - **Méthode :** `POST`  
  - **Endpoint :** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Paramètres :** `fileName`, `sheetName`, `oleObject` (binaire ou en base‑64), `imageFormat` (facultatif)  
  - **Exemple de corps de requête :** multipart/form‑data contenant le flux du fichier.  
  - **Exemple de réponse :** `201 Created` avec l’en‑tête *Location* pointant vers le nouvel objet OLE.

- [Comment mettre à jour un objet OLE spécifique dans une feuille de calcul Excel](/cells/oleobjects/update/)
  - **Méthode :** `PUT`  
  - **Endpoint :** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Paramètres :** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (contenu mis à jour)  
  - **Exemple de réponse :** `200 OK` avec les métadonnées mises à jour de l’objet.

- [Comment convertir un objet OLE en image dans une feuille de calcul Excel](/cells/oleobjects/convert/)
  - **Méthode :** `GET`  
  - **Endpoint :** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Paramètres :** `fileName`, `sheetName`, `oleObjectIndex`, `format` (par ex. `png`, `jpeg`)  
  - **Exemple de réponse :** Flux binaire de l’image issue de la conversion de l’objet OLE.

- [Comment supprimer tous les objets OLE d’une feuille de calcul Excel](/cells/oleobjects/clear/)
  - **Méthode :** `DELETE`  
  - **Endpoint :** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Paramètres :** `fileName`, `sheetName`  
  - **Exemple de réponse :** `204 No Content` indiquant que tous les objets OLE ont été supprimés.

- [Comment supprimer un objet OLE spécifique dans une feuille de calcul Excel](/cells/oleobjects/delete/)
  - **Méthode :** `DELETE`  
  - **Endpoint :** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Paramètres :** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Exemple de réponse :** `204 No Content` confirmant la suppression de l’objet.