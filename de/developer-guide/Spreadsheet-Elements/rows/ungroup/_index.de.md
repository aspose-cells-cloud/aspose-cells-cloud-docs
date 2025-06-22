---
title: Gruppierung von Zeilen in einem Excel-Arbeitsblatt aufheben
second_title: Aspose.Cells Cloud Documen
linktitle: Ungrou
type: docs
url: /de/rows/ungroup/
aliases: [/ungroup-rows-in-excel-worksheet/]
keywords: Ungroup rows on an Excel worksheet
description: Aspose.Cells Cloud REST API unterstützt das Aufheben der Gruppierung von Zeilen in einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 70
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Zeilengruppierung auf einem Excel Arbeitsblatt aufheben
---
Dieser REST API gibt an, dass die Gruppierung von Zeilen in einem Excel-Arbeitsblatt aufgehoben werden soll.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
 
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Der Name der Arbeitsmappe.|
| Blattname| Schnur| Weg| Der Arbeitsblattname.|
| ersterIndex| ganze Zahl| Abfrage| Der erste zu bearbeitende Zeilenindex.|
| letzterIndex| ganze Zahl| Abfrage| Der letzte zu bearbeitende Zeilenindex.|
| istAlles| Boolescher Wert| Abfrage| Sollen alle Reihen bedient werden|
| Ordner| Schnur| Abfrage| Der Dokumentenordner.|
| Speichername| Schnur| Abfrage| Speichername.|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
-X POST \
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

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}
