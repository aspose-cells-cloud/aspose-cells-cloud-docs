---
title: "Hämta en pivottabell i ett Excel-ark"
second_title: "Dokument"
linktitle: Hämta
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, pivottabell, Excel, REST API, hämta pivottabell från kalkylark"
description: "Hämta en pivottabell från ett Excel-ark via Aspose.Cells Cloud REST API. Innehåller begärandesyntax, parametrar, autentisering, svarsschema, felhantering och SDK-exempel."
weight: 10
ArticleTitle: "Hämta en pivottabell i ett Excel-ark"
---

Denna REST API hämtar information om **pivottabell** i ett kalkylark baserat på dess index.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### Begäransparametrar

| Parameternamn       | Typ     | Plats  | Beskrivning                                              |
| ------------------- | ------- | ------ | -------------------------------------------------------- |
| **name**            | string  | path   | Namnet på Excel-filen.                                   |
| **sheetName**       | string  | path   | Namnet på kalkylarket som innehåller pivottabellen.     |
| **pivottableIndex** | integer | path   | Nollbaserat index för pivottabellen i kalkylarket.       |
| **folder**          | string  | query  | Mappen där dokumentet lagras.                            |
| **storageName**     | string  | query  | Namnet på Aspose Cloud-lagringen.                        |

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**Svarschema**

| Fält           | Typ     | Beskrivning                                        |
|----------------|---------|----------------------------------------------------|
| Status         | string  | Statustext för åtgärden (t.ex. "OK").             |
| PivotFilters   | array   | Samling av pivotfilterdefinitioner.               |
| └─ AutoFilter  | object  | Detaljer för automatiskt filter som tillämpas på pivot. |
|    └─ link     | object  | Hyperlänksinformation för filtret.                |
|    └─ FilterColumns | array | Inställningar för individuella kolumnfilter.   |
|    └─ Range    | string  | Cellområde som filtret gäller för.                |
|    └─ Sorter   | object  | Sorteringskonfiguration för den filtrerade datan. |
| (ytterligare nästlade fält följer samma struktur som visas i JSON-exemplet) |

{{< /tab >}}

{{< /tabs >}}

### Felhantering

API:et följer standard HTTP-statuskoder. Typiska svar inkluderar:

| Statuskod | Betydelse                                                        | Exempel JSON (fel)                                |
| --------- | ---------------------------------------------------------------- | ------------------------------------------------ |
| 200       | Lyckades – pivottabellen returneras                              | —                                                |
| 401       | Auktorisering misslyckades – ogiltig eller saknad token         | `{"code":401,"message":"Invalid access token."}` |
| 404       | Hittades inte – fil, kalkylark eller pivottabellindex finns inte | `{"code":404,"message":"Pivot table not found."}` |
| 500       | Serverfel – oväntat tillstånd                                    | `{"code":500,"message":"Internal server error."}` |

**Anteckningar:** API:et stöder Excel-filer upp till 150 MB och fungerar med Excel 2007–2021-format. Se till att kalkylarkets namn är skiftlägeskänsligt.

## Moln SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}