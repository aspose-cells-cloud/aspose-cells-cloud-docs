---
title: Exportieren Sie Arbeitsmappen und interne Objekte in verschiedene Formate
second_title: Aspose.Cells Cloud Documen
linktitle: Expor
type: docs
url: /de/export/
keywords: Export workbook and internal objects to kinds of format files
description: Aspose.Cells Cloud REST API unterstützt den Export von Excel Dateien und internen Objekten in verschiedene Formatdateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 31
---
 Wenn Sie ursprünglich eine Excel-Datei in einem bestimmten Format erstellt haben, z[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , Und[CSV](https://docs.fileformat.com/spreadsheet/csv/) , kann es manchmal hilfreich sein, die Excel-Datei in ein anderes Format zu konvertieren, damit Sie die darin enthaltenen Sonderfunktionen nutzen können. Beispielsweise möchten Sie möglicherweise eine Excel-Datei exportieren[PDF](https://docs.fileformat.com/pdf/) um Ihre Inhalte vor unbefugten Änderungen zu schützen und das gleichzeitige Lesen und Teilen zu erleichtern.

 Excel Der Objektexport ist ein komplexer Prozess. Viele Faktoren tragen zur Komplexität bei und sollten daher beim Exportprozess berücksichtigt werden. Die Möglichkeit, Excel-Objekte in einer Formatdatei mit präziser professioneller Qualität zu exportieren, ist eine Top-Funktion von Aspose.Cells Cloud.

 Es funktioniert perfekt für Arbeitsmappen, Diagramme, Formen und Bilder, die aus einer Excel-Datei exportiert werden. Sie können folgende Formate exportieren:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) . Die Nur-Export-Formate:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [ZAHLEN](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Bei der Anfrage handelt es sich um eine HTTP-Anfrage mit mehrteiligem Inhalt (siehe[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)oder[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des mehrteiligen Inhalts enthält die Datendatei und der zweite Teil enthält Speicheroptionen.

Die REST API `export` Arbeitsmappe und interne Objekte in Dateien unterschiedlichen Formats.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| Formulardaten| Datei zum Hochladen|
| Objekttyp| Zeichenfolge| Abfrage|Objekttyp (Arbeitsmappe/Arbeitsblatt/Diagramm/Form/Bild/Listenobjekt/Oleobjekt)|
| Format| Zeichenfolge| Abfrage|[Datei Format](/cells/de/supported-file-formats/)  |
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie man mit cURL Anrufe zur Cloud API tätigt.
 
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
 
## Cloud SDK-Familie


 Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich die an[GitHub-Repository](https://github.com/aspose-cells-cloud) Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie hier.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:


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


Die folgenden Artikel erklären jeden API im Detail und enthalten cURL und SDK-Beispiele für jeden API:


1. [Exportieren Sie das Diagramm Excel in ein anderes Dateiformat](/cells/de/export/excel-chart-to-different-formats/)
2. [Exportieren Sie das Listenobjekt Excel in ein anderes Dateiformat](/cells/de/export/excel-listobject-to-different-formats/)
3. [Exportieren Sie das Ole-Objekt Excel in ein anderes Dateiformat](/cells/de/export/excel-ole-object/)
4. [Exportieren Sie das Bild Excel in ein anderes Dateiformat](/cells/de/export/excel-picture-to-different-formats/)
5. [Exportieren Sie die Form Excel in ein anderes Dateiformat](/cells/de/export/excel-shape-to-different-formats/)
6. [Exportieren Sie die Arbeitsmappe Excel in ein anderes Dateiformat](/cells/de/export/excel-to-different-formats/)
7. [Exportieren Sie das Arbeitsblatt Excel in ein anderes Dateiformat](/cells/de/export/excel-worksheet-to-different-formats//)
