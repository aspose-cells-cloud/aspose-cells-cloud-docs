---
title: Importera Json-data till Excel
second_title: Aspose.Cells Cloud Documen
linktitle: Importera Jso
type: docs
url: /sv/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: "Aspose.Cells Cloud REST API stöder import av strängmatrisdata till Excel-filer. SDK:n stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift."
weight: 40
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Importera Json-data till Excel
---
Detta REST API `import json data` till Excel-arbetsblad.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

De viktiga parametrarna beskrivs i följande tabell:

**ImportStringArrayAlternativ**

|Parameternamn| Sökväg/Frågesträng/HTTP-kropp|Typ|Beskrivning|
|:- |:- |:- |:- |
| namn| Väg| sträng| Arbetsbokens namn|
| importJsonRequest| HTTPBody| klass| Importera json-begäran.|
| lösenord| Frågesträng| sträng| Lösenordet till arbetsboken.|
| mapp| Frågesträng| sträng| Original arbetsboksmapp.|
| lagringsnamn| Frågesträng| sträng| Lagringsnamn.|
| utväg| Frågesträng| sträng| Sökväg till utdatafil.|
| outStorageName| Frågesträng| sträng| Lagringsnamn för utdatafilen.|
| kontrolleraExcelBegränsning| Frågesträng| sträng| Kontrollera Excel-begränsningen.|

**Exempel**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Cloud SDK-familjen

 Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
