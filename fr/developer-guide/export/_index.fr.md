﻿---
title: Exporter le classeur et les objets internes vers des types de formulaire
second_title: Aspose.Cells Cloud Documen
linktitle: Exportation
type: docs
url: /fr/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API prend en charge l'exportation de fichiers Excel et d'objets internes vers des types de fichiers de format. Le SDK prend en charge différents types de langages de développement. Ils incluent Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby et Swift.
weight: 31
kwords: Excel, Office Cloud, REST API, Feuille de calcul, PDF, CSV, Json, Markdwon, Exporter un classeur et des objets internes vers des types de format
---
 Si vous avez initialement créé un fichier Excel dans un certain format, comme[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , et[CSV](https://docs.fileformat.com/spreadsheet/csv/) vous trouverez parfois utile de convertir le fichier Excel dans un autre format afin de pouvoir profiter des fonctionnalités spéciales qu'il offre. Par exemple, vous souhaiterez peut-être exporter un fichier Excel vers[PDF](https://docs.fileformat.com/pdf/) pour protéger votre contenu de toute modification non autorisée et le rendre facile à lire et à partager simultanément.

 L'exportation d'objets Excel est un processus complexe. De nombreux facteurs contribuent à cette complexité et doivent donc être pris en compte lors du processus d’exportation. La possibilité d'exporter l'objet Excel vers un fichier au format unique avec une qualité professionnelle précise est l'une des principales fonctionnalités de Aspose.Cells Cloud.

 Il fonctionne parfaitement pour les classeurs, graphiques, formes et images exportés à partir d'un fichier Excel. Vous pouvez exporter les formats :[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [SAO](https://docs.fileformat.com/spreadsheet/ods/), [SMS](https://docs.fileformat.com/word-processing/txt/) . Les formats d'exportation uniquement :[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NOMBRES](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

La requête est une requête HTTP avec un contenu en plusieurs parties (voir[RFC2046](http://tools.ietf.org/html/rfc2046#page-17)ou[RFC1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La première partie du contenu en plusieurs parties contient le fichier de données et la seconde contient les options de sauvegarde.

Le classeur REST API `export` et les objets internes dans un fichier de format différent.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 Les paramètres de la requête sont :
 
| Le nom du paramètre| Taper| Chemin/Chaîne de requête/HTTPBody|Description|
|:- |:- |:- |:- |
| déposer| déposer| Données de formulaire| Fichier à télécharger|
| type d'objet| chaîne| requête| type d'objet (classeur/feuille de calcul/graphique/forme/image/listobject/oleobject)|
| format| chaîne| requête|[Format de fichier](/cells/fr/supported-file-formats/)  |
 
 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.
 
Vous pouvez utiliser l'outil de ligne de commande cURL pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers le Cloud API avec cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Famille de SDK Cloud


 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :


{{< tabs tabTotal="9" tabID="3" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" tabName10="C#" tabName11="Java" >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export.cs" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Export.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export.php" >}}


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

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsExport.py" >}}
{{< /tab >}}

{{< /tabs >}}


Les articles suivants expliquent chaque API en détail et contiennent des exemples de cURL et de SDK pour chaque API :


1. [Exporter le graphique Excel vers un format de fichier différent](/cells/fr/export/excel-chart-to-different-formats/)
2. [Exporter l'objet de liste Excel vers un format de fichier différent](/cells/fr/export/excel-listobject-to-different-formats/)
3. [Exporter l'objet ole Excel vers un format de fichier différent](/cells/fr/export/excel-ole-object/)
4. [Exporter l'image Excel vers un format de fichier différent](/cells/fr/export/excel-picture-to-different-formats/)
5. [Exporter la forme Excel vers un format de fichier différent](/cells/fr/export/excel-shape-to-different-formats/)
6. [Exporter le classeur Excel vers un format de fichier différent](/cells/fr/export/excel-to-different-formats/)
7. [Exporter la feuille de calcul Excel vers un format de fichier différent](/cells/fr/export/excel-worksheet-to-different-formats//)
