﻿---
title: Hintergrund in Workboo hinzufügen
second_title: Aspose.Cells Cloud Documen
linktitle: Anzeige
type: docs
url: /de/workbook/background/add/
aliases: [/add-background-in-workbook/,/workbook/add-background/]
keywords: Add background on an Excel workbook
description: Aspose.Cells Cloud REST API unterstützt das Hinzufügen von Hintergrundinformationen zu einer Excel-Arbeitsmappe in einer Excel-Datei. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 160
---
Dieser REST API gibt an, dass `background` zu einer Excel-Arbeitsmappe hinzugefügt werden soll.


**Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Bildpfad|Schnur|Bildposition.|
|Ordner|Schnur|Ursprünglicher Arbeitsmappenordner.|
|Speichername|Schnur|Speichername.|

**Body-Parameter anfordern**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Datendatei| Datendatei|Die Datendatei wird im Anfragetext gespeichert.|

## REST API

|**API**|**Typ**|**Beschreibung**|**Ressourcen-Link**|
|:- |:- |:- |:- |
|/cells/{Name}/Hintergrund|SETZEN|Hintergrund in Excel-Datei hinzufügen|[PutWorkbookBackground](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.

 Sie können verwenden**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.

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

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="Python" tabName4="Android" tabName5="Perl" tabName6="Ruby" tabName7="PHP" tabName8="Node.js" tabName9="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "4f5e06ec874b8b698dfa0e5359c85f96" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "b47350fc841e7c7e8889b1f57723ad94" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "bef09b36e0e7b769022bd810898dbd73" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "a984b922e2a7373755fb877e8754452b" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "7b9fa1a76c49c164d034342a2a59d4e0" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "a56d3fa3fff9c61191ee3e869ec51cdd" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "4a63cab36bb9f03e4e58bc30267b60b8" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4009896954c23f8a1394b3757a30ee9d" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "d3b449b5e5e2cdbb25da9e8de37bdccc" >}}

{{< /tab >}}

{{< /tabs >}}
