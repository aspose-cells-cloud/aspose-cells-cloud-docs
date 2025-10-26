---
title: Dateiversion abrufen
second_title: Documen
linktitle: Dateiversion abrufen
type: docs
url: /de/get-file-versions/
keywords: file versions, Excel API, Office Cloud, REST API, spreadsheet management, document histor
description: Abrufen und Verwalten der Versionen von Dateien, die in der Aspose.Cells Cloud gespeichert sind, wodurch die Dokumentenverwaltung und Zusammenarbeit verbessert wird
weight: 100
kwords: Dateiversionen abrufen, Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Dokumentenverwaltung
---
## **Excel API: Dateiversionen abrufen**

```
GET http://api.aspose.cloud/v4.0/cells/storage/version/{path}
```

### **Funktionsbeschreibung**

 Der**GetFileVersions** Mit API können Benutzer die verschiedenen Versionen einer bestimmten Datei abrufen, die in der Aspose.Cells Cloud gespeichert ist. Diese Funktion ist entscheidend für die Aufrechterhaltung der Dokumentintegrität und die Nachverfolgung von Änderungen im Laufe der Zeit.

###  Die Anfrageparameter von**GetFileVersions** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Weg| Zeichenfolge| Weg| Der Pfad zur Datei, für die Versionen abgerufen werden sollen.|
| Speichername| Zeichenfolge| Abfrage| Der Name des Speichers, in dem sich die Datei befindet.|

### **Antwortbeschreibung**

```json
{
  "Name": "FileVersions",
  "Description": [
    "Contains a list of file versions for the specified document."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "A collection of file version details."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "FileVersion",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "FileVersion",
          "Name": "class:fileversion"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/StorageController/GetFileVersions)bietet eine umfassende Programmierschnittstelle zum Ausführen von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

 Die Verwendung eines SDK rationalisiert die Entwicklung durch die Abstraktion von Komplexitäten auf niedriger Ebene, sodass sich Entwickler auf Kernfunktionen konzentrieren können. Entdecken Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen die Interaktion mit Aspose.Cells-Webdiensten in verschiedenen Programmiersprachen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFileVersions.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFileVersions.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFileVersions.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFileVersions.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFileVersions.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFileVersions.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFileVersions.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFileVersions.go" >}}
{{< /tab >}}
{{< /tabs >}}
