---
title: "Exporter une feuille de calcul – Aspose.Cells Cloud"
second_title: "Document"
linktitle: "Feuille de calcul"
type: docs
url: /fr/export-excel-worksheet-to-different-formats/
aliases: [  /fr/export/excel-worksheet-to-different-formats/ ]
keywords: "Aspose.Cells, exporter une feuille de calcul, API Excel, PDF, CSV, TIFF, ODS, formats d’image"
description: "Découvrez comment exporter une feuille de calcul Excel vers les formats PDF, CSV, TIFF et d’autres à l’aide de l’API REST Aspose.Cells Cloud. Inclut un exemple cURL, les exigences d’authentification, les détails des paramètres et la gestion des réponses."
weight: 20
ArticleTitle: "Exporter une feuille de calcul Excel vers divers formats – Aspose.Cells Cloud"
---

Vous pouvez exporter une feuille de calcul vers les formats suivants :

- **XLS** – [Détails du format XLS](https://docs.fileformat.com/spreadsheet/xls/)
- **XLSX** – [Détails du format XLSX](https://docs.fileformat.com/spreadsheet/xlsx/)
- **XLSB** – [Détails du format XLSB](https://docs.fileformat.com/spreadsheet/xlsb/)
- **CSV** – [Détails du format CSV](https://docs.fileformat.com/spreadsheet/csv/)
- **TSV** – [Détails du format TSV](https://docs.fileformat.com/spreadsheet/tsv/)
- **XLSM** – [Détails du format XLSM](https://docs.fileformat.com/spreadsheet/xlsm/)
- **ODS** – [Détails du format ODS](https://docs.fileformat.com/spreadsheet/ods/)
- **TXT** – [Détails du format TXT](https://docs.fileformat.com/word-processing/txt/)
- **PDF** – [Détails du format PDF](https://docs.fileformat.com/pdf/)
- **OTS** – [Détails du format OTS](https://docs.fileformat.com/spreadsheet/ots/)
- **XPS** – [Détails du format XPS](https://docs.fileformat.com/page-description-language/xps/)
- **DIF** – [Détails du format DIF](https://docs.fileformat.com/spreadsheet/dif/)
- **PNG** – [Détails du format PNG](https://docs.fileformat.com/Image/png/)
- **JPEG** – [Détails du format JPEG](https://docs.fileformat.com/image/jpeg/)
- **BMP** – [Détails du format BMP](https://docs.fileformat.com/image/bmp/)
- **SVG** – [Détails du format SVG](https://docs.fileformat.com/page-description-language/svg/)
- **TIFF** – [Détails du format TIFF](https://docs.fileformat.com/image/tiff/)
- **EMF** – [Détails du format EMF](https://docs.fileformat.com/image/emf/)
- **NUMBERS** – [Détails du format Numbers](https://docs.fileformat.com/spreadsheet/numbers/)
- **FODS** – [Détails du format FODS](https://docs.fileformat.com/spreadsheet/fods/)

[Découvrez d’autres opérations d’export associées, telles que l’export d’un classeur complet ou d’un graphique.](https://docs.aspose.cloud/cells/export-excel-workbook-to-different-formats/)

## API PostExport

```http
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.

### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Obligatoire | Description                                                                 |
|------------------|---------|--------------------------------------------------------|-------------|------------------------------------------------------------------------------|
| file             | fichier | formData                                               | Oui         | Fichier à téléverser                                                        |
| objectType       | chaîne  | query                                                  | Oui         | Type d’objet à exporter. Pour l’export d’un graphique, utilisez `chart`. Les autres valeurs possibles sont `worksheet`, `picture`, etc. |
| format           | chaîne  | query                                                  | Oui         | Format de sortie souhaité. Valeurs prises en charge : `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### Réponse

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet3.tif",
      "FileSize": 2824,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4.tif",
      "FileSize": 1350,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet5.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet7.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet4.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

### **Gestion des erreurs**

En cas d’échec de la requête, l’API renvoie un objet d’erreur JSON contenant des champs tels que `Code` et `Message`. Les codes d’état HTTP typiques incluent **401 Unauthorized** (jeton manquant ou invalide) et **400 Bad Request** (paramètres invalides).

**Codes d’état HTTP**

| Code | Signification               | Description                                                           |
|------|-----------------------------|------------------------------------------------------------------------|
| 200  | OK                          | Filtre appliqué avec succès ; la réponse contient les détails de l’opération. |
| 400  | Bad Request                 | Paramètres manquants ou invalides (par ex., type de fichier non pris en charge). |
| 401  | Unauthorized                | Jeton JWT invalide ou manquant.                                        |
| 413  | Payload Too Large           | Le fichier téléversé dépasse la taille limite.                        |
| 500  | Internal Server Error       | Erreur serveur inattendue.                                             |

**Notes**

- La taille maximale autorisée pour le téléchargement est de 50 Mo.  
- L’API permet d’exporter plusieurs feuilles de calcul en une seule requête ; chaque feuille est renvoyée sous forme d’un fichier distinct dans le tableau `Files`.  
- Le traitement asynchrone est disponible pour les grands classeurs ; utilisez le code de réponse `202 Accepted` pour interroger l’état de l’opération.

## Comment utiliser l’API PostExport avec les SDK

### Prérequis

Avant d’appeler l’API, obtenez un jeton d’accès JWT valide à l’aide du flux d’authentification Aspose.Cells Cloud. Assurez-vous que ce jeton est inclus dans l’en-tête `Authorization` de chaque requête. Les SDK gèrent automatiquement l’acquisition du jeton une fois configurés avec vos identifiants client.

### Spécification de l’API PostExport

La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation publiquement accessible et permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud avec cURL.

```bash
# Exporter une feuille de calcul au format TIFF
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=worksheet&format=tiff" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -F "File=@MyWorkbook.xlsx"
```

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK est la méthode la plus rapide pour développer avec Aspose.Cells Cloud. Un SDK masque les détails de bas niveau, vous permettant de vous concentrer sur votre logique métier. Pour obtenir la liste complète des SDK pris en charge, veuillez visiter le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment appeler les services web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}
---