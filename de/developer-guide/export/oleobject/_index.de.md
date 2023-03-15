---
title: OLE-Objekt exportieren
second_title: Aspose.Cells Cloud Documen
linktitle: OLE-Objekt
type: docs
url: /de/export/excel-ole-object/
keywords: Export Excel OLE object to kinds of format files
description: Aspose.Cells Cloud REST API unterstützt den Export von Excel OLE-Objekten in verschiedene Formatdateien. SDK unterstützt Arten von Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 20
---
- **REST API**

|**API**|**Typ**|**Beschreibung**|**Swagger-Link**|
|:- |:- |:- |:- |
|/cells/exportieren|POST|Exportieren Sie Excel aus Anforderungsinhalten in ein bestimmtes Format|[PostExport](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport)|


 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LiteCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und lässt Sie REST-Interaktionen direkt von einem Webbrowser ausführen.

 Sie können verwenden**cURL** Befehlszeilentool für den einfachen Zugriff auf Aspose.Cells-Webdienste. Das folgende Beispiel zeigt, wie Sie Cloud API mit cURL anrufen.



- **Anfrage**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Antwort**

```bash
{
    "Files": [{
        "Filename": "OLESlide.ppt",
        "FileSize": 390,
        "FileContent": "-----Base64String--------"
    }, {
        "Filename": "OLEDoc.docx",
        "FileSize": 382,
        "FileContent": "-----Base64String--------"
    }]
}
```

- **Cloud SDK-Familie**

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Bitte überprüfen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-shape-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LiteCells-Export-shape-tiff.php" >}}

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

{{< /tabs >}}
