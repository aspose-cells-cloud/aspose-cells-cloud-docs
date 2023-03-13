---
title: Importieren Sie Daten ohne Verwendung von Speicher
second_title: Aspose.Cells Cloud Documen
linktitle: Importieren Sie Daten ohne Speicher
type: docs
url: /de/import/without-using-storage/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: REST API,  spreadsheets, excel, Import
description: Cells.Cloud API für Excel-Dateien importieren
weight: 10
---
Excel Datenimport ist ein komplexer Vorgang. Viele Faktoren tragen zur Komplexität bei und sollten daher während des Exportprozesses berücksichtigt werden. Die Möglichkeit, verschiedene Formate und Datentypen in präziser professioneller Qualität in die Datei zu importieren, ist ein Top-Feature von Aspose.Cells Cloud.

Dieser REST API gibt `import data` in einer Excel-Datei an.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/import

```

**Die Anforderungsparameter sind:** 
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Datei| Datei| Formulardaten| Datei zum Hochladen|
| ImportOption| Importoptionen| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

**Die Parameter der Importdatenoptionen**sind darin beschrieben[der Referenzlink](/cells/de/import/#import-data-option-parameter).




 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LiteCells/PostImport) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.
 
Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/import" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
-F 'ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}'
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
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
 
 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}

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

{{< /tab >}}

{{< /tabs >}}
