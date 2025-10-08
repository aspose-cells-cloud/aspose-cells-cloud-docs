---
title: Datei auf Aspose Handy hochladen
second_title: Developer Guide for File Uploa
linktitle: Datei hochladen
type: docs
url: /de/upload-file/
keywords: Aspose, file upload, Excel API, Office Cloud, REST API, Spreadsheet, PDF, CSV, JSON, Markdown, upload Excel files, match blank cell
description: Umfassende Anleitung zum Hochladen von Dateien mit Aspose Cells API, einschließlich Parameter und Antwortstruktur
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen, Datei hochladen
---
## **Aspose Cells API: Datei hochladen**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Funktionsbeschreibung**

 Der**Datei hochladen** API ermöglicht Entwicklern, Dateien direkt in den Cloud-Speicher hochzuladen, um sie mit Aspose Cells zu verarbeiten.

###  Die Anfrageparameter von**Datei hochladen** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Dateien hochladen| Datei| FormData|Laden Sie Dateien in den Cloud-Speicher hoch.|
| Weg| Zeichenfolge| Weg| Der Zielpfad im Cloud-Speicher. Geben Sie den Pfad an, in den die Datei hochgeladen werden soll.|
| Speichername| Zeichenfolge| Abfrage| Der Name des Speichers, in den die Datei hochgeladen wird.|

### **Antwortbeschreibung**

```json
{
  "Name": "FilesUploadResult",
  "Description": [
    "File upload result"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": [
        "List of uploaded file names"
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": [
        "List of errors."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/UploadFile) bietet eine detaillierte Beschreibung von API und ermöglicht Entwicklern, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

## Aspose Cells API SDK

 Die Verwendung eines SDK steigert die Entwicklungseffizienz durch die Verwaltung von Details auf niedriger Ebene und ermöglicht es Entwicklern, sich auf Projektaufgaben zu konzentrieren. Besuchen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine umfassende Liste von Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
