---
title: Fügen Sie eine Form auf einem Arbeitsblatt Excel hinzu
second_title: Aspose.Cells Cloud Documen
linktitle: Anzeige
type: docs
url: /de/shapes/add/
aliases: [/add-a-shape-inside-the-worksheet/]
keywords: Add shape on an Excel workshee
description: Aspose.Cells Cloud REST API unterstützt das Hinzufügen von Formen zu einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 30
---
Dieser REST API gibt an, eine Form zu einem Excel-Arbeitsblatt hinzuzufügen.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
 
```
 Die Anforderungsparameter sind:
 
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Zeichenfolge| Weg| Dokumentname.|
| Blattname| Zeichenfolge| Weg| Arbeitsblattname.|
| FormDTO|| Körper||
| Zeichnungstyp| Zeichenfolge| Abfrage| Formobjekttyp|
| UpperLeftRow| ganze Zahl| Abfrage| Zeilenindex oben links.|
| UpperLeftColumn| ganze Zahl| Abfrage| Spaltenindex oben links.|
| Spitze| ganze Zahl| Abfrage| Stellt den vertikalen Versatz des Spinners von seiner linken Zeile in Pixeleinheiten dar.|
| links| ganze Zahl| Abfrage| Stellt den horizontalen Versatz des Spinners von seiner linken Spalte in Pixeleinheiten dar.|
| Breite| ganze Zahl| Abfrage| Stellt die Höhe des Spinners in Pixeleinheiten dar.|
| Höhe| ganze Zahl| Abfrage| Stellt die Breite des Spinners in Pixeleinheiten dar.|
| Ordner| Zeichenfolge| Abfrage| Ordner des Dokuments.|
| Speichername| Zeichenfolge| Abfrage| Speichername.|
 
 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht die Durchführung von REST-Interaktionen direkt über einen Webbrowser.
 
Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie man mit cURL Anrufe zur Cloud API tätigt.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-Familie
 
 Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich die an[GitHub-Repository](https://github.com/aspose-cells-cloud) Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie hier.
 
Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:
 
 
{{< tabs tabTotal="5" tabID="4" tabName1="C#" tabName2="Java" tabName3="Perl" tabName4="Go" tabName5="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-PutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example-PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "34f478cae8c02848db0e376bd592a087" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f342d1e6f85982e0429fcd9bed8b11a8" "Example-PutWorksheetShape.swift" >}}

{{< /tab >}}

{{< /tabs >}}
