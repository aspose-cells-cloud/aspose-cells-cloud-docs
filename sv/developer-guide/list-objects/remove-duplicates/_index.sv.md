---
title:  Listobjekt ta bort dubbletter
second_title: Aspose.Cells Cloud Documen
linktitle: Ta bort dubblett
type: docs
keywords: list object(table) remove duplicates 
url: /sv/list-objects/remove-duplicates/
description:  Ta bort dubbletter på listobjekt.
weight: 20
---
 Denna REST API indikerar att ta bort dubbletter på listobjekt.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 Begärans parametrar är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg||
|arknamn|Sträng|Väg||
|listObjectIndex|Heltal|Väg||
|mapp|Sträng|Fråga||
|lagringsnamn|Sträng|Fråga||



 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
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
