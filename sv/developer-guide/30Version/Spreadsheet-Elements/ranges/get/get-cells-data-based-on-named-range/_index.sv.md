---
title: "Hämta celldata baserat på namngivet intervall"
second_title: "Document"
linktitle: "Värden"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, moln, REST API, Excel, namngivet intervall, cellvärden, kalkylblad"
description: "Hämta cellvärden från ett namngivet intervall i ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Tjänsten är tillgänglig via flera SDK:er (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) och fungerar över ett brett spektrum av utvecklingsplattformar."
weight: 20
ArticleTitle: "Hämta celldata baserat på namngivet intervall – Aspose.Cells Cloud API"
---

**Förutsättningar**

- En giltig JWT-åtkomsttoken med lämpligt omfattning.  
- Arbetsboken måste ha laddats upp till Aspose Cloud-lagring (eller en angiven mapp).  
- Se till att lagringsnamnet anges om du använder en icke-standardlagring.

Denna REST API returnerar en lista över celler i ett intervall som identifieras av ett namngivet intervall eller av rad-/kolumnindex.

Denna åtgärd tillåter utvecklare att programmatiskt hämta värdena på celler som tillhör ett specifikt namngivet intervall i ett Excel-kalkylblad. Genom att ange antingen `namedRange`-identifieraren eller explicita rad- och kolumnindex returnerar API:et en detaljerad lista över celler, inklusive deras adress, rad, kolumn, värde, datatyp och formateringsinformation. Svaret kan användas för att driva datastyrd programvara, generera rapporter eller utföra ytterligare beräkningar på serversidan. Aspose.Cells Cloud-tjänsten stöder flera programmeringsspråk via sina SDK:er, vilket säkerställer sömlös integration oavsett utvecklingsplattform. Genom att använda HTTPS säkerställs säker överföring av data, och API:et följer REST-principer och returnerar standard HTTP-statuskoder för lyckade och felaktiga åtgärder.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **Förfrågningsparametrar**

| Parameternamn | Typ    | Plats  | Beskrivning                                                                 |
| ------------- | ------ | ------ | --------------------------------------------------------------------------- |
| name          | string | path   | Namnet på arbetsboksfilen.                                                  |
| sheetName     | string | path   | Namnet på kalkylbladet i arbetsboken.                                       |
| namedRange    | string | query  | Det namngivna intervallet som ska hämtas, t.ex. `A1:B2` eller `range_name1`. |
| firstRow      | integer | query | Nollbaserat index för första raden i intervallet (används när `namedRange` inte anges). |
| firstColumn   | integer | query | Nollbaserat index för första kolumnen i intervallet (används när `namedRange` inte anges). |
| rowCount      | integer | query | Antal rader som ska ingå i intervallet.                                     |
| columnCount   | integer | query | Antal kolumner som ska ingå i intervallet.                                  |
| folder        | string | query  | Mappen som innehåller arbetsboken.                                          |
| storageName   | string | query  | Namnet på molnlagringsplatsen där arbetsboken finns.                        |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt anropa Aspose.Cells-webbtjänster. Exemplet nedan visar hur du begär cellvärden från ett namngivet intervall.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Säkerhetsnotering:** Använd alltid HTTPS när du anropar API:et. Tjänsten stöder inte obekräftat HTTP; HTTPS säkerställer att förfrågan är krypterad och följer säkerhetsrekommendationer.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                            |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

**Exempel på felaktigt svar (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Parametern 'namedRange' saknas eller är ogiltig."
}
```

> **Tips:** API:et använder nollbaserade index för `firstRow` och `firstColumn`. Den första raden i kalkylbladet är till exempel `0`.

## Moln-SDK-familj

Att använda en SDK är det mest effektiva sättet att snabba upp utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}