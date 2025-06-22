---
title: Konvertiert die Datei Excel in ein anderes Format
second_title: Aspose.Cells Cloud Documen
linktitle: Holen Sie sich Exce
type: docs
url: /de/get different formats files/
aliases: [/export-excel-workbook-to-different-file-formats/, /export-different-formats/]
keywords: Get excel files to kinds of format files
description: Aspose.Cells Cloud REST API unterstützt die Konvertierung von Excel-Dateien in verschiedene Formate. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Ruft Excel Datei in andere Formate ab
---
Dieser REST API gibt an, dass die Excel-Datei `get` eine Datei in einem anderen Format ist.

**Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Format|Schnur|Das Dateiformat: csv, xls, html, mhtml, ods, pdf, xml, txt, tiff, xlsb, xlsm, xlsx, xltm, xltx, xps, png, jpg, gif, emf, bmp, md, Numbers, wmf, svg usw.|
|Passwort|Schnur|Das zum Öffnen einer Excel-Datei erforderliche Kennwort.|
|isAutoFit|Schnur|Passt die Zeilen- und Spaltenbreite in dieser Arbeitsmappe automatisch an. Der Standardwert ist „false“.|
|onlySaveTable|Schnur|wahr/falsch|
|Ausgangspfad|Schnur| Pfad zum Speichern des Ergebnisses. Handelt es sich um eine einzelne Datei, sollte `outPath` sowohl den Dateinamen als auch die Erweiterung umfassen. Bei mehreren Dateien sollte `outPath` nur den Ordner enthalten.|
|outStorageName|Schnur| Der Speichername, in dem sich die gespeicherte Datei befindet.|
|checkExcelRestriction|bool| Ob die Einschränkung der Excel-Datei überprüft wird, wenn der Benutzer zellenbezogene Objekte ändert.|
|Region|Schnur| Die regionalen Einstellungen für die Arbeitsmappe.|
|SeitenbreiteAnpassungAufProBlatt|bool| Die Seitenbreite passt auf das Arbeitsblatt.|
|Seite hoch, passend für Blattgröße|bool| Die Seitenhöhe passt auf das Arbeitsblatt.|
|eineSeiteProBlatt|bool| Bei der Konvertierung in das Format PDF eine Seite pro Blatt.|
|Ordner|Schnur|Original-Arbeitsmappenordner.|
|Speichername|Schnur|Der Name des Speicherorts, an dem sich die Datei befindet.|

## REST API

|**API**|**Typ**|**Beschreibung**|**Swagger-Link**|
|:- |:- |:- |:- |
|/Zellen/{Name}|ERHALTEN|Exportiert die Arbeitsmappe in ein anderes Format.|[GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)|

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

 Sie können**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="1" tabID="11" tabName11="Request" >}}

{{< tab tabNum="11" >}}

```bash

curl -X PUT "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
