---
title: "Importer des données à l’aide du stockage"
second_title: "Document"
linktype: "Importer des données avec le stockage"
type: docs
url: /fr/import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Importer des données à l’aide du stockage : importez des données dans une feuille de calcul Excel à l’aide de l’API Aspose.Cells Cloud à partir de diverses sources de stockage. Prend en charge les formats JSON, CSV et d’autres via HTTPS."
keywords: "Aspose.Cells Cloud, Excel, Importer des données, API REST, Stockage cloud, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Importer des données à l’aide du stockage – Documentation de l’API Aspose.Cells Cloud"
---

Cet API REST permet d’importer des données dans un fichier Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type   | Emplacement | Description                                            |
| ---------------- | ------ | ----------- | ------------------------------------------------------ |
| name             | string | path        | Le nom du fichier Excel.                              |
| folder           | string | query       | Le chemin du dossier dans lequel le fichier est stocké. |
| storageName      | string | query       | Le nom du service de stockage.                        |
| importData       | object | body        | Objet JSON contenant les données à importer.          |

**Les paramètres d’options d’importation des données** sont décrits dans [le lien de référence](/cells/import/#import-data-option-parameter).

**Prérequis :** Vous devez fournir un jeton JWT valide dans l’en-tête `Authorization` et vous assurer que le classeur cible existe déjà à l’emplacement spécifié dans le stockage.

### Réponse

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                           |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                       |
| 413  | Charge utile trop grande      | Le fichier téléchargé dépasse la limite de taille. |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                            |

## Comment utiliser l’API PostImportData avec les SDK

### Spécification de l’API PostImportData

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">spécification OpenAPI</a> définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple ci-dessous montre comment appeler l’API Cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jeton JWT>"
```

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

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est le meilleur moyen d’accélérer le développement. Un SDK abstractise les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

L’exemple de code suivant montre comment appeler le service web Aspose.Cells à l’aide du SDK PHP :
---