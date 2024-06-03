---
title: Importera Json-data till Exce
second_title: Aspose.Cells Cloud Documen
linktitle: Importera Jso
type: docs
url: /sv/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API stöder import av strängarraydata till Excel-filer. SDK stöder olika utvecklingsspråk. De inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och swift
weight: 40
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Importera Json-data till Excel
---
Detta REST API `import json data` till Excel arbetsblad.


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

De viktiga parametrarna beskrivs i följande tabell:


**ImportStringArrayOption**

|Parameternamn|Typ|Beskrivning|
|:- |:- |:- |
| namn| sträng| Arbetsbokens namn|
| importJsonRequest| klass| Importera json-förfrågan.|
| Lösenord| sträng| Lösenordet för arbetsboken.|
| mapp| sträng| Original arbetsboksmapp.|
| lagringsnamn| sträng| Lagringsnamn.|
| outPath| sträng| Utdatafilens sökväg.|
| outStorageName| sträng|Lagringsnamn för utdatafil.|
| checkExcelRestriction| sträng| Kontrollera Excel begränsning.|


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

## Cloud SDK-familj

 Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK tar hand om detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Vänligen kolla in[GitHub-förråd](https://github.com/aspose-cells-cloud) för en komplett lista med Aspose.Cells Cloud SDK.

Följande kodexempel visar hur man ringer till Aspose.Cells webbtjänster med olika SDK:er:





