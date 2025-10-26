---
title: Dateiliste abrufen – Aspose.Cells AP
second_title: Developer Guide for Aspose.Cell
linktitle: Dateienliste abrufen
type: docs
url: /de/get-files-list/
keywords: Aspose.Cells API, Get Files List, REST API, Excel File Management, Cloud Storage, File Retrieval, Programming Interfac
description: Erfahren Sie, wie Sie mithilfe von Aspose.Cells API eine Liste von Dateien aus einem angegebenen Ordner abrufen. Dieses Handbuch enthält Details zu Anforderungsparametern, Antwortstruktur und Codebeispielen in verschiedenen Programmiersprachen
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Cloud-Dateiverwaltung, Dateien abrufen
---
## **Excel API: Dateienliste abrufen**

```
GET http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Funktionsbeschreibung**

 Der**getFilesList**Mit API können Benutzer eine umfassende Liste der Dateien und Ordner abrufen, die in einem bestimmten Verzeichnis im Cloud-Speicher Aspose.Cells enthalten sind. Dieser Endpunkt ist für die effiziente Verwaltung von Dateien von entscheidender Bedeutung und unterstützt verschiedene Dateiformate.

###  Die Anfrageparameter von**getFilesList** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Weg| Zeichenfolge| Weg| Der Pfad zum Ordner im Cloud-Speicher, aus dem die Dateiliste abgerufen werden soll.|
| Speichername| Zeichenfolge| Abfrage| Der Name des Speichers, auf den zugegriffen werden soll.|

### **Antwortbeschreibung**

```json
{
  "Name": "FilesList",
  "Description": [
    "Files list"
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Value",
      "Description": [
        "Files and folders contained by the specified StorageFile."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "StorageFile",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "StorageFile",
          "Name": "class:storagefile"
        },
        "Name": "container"
      }
    }
  ]
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FolderController/GetFilesList) definiert eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht und so eine einfache Integration und Prüfung erleichtert.

## Excel API SDK

 Die Nutzung eines SDKs ist der optimale Ansatz, um Ihren Entwicklungsprozess zu beschleunigen. Ein SDK verwaltet Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie unter[GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetFilesList.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetFilesList.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetFilesList.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetFilesList.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetFilesList.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetFilesList.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetFilesList.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetFilesList.go" >}}
{{< /tab >}}
{{< /tabs >}}
