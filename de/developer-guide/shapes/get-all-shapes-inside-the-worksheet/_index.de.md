---
title: Holen Sie sich alle Formen auf einem Excel Arbeitsblatt
second_title: Aspose.Cells Cloud Documen
linktitle: Hol's dir
type: docs
url: /de/shapes/get-all/
aliases: [/get-all-shapes-inside-the-worksheet/]
keywords: Get all shapes on an Excel workshee
description: Aspose.Cells Cloud REST API unterstützt das Abrufen aller Formen auf einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Alle Formen auf einem Excel Arbeitsblatt abrufen
---
 Dieser REST API zeigt an, Arbeitsblattformen abrufen
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Arbeitsblattname.|
| Ordner| Schnur| Abfrage| Ordner des Dokuments.|
| Speichername| Schnur| Abfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShapes) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.
 
Mit dem Befehlszeilentool cURL können Sie ganz einfach auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Anrufe an Cloud API tätigen.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash

{

  "Shapes" : {

    "ShapeList" : [

      {

        "link" : {

          "Href" : "/0",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/1",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/2",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      },

      {

        "link" : {

          "Href" : "/3",

          "Rel" : "self",

          "Type" : null,

          "Title" : null

        }

      }

    ],

    "link" : {

      "Href" : "http://api.aspose.com/v1.1/cells/sampleShapes.xlsx/worksheets/Sheet1/shapes",

      "Rel" : "self",

      "Type" : null,

      "Title" : null

    }

  },

  "Code" : 200,

  "Status" : "OK"

}
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte lesen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
 
Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-GetWorksheetShapes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-GetWorksheetShapes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-GetWorksheetShapes.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "2118580a8c2f08f37269d89ff9f57781" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-GetWorksheetShapes.swift" >}}

{{< /tab >}}

{{< /tabs >}}
