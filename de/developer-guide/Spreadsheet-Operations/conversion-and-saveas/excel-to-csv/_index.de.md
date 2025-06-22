---
title: Excel an CS
second_title: Aspose.Cells Cloud Documen
linktitle: Excel an CS
type: docs
url: /deconvert-excel-file-to-csv-file/
aliases: [/convert-excel-file-to-csv-in-cloud/,/convert/excel-to-csv/,/convert-excel-file-to-csv-file/]
keywords: Convert excel files to csv files
description: Aspose.Cells Cloud REST API unterstützt die Konvertierung von Excel-Dateien in CSV-Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift.
weight: 90
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Excel zu CSV
---
Dieser REST API gibt an, `convert` eine Tabellenkalkulationsdatei in eine Datei im CSV-Format umzuwandeln.

**Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Passwort|Schnur| Das zum Öffnen einer Excel-Datei erforderliche Kennwort.|
|Speichername|Schnur| Der Name des Speicherorts, an dem sich die Datei befindet.|
|checkExcelRestriction|bool| Ob die Einschränkung der Excel-Datei überprüft wird, wenn der Benutzer zellenbezogene Objekte ändert.|

**Anforderungstextparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Datendatei| Datendatei|Die Datendatei wird im ersten Teil des mehrteiligen Inhalts gespeichert.|

**Antwort**

[Dateiinfo](/cells/de/file-info/)

## REST API Spezifikation

|**API**|**Typ**|**Beschreibung**|**Swagger-Link**|
|:- |:- |:- |:- |
|/Zellen/konvertieren/csv|POST|Konvertieren Sie eine Tabelle in eine CSV-Datei.|[PostConvertWorkbookToCSV](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV)|

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

 Sie können**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.csv",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um grundlegende Details und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPdf.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPdf.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPdf.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPdf.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPdf.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPdf.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPdf.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPdf.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andere APIs implementieren diese Funktion

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)Mit API können Sie die Datei MS Excel als CSV-Datei mit zusätzlichen Einstellungen speichern und das Ergebnis im Speicher speichern.

Diese REST API `convert` Excel-Datei in CSV.

[PUT /Zellen/Konvertieren](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) Mit API können Sie die Datei MS Excel mit zusätzlichen Einstellungen in eine CSV-Datei konvertieren und das Ergebnis in der Antwort speichern.

Diese REST API `export` Excel-Datei in CSV.

[GET /Zellen/{Name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) Mit API können Sie die Datei MS Excel mit zusätzlichen Einstellungen in eine CSV-Datei konvertieren und das Ergebnis in der Antwort speichern.
