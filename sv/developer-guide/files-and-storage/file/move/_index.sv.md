---
title: Flytta Fil
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/file/move/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Lär dig hur du laddar ner filer med Aspose Cells Cloud REST API SDK-stöd för olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 100
---
Denna REST API indikerar `move file`
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| srcPath| sträng| väg| Källfilens sökväg t.ex. '/src.ext'|
| destPath| sträng| fråga| Destinationsfilens sökväg t.ex. '/dest.ext'|
| srcStorageName| sträng| fråga| Källlagringsnamn|
| destStorageName| sträng| fråga| Destinationslagringsnamn|
| versionId| sträng| fråga| Filversions-ID att flytta|
 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/MoveFile) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Cloud SDK-familj
 
 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
 
 