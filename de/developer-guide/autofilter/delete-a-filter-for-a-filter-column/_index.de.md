---
title: Löschen Sie einen Filter in einem Excel-Arbeitsblatt
second_title: Aspose.Cells Cloud Documen
linktitle: Filter löschen
type: docs
url: /de/delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/,/delete-auto-filter/]
keywords: Deletes a filter on an Excel worksheet
description: Die Aspose.Cells-Cloud API unterstützt das Löschen eines Filters auf einem Excel-Arbeitsblatt. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 100
---
Dieser REST API gibt an, dass ein `filter` auf einem Excel-Arbeitsblatt gelöscht werden soll.

## RSET API

```bash

DELETE http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter

```

Die Anforderungsparameter sind:
| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg|Der Name der Arbeitsmappe.|
| Tabellenname| Schnur| Weg| Der Arbeitsblattname.|
|Bereich|Schnur| Anfrage||
|FeldIndex|ganze Zahl| Anfrage||
|dateTimeGroupingType|Schnur| Anfrage| Tag/Stunde/Minute/Monat/Sekunde/Jahr|
|Jahr|ganze Zahl| Anfrage||
|Monat|ganze Zahl| Anfrage||
|Tag|ganze Zahl| Anfrage||
|Stunde|ganze Zahl| Anfrage||
|Minute|ganze Zahl| Anfrage||
|zweite|ganze Zahl| Anfrage||
|übereinstimmenBlanks|Schnur| Anfrage|wahr falsch|
|Aktualisierung|Schnur| Anfrage|wahr falsch|
|Ordner|Schnur| Anfrage|Ursprünglicher Arbeitsmappenordner.|
|Speichername|Schnur| Anfrage|Speichername.|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.

Sie können das cURL-Befehlszeilentool verwenden, um einfach auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash

curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&criteria=Year" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
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

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Worksheet-DeleteFilter-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-filters-DeleteFilterForFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-AutoFilter-DeleteWorksheetFilter-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-AutoFilter-delete_worksheet_filter-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-DeleteFilter-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "75ea6b5d2f6d82f9c2f9279fb37ebbdf" "Examples-Android-filters-DeleteFilterForFilterColumnExample-1.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-DeleteFilter-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "4e5d4702f8c09698ab20c1a577b259c9" >}}

{{< /tab >}}

{{< /tabs >}}
