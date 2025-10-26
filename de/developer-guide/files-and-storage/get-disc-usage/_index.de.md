---
title: Holen Sie sich Disk Usag
second_title: Documen
linktitle: Holen Sie sich Disk Usag
type: docs
url: /de/get-disk-usage/
keywords: API, Disk Usage, Aspose, Cloud, Excel, REST, Storage, Disc Space, SDK, Programming Interfac
description: Abrufen der aktuellen Datenträgernutzung für Excel API in Aspose Cloud
weight: 100
kwords: Festplattennutzung, Excel API, Aspose Cloud, REST API, Speicherinformationen, SDK-Beispiele, Programmierschnittstelle
---
## **Excel API: GetDiskUsage**

```
GET http://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Funktionsbeschreibung**

Dieser API-Endpunkt ruft die aktuelle Festplattennutzung für Excel API in der Aspose-Cloud-Umgebung ab und ermöglicht Entwicklern, den von ihren Anwendungen verwendeten Speicherplatz zu überwachen.

###  Die Anfrageparameter von**getDiskUsage** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Speichername|Zeichenfolge|Abfrage|Der Name des Speichers, für den die Datenträgernutzung abgerufen werden soll.|

### **Antwortbeschreibung**

```json
{
  "Name": "DiskUsage",
  "Description": [
    "Class for disk space information."
  ],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": [
        "Amount of disk space used by the application."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": [
        "Total available disk space."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung. Ein SDK verarbeitet grundlegende Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{< /tab >}}
{{< /tabs >}}
