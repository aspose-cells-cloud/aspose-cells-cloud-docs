---
title: "Exporter une zone de feuille de calcul en PNG, PDF, CSV – Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "Zone"
type: docs
url: /fr/worksheets/area-to-different-formats/
aliases: [  /fr/get-worksheet-for-area/ ]
keywords: "Aspose.Cells, exporter une zone de feuille de calcul, PNG, PDF, CSV, conversion Excel, API REST, SDK"
description: "Découvrez comment exporter une plage de cellules spécifique d'une feuille de calcul Excel vers PNG, PDF, CSV et plus de 20 autres formats à l'aide de l'API REST Aspose.Cells Cloud ou des SDK (C#, Java, Python, …)."
weight: 230
ArticleTitle: "Exporter une zone de feuille de calcul en PNG, PDF, CSV à l'aide de l'API Aspose.Cells Cloud – Guide complet"
---

L'API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) permet de convertir une zone spécifiée d'une feuille de calcul en divers formats de fichiers. Les formats pris en charge : [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Ce guide explique comment exporter une **plage de cellules spécifique** d'une feuille de calcul Excel vers PNG, PDF, CSV et plus de 20 autres formats à l'aide de l'API Aspose.Cells Cloud. Pour des opérations connexes telles que l'exportation d'une feuille de calcul complète ou la conversion d'un classeur entier, consultez les pages **[Exporter une feuille de calcul complète](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** et **[Convertir un classeur en PDF](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)**.

## API REST

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

### Paramètres de la requête

| Paramètre               | Type   | Obligatoire | Description                                         |
|-------------------------|--------|-------------|-----------------------------------------------------|
| `name`                  | string | Oui         | Nom du fichier de classeur.                         |
| `sheetName`             | string | Oui         | Nom de la feuille de calcul cible.                 |
| `format`                | string | Oui         | Format de sortie souhaité (png, pdf, csv, etc.).   |
| `area`                  | string | Non         | Plage de cellules à exporter (par ex., `B3:K8`).    |
| `verticalResolution`    | int    | Non         | Résolution verticale en DPI pour les formats rastérisés. |
| `horizontalResolution`  | int    | Non         | Résolution horizontale en DPI pour les formats rastérisés. |
| `folder`                | string | Non         | Dossier dans le stockage cloud contenant le fichier. |
| `storage`               | string | Non         | Nom du service de stockage.                         |

### Réponse réussie

* **200 OK** – Retourne le fichier demandé en binaire (PNG, PDF, CSV, etc.).

### Réponses d’erreur

| Code d’état | Description                                           |
|-------------|-------------------------------------------------------|
| 400         | Requête incorrecte – paramètres manquants ou invalides. |
| 401         | Non autorisé – jeton d’authentification manquant ou invalide. |
| 404         | Non trouvé – le classeur ou la feuille de calcul spécifié n’existe pas. |
| 500         | Erreur interne du serveur – condition inattendue sur le serveur. |

**Exemple de charge utile d’erreur**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "Le paramètre 'area' est mal formé. Format attendu : B3:K8."
  }
}
```

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API cloud à l’aide de cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton jwt>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Image convertie (PNG binaire)

{{< /tab >}}

{{< /tabs >}}

## Famille de SDK Cloud

Utiliser un SDK est le moyen le plus rapide de développer. Un SDK abstrait les détails de bas niveau, vous permettant de vous concentrer sur la logique de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}