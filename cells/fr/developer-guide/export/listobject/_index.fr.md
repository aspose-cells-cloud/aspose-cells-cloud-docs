---
title: Exporter un objet de liste
second_title: Aspose.Cells Cloud Documen
linktitle: Liste d'objets
type: docs
url: /fr/export/excel-listobject-to-different-formats/
keywords: Export Excel list object to kinds of format files
description: Aspose.Cells Cloud REST API prend en charge l'exportation d'objets de liste Excel vers des types de fichiers de format. SDK prend en charge les types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift
weight: 20
---
 Vous pouvez exporter des formats :[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [VST](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [SAO](https://docs.fileformat.com/spreadsheet/ods/), [SMS](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NOMBRES](https://docs.fileformat.com/spreadsheet/numbers/), [FOD](https://docs.fileformat.com/spreadsheet/fods/)..

- **REPOS API**

|**API**|**Taper**|**Description**|**Lien fanfaron**|
|:- |:- |:- |:- |
|/cellules/exporter|POSTE|Exporter Excel du contenu de la demande vers un certain format|[Post-exportation](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)|


 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) définit une interface de programmation accessible au public et permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.



- **Demande**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Réponse**

```bash
{
    "Files": [{
        "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
        "FileSize": 390,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
        "FileSize": 10040,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
        "FileSize": 382,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **Famille SDK Cloud**

 L'utilisation d'un SDK est le meilleur moyen d'accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Référentiel GitHub](https://github.com/aspose-cells-cloud) pour obtenir la liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-shape-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export-shape-tiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< /tabs >}}
