﻿---
title: Hintergrund in Workboo hinzufügen
second_title: Aspose.Cells Cloud Documen
linktitle: Anzeige
type: docs
url: /de/add-background-in-excel-file/
aliases: [/add-background-in-workbook/,/workbook/add-background/,/workbook/background/add/]
keywords: Add background on an Excel workbook
description: Aspose.Cells Cloud REST API unterstützt das Hinzufügen von Hintergrundinformationen zu einer Excel Arbeitsmappe in einer Excel Datei. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 160
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Hintergrund in Arbeitsmappe hinzufügen
---
Dieser REST API gibt an, `background` zu einer Excel-Arbeitsmappe hinzuzufügen.

**Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Bildpfad|Schnur|Bildposition.|
|Ordner|Schnur|Original-Arbeitsmappenordner.|
|Speichername|Schnur|Speichername.|

**Anforderungstextparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Datendatei| Datendatei|Die Datendatei wird im Anforderungstext gespeichert.|

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcenlink**|
|:- |:- |:- |:- |
|/Zellen/{Name}/Hintergrund|SETZEN|Hintergrund in Excel-Datei hinzufügen|[PutWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

 Sie können**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

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

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
