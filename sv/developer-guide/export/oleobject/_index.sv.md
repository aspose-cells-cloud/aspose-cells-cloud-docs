---
title: Exportera OLE-objekt
second_title: Aspose.Cells Cloud Documen
linktitle: OLE Objekt
type: docs
url: /sv/export/excel-ole-object/
keywords: Export Excel OLE object to kinds of format files
description: Aspose.Cells Cloud REST API stöder export av Excel OLE-objekt till olika formatfiler. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 20
---
- **REST API**

|**API**|**Typ**|**Beskrivning**|**Swagger Link**|
|:- |:- |:- |:- |
|/celler/export|POSTA|Exportera excel från begäran om innehåll till något format|[PostExport](https://apireference.aspose.cloud/cells/#/LightCells/PostExport)|


 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

 Du kan använda**cURL** kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.



- **Begäran**

```bash

curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject" -H "accept: multipart/form-data" -H "Content-Type: multipart/form-data" -H "x-aspose-client: Containerize.Swagger" -d {"File":{}}
```

- **Svar**

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

- **Cloud SDK-familj**

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:


{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Export-shape-tiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Export-shape-tiff.php" >}}

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
