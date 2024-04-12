---
title: Importera data med hjälp av lagring
second_title: Aspose.Cells Cloud Documen
linktitle: Importera data med lagring
type: docs
url: /sv/import/with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/]
description: "Cells.Cloud API för Excel fungerar: Importera data till Excel Arbetsblad"
weight: 10
---
Denna REST API indikerar `import data` till Excel fil.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```
 Begärans parametrar är:
 
| Parameternamn| Typ| Sökväg/Frågesträng/HTTPBody|Beskrivning|
|:- |:- |:- |:- |
| namn| sträng| väg||
| mapp| sträng| fråga||
| lagringsnamn| sträng| fråga| lagringsnamn.|
| importera data|| kropp||

**Parametrarna för import av dataalternativ** beskrivs i[referenslänken](/cells/sv/import/#import-data-option-parameter).

 
 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definierar ett allmänt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.
 
Du kan använda cURL kommandoradsverktyg för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till Cloud API med cURL.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
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
 
 
Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:

