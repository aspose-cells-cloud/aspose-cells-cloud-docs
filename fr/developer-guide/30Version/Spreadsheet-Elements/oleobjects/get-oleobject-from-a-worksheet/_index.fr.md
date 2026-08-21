---
title: "Récupérer un objet OLE à partir d'une feuille Excel – Aspose.Cells Cloud API"
second_title: "Documentation"
linktype: "Récupérer"
type: docs
url: /fr/oleobjects/get/
aliases: [/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, objet OLE, excel, feuille de calcul, récupérer un objet OLE, API REST"
description: "Récupérez un objet OLE (image, graphique ou fichier intégré) à partir d’une feuille de calcul à l’aide de l’API REST Aspose.Cells Cloud. Inclut le point de terminaison HTTPS, les paramètres requis, un exemple cURL et du code SDK dans plusieurs langues."
ArticleTitle: "Récupérer un objet OLE à partir d'une feuille Excel – Aspose.Cells Cloud API"
weight: 10
---

Cette API REST permet de récupérer un **objet OLE** à partir d'une feuille de calcul Excel.

## Sécurité et authentification
Les API Aspose.Cells Cloud sont sécurisées et nécessitent une [authentification basée sur un jeton JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement | Description                                                  |
| ---------------- | ------- | ----------- | ------------------------------------------------------------ |
| name             | string  | path        | Nom du document.                                             |
| sheetName        | string  | path        | Nom de la feuille de calcul.                                 |
| objectNumber     | integer | path        | Numéro de l'objet dans la feuille de calcul.                 |
| format           | string  | query       | Format d’export souhaité pour l’objet (par ex. `png`, `jpeg`). |
| folder           | string  | query       | Dossier contenant le document.                               |
| storageName      | string  | query       | Nom du stockage à utiliser.                                  |

### Options de stockage

- **folder** – spécifie le sous-dossier dans le stockage par défaut où se trouve le classeur.
- **storageName** – remplace le nom du stockage par défaut si le classeur est stocké ailleurs.

La [Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) définit une interface de programmation accessible publiquement et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour appeler le service web Aspose.Cells. L’exemple ci-dessous montre comment demander un objet OLE sous forme d’image PNG.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Réponse binaire (image)

Lorsque le paramètre `format` est défini sur un type d’image (par ex. `png`), l’API renvoie les données binaires de l’image avec l’en-tête :

```
Content-Type: image/png
```

_(Le fichier image est transmis en flux direct au client.)_

### Réponse JSON (méta-données)

Si `format` est omis ou défini sur `json`, l’API renvoie une charge utile JSON décrivant l’objet OLE :

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Réponses d’erreur

| Statut HTTP | Code d’erreur | Description                                      |
| ----------- | ------------- | ------------------------------------------------ |
| 400         | BadRequest    | Paramètres manquants ou non valides.             |
| 401         | Unauthorized  | Jeton JWT invalide ou manquant.                  |
| 404         | NotFound      | Classeur, feuille de calcul ou objet OLE introuvable. |
| 500         | ServerError   | Erreur serveur inattendue.                       |

**Exemple de réponse 404**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "L'objet OLE numéro 0 n'a pas été trouvé dans la feuille 'Sheet1'."
}
```

## Famille de SDK Cloud

Utiliser un SDK est la méthode la plus rapide pour intégrer l’API. Les SDK gèrent les détails de bas niveau afin que vous puissiez vous concentrer sur votre logique métier. Consultez le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}