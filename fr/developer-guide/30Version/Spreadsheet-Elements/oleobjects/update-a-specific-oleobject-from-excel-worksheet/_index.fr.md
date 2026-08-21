---
title: "Mettre à jour un objet OLE dans une feuille de calcul Excel"
second_title: "Document"
linktitle: "Mettre à jour"
type: docs
url: /oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "mettre à jour objet OLE, Excel, Aspose.Cells Cloud, API REST, SDK"
description: "Découvrez comment mettre à jour un objet OLE (image, graphique, etc.) dans une feuille de calcul Excel à l’aide de l’API REST Aspose.Cells Cloud. Inclut des exemples cURL, SDK, étapes d’authentification et gestion des erreurs."
weight: 30
author: "Équipe de documentation Aspose Cloud"
lastmod: "2024-03-01"
ArticleTitle: "Mettre à jour un objet OLE dans une feuille de calcul Excel – Guide de l’API Aspose.Cells Cloud"
---

Cette API REST met à jour un **objet OLE** dans une feuille de calcul Excel.

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

## API PostUpdateWorksheetOleObject

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

Les paramètres de la requête sont les suivants :

| Nom du paramètre | Type    | Emplacement du paramètre | Description                                          |
| ---------------- | ------- | ------------------------ | ---------------------------------------------------- |
| name             | string  | path                     | Nom du classeur.                                     |
| sheetName        | string  | path                     | Nom de la feuille de calcul.                         |
| oleObjectIndex   | integer | path                     | Index de l’objet OLE dans la feuille de calcul.      |
| ole              | object  | body                     | Représentation JSON de l’objet OLE à mettre à jour.  |
| folder           | string  | query                    | Dossier contenant le classeur.                       |
| storageName      | string  | query                    | Nom du service de stockage.                          |

### Champs du corps de la requête

| Champ                 | Type    | Obligatoire | Description                                                |
| --------------------- | ------- | ----------- | ---------------------------------------------------------- |
| ImageSourceFullName   | string  | facultatif  | Chemin vers le fichier image utilisé pour l’objet OLE.     |
| IsAutoSize            | boolean | facultatif  | Indique si l’objet OLE doit être redimensionné automatiquement. |
| SourceFullName        | string  | obligatoire | Fichier source (par exemple, image ou graphique) de l’OLE. |
| UpperLeftRow          | integer | obligatoire | Index de ligne (à partir de 0) du coin supérieur gauche.   |
| UpperLeftColumn       | integer | obligatoire | Index de colonne (à partir de 0) du coin supérieur gauche. |
| Left                  | integer | facultatif  | Décalage horizontal, en points, par rapport au coin supérieur gauche. |
| Top                   | integer | facultatif  | Décalage vertical, en points, par rapport au coin supérieur gauche. |
| Width                 | integer | obligatoire | Largeur de l’objet OLE, en points.                         |
| Height                | integer | obligatoire | Hauteur de l’objet OLE, en points.                         |

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Réponses d’erreur

| Statut HTTP | Code | Message                                                                 |
| ----------- | ---- | ----------------------------------------------------------------------- |
| 400         | 4000 | Requête incorrecte – paramètres manquants ou non valides.               |
| 401         | 4010 | Non autorisé – jeton JWT invalide ou manquant.                          |
| 404         | 4040 | Introuvable – le classeur, la feuille de calcul ou l’objet OLE n’existe pas. |
| 500         | 5000 | Erreur interne du serveur – échec inattendu côté serveur.               |

L’API renvoie également un champ personnalisé **Code** dans le corps de la réponse, qui correspond au statut HTTP (par exemple, 200 → 2000, 400 → 4000, etc.).

## Quand utiliser cette API ?

Utilisez ce point de terminaison lorsque vous devez modifier un objet OLE existant — par exemple, une image, un graphique ou un document intégré — sans avoir à réimporter l’ensemble de la feuille de calcul. Les scénarios typiques incluent la mise à jour de la source de l’image, le redimensionnement de l’objet ou le changement de sa position après la génération du classeur. Pour des opérations connexes, voir [Ajouter un objet OLE](/oleobjects/add/) et [Supprimer un objet OLE](/oleobjects/delete/).

## Famille de SDK Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer. Un SDK abstractise les détails de bas niveau afin que vous puissiez vous concentrer sur votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Voici un court exemple en C# qui met à jour un objet OLE à l’aide du SDK Aspose.Cells Cloud :

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<votre-app-sid>",
    AppKey = "<votre-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Statut : {response.Status}");
```

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}