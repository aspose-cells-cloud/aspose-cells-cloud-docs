---
title: "Exporter une page de feuille de calcul – Référence de l'API Aspose.Cells Cloud"
ArticleTitle: "Exporter une page de feuille de calcul – Référence de l'API Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Page"
type: docs
url: /worksheets/page-to-different-formats/
aliases: [/get-worksheet-for-page-index/]
keywords: "Aspose.Cells Cloud, exportation de page de feuille de calcul, PDF, PNG, CSV, API REST, authentification JWT, formats de fichiers"
description: "Découvrez comment exporter une page spécifique d'une feuille de calcul vers PDF, PNG, CSV, et bien plus encore à l'aide de l'API REST Aspose.Cells Cloud. Inclut une requête cURL, un guide des paramètres et des exemples de SDK pour plusieurs langages."
weight: 240
---

L’exportation d’une page spécifique d’une feuille de calcul est utile lorsque vous avez besoin d’une version imprimable d’un rapport, d’une image de graphique ou d’un extrait de données, sans avoir à télécharger l’ensemble du classeur. Ce point de terminaison vous permet d’obtenir une seule page dans le format le mieux adapté à votre flux de travail en aval.

L’API [GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) permet de convertir une page spécifique d’une feuille de calcul en divers formats de fichiers. Formats pris en charge : [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API REST

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) définit une interface de programmation accessible publiquement et vous permet d’effectuer des interactions REST directement depuis un navigateur web.

> **Prérequis** – Vous devez disposer d’un jeton d’authentification JWT valide et du classeur stocké dans un dossier cloud spécifié via le paramètre `folder`.

Vous pouvez utiliser l’outil en ligne de commande cURL pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment effectuer un appel à l’API Cloud avec cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Requête" tabName2="Réponse" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jeton JWT>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Réponse** – Le service renvoie la page demandée dans le format choisi. Pour les formats d’image (png, jpeg, gif, etc.), le corps contient l’image binaire ; pour les formats de document (pdf, xls, csv, etc.), le corps contient le contenu du fichier. Une requête réussie renvoie le code HTTP 200.

*Exemple de réponse PNG (extraire base64 tronqué) :*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Paramètres**

| Paramètre              | Type    | Description                                                             | Valeur par défaut |
| ---------------------- | ------- | ----------------------------------------------------------------------- | ----------------- |
| `format`               | string  | Format de fichier de sortie (par ex. `pdf`, `png`, `csv`).             | `pdf`             |
| `verticalResolution`   | integer | Résolution verticale (DPI) de l’image rendue.                          | `100`             |
| `horizontalResolution` | integer | Résolution horizontale (DPI) de l’image rendue.                        | `100`             |
| `pageIndex`            | integer | Index de page de la feuille de calcul à exporter (index à zéro ; `0` = première page). | `0`               |
| `folder`               | string  | Dossier de stockage cloud où réside le classeur source.                | —                 |

**Codes de statut HTTP**

| Code | Signification               | Description                                                      |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Mauvaise requête            | Paramètres manquants ou non valides (par ex. type de fichier non pris en charge). |
| 401  | Non autorisé                | Jeton JWT invalide ou manquant.                                  |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la limite de taille.            |
| 500  | Erreur interne du serveur   | Erreur serveur inattendue.                                       |

**Erreurs possibles**

- **401 Non autorisé** – Jeton JWT invalide ou manquant.
- **404 Non trouvé** – Le classeur ou la feuille de calcul spécifié n’existe pas.
- **400 Mauvaise requête** – Valeur de paramètre non valide (par ex. `format` non pris en charge).
- **500 Erreur interne du serveur** – Problème inattendu côté serveur.

## Famille de SDK Cloud

L’utilisation d’un SDK est le moyen le plus efficace d’accélérer le développement. Un SDK gère les détails de bas niveau, vous permettant ainsi de vous concentrer sur les tâches de votre projet. Veuillez consulter le [dépôt GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Aspose.Cells Cloud.

Les exemples de code suivants illustrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}