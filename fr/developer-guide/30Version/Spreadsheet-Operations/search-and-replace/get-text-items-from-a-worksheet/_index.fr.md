---
title: "Récupérer des éléments textuels à partir d'une feuille de calcul Excel"
second_title: "Document"
linktitle: "Obtenir les éléments textuels dans une feuille de calcul"
type: docs
url: /fr/worksheets/get-text-items/
aliases: [  /fr/get-text-items-from-a-worksheet/ ]
weight: 20
keywords: "Aspose.Cells, API Cloud, Excel, feuille de calcul, éléments textuels, REST"
description: "Récupérer tous les éléments textuels d'une feuille de calcul spécifique dans un fichier Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples cURL, du code SDK, des étapes d’authentification et le schéma de réponse."
ArticleTitle: "Récupérer des éléments textuels à partir d'une feuille de calcul Excel"
---

## API REST

Cette API REST lit les éléments textuels d'une feuille de calcul dans un fichier Excel.

```
https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{worksheet}/textItems
```

### Sécurité et authentification
Les API REST Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Paramètres de la requête


| Nom du paramètre | Type   | Emplacement | Obligatoire | Description                                            |
|------------------|--------|-------------|-------------|--------------------------------------------------------|
| name             | string | path        | Oui         | Nom du fichier classeur.                               |
| sheetName        | string | path        | Oui         | Nom de la feuille de calcul.                           |
| folder           | string | query       | Non         | Chemin du dossier contenant le classeur.               |
| storageName      | string | query       | Non         | Nom du stockage Aspose Cloud.                          |

### **Réponse**

```json
{
  "Status":"OK",
  "Code":200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

**Codes de statut HTTP**

| Code | Signification               | Description                                             |
|------|-----------------------------|---------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Requête incorrecte          | Paramètres manquants ou non valides (par exemple, type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                         |
| 413  | Charge utile trop grande     | Le fichier téléchargé dépasse la limite de taille.     |
| 500  | Erreur interne du serveur   | Erreur inattendue sur le serveur.                       |

## Comment utiliser l’API GetWorksheetTextItems avec les SDK

### Spécification de l’API GetWorksheetTextItems

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetTextItems){:target="_blank" rel="noopener noreferrer"} définit une interface de programmation accessible publiquement et permet d’effectuer directement des interactions REST depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer des appels à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/sheet1/textItems" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "Text": "string"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Utiliser les SDK Aspose.Cells Cloud

Les SDK simplifient l'intégration en gérant les détails de bas niveau et en vous permettant de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment effectuer des appels aux services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetTextItems.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetTextItems.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetTextItems.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetTextItems.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetTextItems.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetTextItems.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetTextItems.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetTextItems.go" >}}

{{< /tab >}}

{{< /tabs >}}