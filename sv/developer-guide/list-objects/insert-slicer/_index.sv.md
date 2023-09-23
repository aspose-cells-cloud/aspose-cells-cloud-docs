---
title:  Listobjekt infogning slicer
second_title: Aspose.Cells Cloud Documen
linktitle: Sätt i skiva
type: docs
keywords: Insert slicer for list object
url: /sv/list-objects/insert-slicer/
description:  Infoga slicer för listobjekt.
weight: 20
---
 Denna REST API indikerar insert slicer för listobjekt på ett Excel kalkylblad.

## RSET API

```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer

```

 Begärans parametrar är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg||
|arknamn|Sträng|Väg||
|listObjectIndex|Heltal|Väg||
|columnIndex|Heltal|Fråga||
|destCellName|Sträng|Fråga||
|mapp|Sträng|Fråga||
|lagringsnamn|Sträng|Fråga||



 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectInsertSlicer) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/InsertSlicer" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in GitHub-förvaret för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:
