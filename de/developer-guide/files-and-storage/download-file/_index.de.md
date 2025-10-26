---
title: Datei von Aspose.Cells AP herunterladen
second_title: Developer Guide for Aspose.Cells AP
linktitle: Datei AP herunterladen
type: docs
url: /de/download-file/
keywords: Aspose.Cells API, Download File, REST API, Excel File, Office Cloud, Spreadsheet Download, File Management, File Retrieval, CSV, PDF, JSON, Markdow
description: Erfahren Sie, wie Sie mit Aspose.Cells API Dateien wie Excel, PDF, CSV und effizienter herunterladen können
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Download Excel Datei, Abrufen Blank Cells
---
## **Excel API: Datei herunterladen**

```
GET http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Funktionsbeschreibung**

 Der**Datei herunterladen** Mit API können Sie im Cloud-Speicher Aspose gespeicherte Dateien abrufen. Diese Funktion ist für die Verwaltung und den Zugriff auf verschiedene Dateiformate, einschließlich Excel Tabellenkalkulationen, PDFs und CSVs, unerlässlich.

###  Die Anfrageparameter von**Datei herunterladen** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Weg| Zeichenfolge| Weg| Der Pfad zur Datei, die Sie herunterladen möchten.|
| Speichername| Zeichenfolge| Abfrage| Der Name des Speichers, aus dem die Datei abgerufen wird.|
| Versions-ID| Zeichenfolge| Abfrage| Die Versionskennung der herunterzuladenden Datei, falls zutreffend.|

### **Antwortbeschreibung**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung. Ein SDK verarbeitet grundlegende Details und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
