---
title: "Importera heltalsarray till Excel-arbetsblad"
linktitle: "Importera heltalsarray"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, importera heltalsarray, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Lär dig hur du importerar en heltalsarray till ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Innehåller begäresyntax, parametrar, exempelkod för flera SDK:er och svarsinformation."
weight: 30
ArticleTitle: "Importera heltalsarray till Excel-arbetsblad – Aspose.Cells Cloud API"
---

Denna REST API importerar en heltalsarray till ett Excel-arbetsblad.

Begäran måste vara en HTTP **POST** med multipart-innehåll (se [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av multipart-kroppen innehåller JSON-payloaden **ImportIntegerArrayOption**, och den andra delen innehåller källfilen (t.ex. en CSV- eller binär Excel-fil).

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Båda slutpunkterna accepterar samma multipart-payload. Den första slutpunkten utför en generisk importåtgärd, medan den andra riktar sig till en specifik arbetsbok som identifieras av `{name}`.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäran parametrar**

### ImportIntegerArrayOption

| Parameternamn            | Typ        | Beskrivning                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | Nullbaserat index för den första raden där data ska placeras.                                                                                                                                |
| **FirstColumn**          | int        | Nullbaserat index för den första kolumnen där data ska placeras.                                                                                                                             |
| **IsVertical**           | boolean    | `true` för att infoga arrayen vertikalt (nedåt i en kolumn); `false` för att infoga den horisontellt ( längs en rad).                                                                       |
| **Data**                 | Integer[]  | Den heltalsarray som ska importeras.                                                                                                                                                           |
| **DestinationWorksheet** | string     | Namn på det arbetsblad som ska ta emot data.                                                                                                                                                   |
| **IsInsert**             | boolean    | `true` för att infoga rader/kolumner innan data skrivs; `false` för att skriva över befintliga celler.                                                                                       |
| **ImportDataType**       | string     | Typ av data som importeras. Giltiga värden: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | Indikerar positionen för datafilen när parametern **BatchData** är `null`.                                                                                                                   |

#### Exempel på begäran

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Svar

En lyckad begäran returnerar **HTTP 200** med en JSON-payload liknande följande:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Möjliga statuskoder:

| Kod | Betydelse                               |
| --- | --------------------------------------- |
| 200 | Importen lyckades                       |
| 400 | Felaktig begäran – saknad eller ogiltig data |
| 401 | Obehörig – ogiltig eller saknad token   |
| 500 | Internt serverfel                       |

## Hur du använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att integrera denna funktionalitet. SDK:er abstraherar från de lågnivådetaljer och låter dig fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}