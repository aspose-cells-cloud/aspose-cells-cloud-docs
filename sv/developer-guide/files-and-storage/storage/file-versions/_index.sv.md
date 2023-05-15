---
title: Filversion
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/storage/file-versions/
keywords: Learn how to get file version with Aspose Cells Cloud REST API
description: Lär dig hur du får en filversion med Aspose Cells Cloud REST API SDK-stöd för olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 100
---
Denna REST API indikerar få `file versions`.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Filsökväg t.ex. '/file.ext'|
| lagringsnamn| sträng| fråga| Lagringsnamn|

 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 
 