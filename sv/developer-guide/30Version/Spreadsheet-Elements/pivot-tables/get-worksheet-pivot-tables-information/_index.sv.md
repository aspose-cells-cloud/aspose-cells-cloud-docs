---
title: "Hämta alla pivottabeller i ett Excel-ark"
second_title: "Document"
linktitle: Hämta alla
type: docs
url: /sv/pivot-tables/get-all/
aliases: [  /sv/get-worksheet-pivot-tables-information/ ]
keywords: "hämta alla pivottabeller, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "Hämta alla pivottabeller från ett Excel-ark via Aspose.Cells Cloud API. Inkluderar endpoint, parametrar, autentiseringsssteg, cURL- och SDK-exempel för PivotTables API:t."
weight: 20
ArticleTitle: "Hämta alla pivottabeller i ett Excel-ark – Aspose.Cells Cloud API"
---

En **PivotTable** är ett verktyg i Excel för sammanställning av data som låter dig organisera och analysera stora datamängder. Denna REST API hämtar information om **alla** pivottabeller i ett angivet kalkylark.

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Begäringsparametrar**

| Parameternamn  | Typ    | Plats  | Beskrivning                            |
| -------------- | ------ | ------ | -------------------------------------- |
| name           | string | path   | Namn på Excel-dokumentet.              |
| sheetName      | string | path   | Namn på kalkylarket.                   |
| folder         | string | query  | Mapp där dokumentet lagras.            |
| storageName    | string | query  | Namn på lagringstjänsten.              |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Begäran

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### Svar

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Felsvar

| HTTP-kod | Beskrivning                                                     | Exempel på JSON-svar                                           |
| -------- | --------------------------------------------------------------- | ------------------------------------------------------------- |
| 400      | Felaktig begäran – nödvändig parameter saknas.                  | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401      | Auktorisering misslyckades – ogiltig eller saknad token.        | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404      | Resurs hittades inte – arbetsbok, kalkylark eller pivottable finns inte. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500      | Internt serverfel – oväntat tillstånd på servern.               | `{ "Code": "500", "Message": "Server error." }`               |

## Molnsdk-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på ditt projekt. Ta en titt på [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}