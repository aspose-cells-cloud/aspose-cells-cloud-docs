---
title: "Convertir un tableau en tableau croisé dynamique"
second_title: "Document"
linktitle: Convertir
type: docs
url: /fr/pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/fr/create-a-pivottable-with-table/",
    "/fr/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "tableau croisé dynamique, objet liste, Aspose.Cells Cloud, API REST, convertir un tableau en tableau croisé dynamique"
description: "Découvrez comment créer un tableau croisé dynamique à partir d’un objet liste à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails de la requête, un exemple cURL et des références aux SDK."
weight: 60
ArticleTitle: "Convertir un tableau en tableau croisé dynamique – Documentation Aspose.Cells Cloud"
---

Cette API REST crée un **tableau croisé dynamique** à partir d’un objet liste.

Un tableau croisé dynamique résume les données provenant d’un objet liste, vous permettant d’analyser et de produire des rapports sur de grands jeux de données directement dans le classeur.

**Conditions préalables :**  
- Un jeton bearer JWT valide pour l’authentification.  
- Le classeur doit exister à l’emplacement de stockage spécifié.  
- La feuille de calcul cible doit contenir l’objet liste que vous souhaitez résumer.

## API PostWorksheetListObjectSummarizeWithPivotTable

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Sécurité et authentification**

Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre | Type    | Emplacement | Description                                |
| ---------------- | ------- | ----------- | ------------------------------------------ |
| name             | string  | chemin      | Nom du fichier du classeur.                |
| sheetName        | string  | chemin      | Feuille de calcul contenant l’objet liste. |
| listObjectIndex  | integer | chemin      | Index de l’objet liste dans la feuille de calcul. |
| destsheetName    | string  | paramètre de requête | Nom de la feuille de calcul de destination. |
| request          | object  | corps       | Charge utile JSON définissant le tableau croisé dynamique. |
| folder           | string  | paramètre de requête | Chemin du dossier contenant le classeur. |
| storageName      | string  | paramètre de requête | Nom du stockage. |

Le corps de la requête doit respecter le schéma JSON défini ci-dessous :

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Nom du nouveau tableau croisé dynamique." },
    "DestCellName": { "type": "string", "description": "Cellule en haut à gauche du tableau croisé dynamique (par ex., \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Index à partir de zéro des champs à placer dans les lignes."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Index à partir de zéro des champs à placer dans les colonnes."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Index à partir de zéro des champs à utiliser comme champs de données."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

La <a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jeton jwt>"
```

*Remarque : Utilisez le point de production (`api.aspose.cloud`) pour les environnements en production. Le point de test (`api-qa.aspose.cloud`) est destiné uniquement aux tests. HTTPS est requis pour tous les appels en production.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Codes de statut HTTP**

| Code | Signification               | Description                                              |
|------|-----------------------------|----------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou invalides (par ex., type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant. |
| 413  | Charge utile trop grande    | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur. |

## Famille de SDK Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK gère les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :