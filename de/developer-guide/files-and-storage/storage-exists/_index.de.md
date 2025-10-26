---
title: Speicher vorhanden
second_title: Documen
linktitle: Speicher vorhanden
type: docs
url: /de/storage-exists/
keywords: Excel API, Storage Exists, REST API, Office Cloud, Cloud Storage, Excel Worksheet, Check Storage, Data Management, API Integratio
description: Erfahren Sie, wie Sie mit Aspose.Cells REST API prüfen, ob Speicher vorhanden ist. Dieses Handbuch enthält detaillierte API-Endpunktinformationen, Anforderungsparameter und Antwortbeschreibungen
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel-Arbeitsblatt abgleichen
---
## **Excel API : Speicher vorhanden**

```
GET http://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Funktionsbeschreibung**

 Der**SpeicherExistiert**API prüft, ob ein angegebener Speicher im Cloud-Dienst Aspose.Cells vorhanden ist. Diese Funktion ist entscheidend, um sicherzustellen, dass alle vom Speicher abhängigen Vorgänge fehlerfrei ausgeführt werden können.

###  Die Anfrageparameter von**SpeicherExistiert** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Speichername|Zeichenfolge|Weg|Der Name des Speichers, dessen Existenz überprüft werden soll.|

### **Antwortbeschreibung**

```json
{
  "Name": "StorageExist",
  "Description": [
    "Indicates whether the specified storage exists."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Indicates if the storage exists.",
        "This property returns true if the storage is present; otherwise, it returns false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/StorageController/StorageExists) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Entwicklern ermöglicht, nahtlos direkt von einem Webbrowser aus mit REST API zu interagieren.

## Excel API SDK

 Die Nutzung eines SDKs ist der effizienteste Ansatz zur Beschleunigung der Entwicklung. Ein SDK abstrahiert Low-Level-Implementierungsdetails und ermöglicht es Entwicklern, sich auf ihre Projektaufgaben zu konzentrieren. Eine umfassende Liste der verfügbaren Aspose.Cells Cloud SDKs finden Sie unter[GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs API-Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{< /tab >}}
{{< /tabs >}}
