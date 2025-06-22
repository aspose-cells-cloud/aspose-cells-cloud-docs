---
title: Clea
type: docs
url: /de/hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: Clear hyperlinks from an Excel worksheet
description: Aspose.Cells Cloud REST API unterstützt das Löschen von Hyperlinks aus einem Excel Arbeitsblatt. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 40
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Löschen
---
Dieser REST API weist auf einem Excel-Arbeitsblatt auf `delete all hyperlinks` hin.

## RSET API

```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
 
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg| Dokumentname.|
| Blattname| Schnur| Weg| Arbeitsblattname.|
| Ordner| Schnur| Abfrage| Der Dokumentenordner.|
| Speichername| Schnur| Abfrage| Speichername.|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Hypelinks/DeleteWorksheetHyperlinks) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}
