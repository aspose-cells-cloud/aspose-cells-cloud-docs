---
title: "Exporter un classeur"
second_title: "Document"
linktitle: "Classeur"
type: docs
url: /export-excel-to-different-formats/
aliases: [/export/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, export Excel, conversion de classeur, PDF, CSV, JSON, formats d’image, API de feuille de calcul, XLSX, ODS, PNG"
description: "Guide pas à pas sur l’exportation de classeurs Excel vers plusieurs formats, notamment PDF, CSV, JSON et divers types d’images, à l’aide de l’API REST Aspose.Cells Cloud et des SDK."
weight: 20
---

Vous pouvez exporter des classeurs vers l’un des formats suivants : [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## API REST


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sécurité et authentification**

Les API Aspose.Cells Cloud sont sécurisées et nécessitent une <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">authentification basée sur un jeton JWT</a>.


### Paramètres de la requête

| Nom du paramètre | Type    | Emplacement (chemin / chaîne de requête / corps HTTP) | Obligatoire | Description |
|------------------|---------|--------------------------------------------------------|-------------|-------------|
| file             | fichier | formData                                               | Oui         | Fichier à télécharger |
| objectType       | string  | query                                                  | Oui         | Type d’objet à exporter. Pour l’exportation de graphiques, utilisez `chart`. Autres valeurs possibles : `worksheet`, `picture`, etc. |
| format           | string  | query                                                  | Oui         | Format de sortie souhaité. Valeurs prises en charge : `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |


### **Réponse**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**Codes d’état HTTP**

| Code | Signification         | Description |
|------|-----------------------|-------------|
| 200  | OK                    | Les formes ont été exportées avec succès ; la réponse contient la liste des fichiers. |
| 400  | Requête incorrecte    | Paramètres manquants ou non valides. |
| 401  | Non autorisé          | Jeton d’accès invalide ou manquant. |
| 413  | Charge utile trop volumineuse | Le fichier téléchargé dépasse la taille limite. |
| 500  | Erreur interne du serveur | Erreur inattendue du serveur. |


## Comment utiliser l’API PostExport avec les SDK

### Spécification de l’API PostExport


La [spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation accessible publiquement qui vous permet d’effectuer des interactions REST directement depuis un navigateur web.

Vous pouvez utiliser l’outil en ligne de commande **cURL** pour accéder facilement aux services web Aspose.Cells. L’exemple suivant montre comment appeler l’API Cloud à l’aide de cURL.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Utiliser les SDK Aspose.Cells Cloud

L’utilisation d’un SDK accélère le développement en gérant les détails de bas niveau, afin que vous puissiez vous concentrer sur la logique métier. Une liste complète des SDK Aspose.Cells Cloud est disponible dans le [dépôt GitHub](https://github.com/aspose-cells-cloud).

Les exemples de code suivants montrent comment appeler le service web Aspose.Cells à l’aide de divers SDK :

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}