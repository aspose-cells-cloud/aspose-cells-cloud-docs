---
title: Teilen Sie eine Excel-Arbeitsmappe in mehrere Dateien auf
second_title: Aspose.Cells Cloud Documen
linktitle: Arbeitsboom
type: docs
url: /de/workbook/split/
aliases: [/split-excel-workbooks/]
keywords: Split an Excel workbook to multi-files
description: Aspose.Cells Cloud REST API unterstützt das Aufteilen einer Excel Arbeitsmappe in mehrere Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 130
---
Dieser REST API gibt an, einen Excel `workbook` in mehrere Dateien mit unterschiedlichem Format aufzuteilen.

**Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Format|Schnur|Geteiltes Format.|
|aus|ganze Zahl|Arbeitsblattindex starten.|
|Zu|ganze Zahl|Arbeitsblattindex beenden.|
|horizontale Auflösung|ganze Zahl|Horizontale Bildauflösung.|
|vertikale Auflösung|ganze Zahl|Vertikale Bildauflösung.|
|outFolder|Schnur|Position der aufgeteilten Datei ausgeben.|
|splitNameRule|Schnur||
|Ordner|Schnur|Ursprünglicher Arbeitsmappenordner.|
|Speichername|Schnur|Speichername.|


## REST API

|**API**|**Typ**|**Beschreibung**|**Swagger-Link**|
|:- |:- |:- |:- |
|/cells/{name}/split|POST|Teilen Sie eine Excel-Arbeitsmappe|[PostWorkbookSplit](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.

 Sie können verwenden**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Result": {

    "Documents": [

      {

        "Id": 1,

        "link": {

          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",

          "Rel": null,

          "Title": null,

          "Type": null

        }

      }

    ]

  },

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-SplitWorkbooks-split-excel-workbooks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostWorkbookSplit-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-split_workbook-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SplitExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-SplitWorkbooks-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-SplitWorkbooks-split-excel-workbooks.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-SplitWorkbooks-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "ec45ec662143f4c94c2a8bc8c95953ce" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "6ddbdc7793cac6e13ad09bbfbc44a614" >}}

{{< /tab >}}

{{< /tabs >}}
