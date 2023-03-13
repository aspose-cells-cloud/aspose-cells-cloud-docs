---
title: Metadaten aus der Datei Excel abrufen
second_title: Aspose.Cells Cloud Documen
linktitle: Holen Sie sich ohne Verwendung von storag
type: docs
url: /de/metadata/get/
keywords: Get properties from Excel files
description: Aspose.Cells Cloud REST API unterstützt das Abrufen von Eigenschaften aus Excel-Dateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 23
---
Dieser REST API gibt an, dass `metadata` aus mehreren Excel-Dateien abgerufen werden soll.

```bash

POST https://api.aspose.cloud/v3.0/cells/metadata/get

```

- **Abfrageparameter**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Typ| Schnur| ALLE/Integriert/Benutzerdefiniert|


- **Body-Parameter anfordern**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
|Excel-Datei| Datendatei|Die Datendatei wird im ersten Teil des mehrteiligen Inhalts gespeichert.|

- **Antwort**

```bash
{
    [
        { 
            "Name":"test1",
            "Value":"test1",
            ...
        },
        { 
            "Name":"test2",
            "Value":"test3",
            ...
        }
    ]
}
```
- **Cloud SDK-Familie**

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Metadata-Get.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-MetaData-Get.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Metadata-Get.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}
{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LiteCellsMetadata-Get.py" >}}
{{< /tab >}}
{{< /tabs >}}
