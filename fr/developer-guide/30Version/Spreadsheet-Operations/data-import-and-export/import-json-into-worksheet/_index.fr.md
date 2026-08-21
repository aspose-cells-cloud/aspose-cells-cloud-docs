---
title: "Importer des données JSON dans Excel"
second_title: "Document"
linktitle: "Importer JSON"
type: docs
url: /import-json-data-into-excel/
aliases: [/import/json/]
keywords: "Aspose.Cells Cloud, import JSON, API Excel, import REST JSON, exemples SDK"
description: "Découvrez comment importer des données JSON dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut les détails des points de terminaison, des exemples de requête/réponse et du code SDK pour .NET, Java et Python."
weight: 40
---

Cet **API REST importe des données JSON** dans une feuille de calcul Excel.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et exigent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### **Paramètres de la requête**

| Nom du paramètre      | Emplacement   | Type   | Description                                                                                          |
| --------------------- | ------------- | ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | chemin (Path) | string | Le nom du fichier du classeur.                                                                       |
| importJsonRequest     | corps HTTP    | class  | La charge utile de la requête contenant les détails de l’import JSON.                               |
| password              | chaîne de requête (Query string) | string | Mot de passe pour ouvrir le classeur (le cas échéant, s’il est protégé).                            |
| folder                | chaîne de requête (Query string) | string | Le dossier contenant le classeur original.                                                           |
| storageName           | chaîne de requête (Query string) | string | Le nom du stockage où réside le classeur.                                                            |
| outPath               | chaîne de requête (Query string) | string | Chemin du fichier de sortie après l’import. Si omis, le classeur mis à jour est renvoyé dans la réponse. |
| outStorageName        | chaîne de requête (Query string) | string | Nom du stockage pour le fichier de sortie.                                                           |
| checkExcelRestriction | chaîne de requête (Query string) | string | Indicateur précisant s’il faut appliquer les restrictions spécifiques à Excel (true/false).         |

### **Exemple de corps de requête**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Réponse

Une requête réussie renvoie **HTTP 200** avec une charge utile JSON similaire à :

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codes d’état possibles :

| Code | Signification                                     |
| ---- | ------------------------------------------------- |
| 200  | Import réussi                                     |
| 400  | Requête incorrecte – données manquantes ou invalides |
| 401  | Non autorisé – jeton invalide ou manquant         |
| 500  | Erreur interne du serveur                         |


## Comment utiliser l’API PostWorkbookImportJson avec les SDK

### Spécification de l’API PostWorkbookImportJson

La [spécification OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) définit une interface de programmation publiquement accessible et permet d’effectuer directement des interactions REST depuis un navigateur web.

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus efficace pour accélérer le développement. Les SDK gèrent les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Pour une liste complète des SDK Aspose.Cells Cloud, veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

---