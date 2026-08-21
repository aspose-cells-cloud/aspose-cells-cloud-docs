---
title: "Hämta första cellen (A1) från ett Excel-arbetsblad"
type: docs
url: /sv/get-first-cell-from-excel-worksheet/
weight: 20
keywords: "Aspose.Cells Cloud, Excel, REST API, Hämta första cellen, Arbetsblad, A1, API v3"
description: "Lär dig hur du hämtar den första cellen (A1) i ett Excel-arbetsblad med Aspose.Cells Cloud REST API v3.0. Innehåller cURL-förfrågan, JSON-svar, felexempel och SDK-exempel för C#, Java, PHP, Python och mer."
ArticleTitle: "Hämta första cellen (A1) från ett Excel-arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API visar hur du hämtar **den första cellen** i en Excel-fil när parametern `cellOrMethodName` är inställd på `firstcell`.

**Slutpunkt**  
`GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{worksheet}/cells/firstcell`

- **cURL-exempel**

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/firstcell" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parametrar**

| Parameter          | Typ    | Beskrivning                                                | Obligatoriskt |
|--------------------|--------|------------------------------------------------------------|---------------|
| `cellOrMethodName` | sträng | Måste vara inställd på `firstcell` för att hämta första cellen. | Ja            |
| `fileName`         | sträng | Namn på arbetsboksfilen (t.ex. `myWorkbook.xlsx`).          | Ja            |
| `worksheet`        | sträng | Namn på arbetsbladet (t.ex. `Sheet1`).                    | Ja            |
| `Authorization`    | header | Bearer-token för autentisering.                            | Ja            |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A1",
    "Row": 0,
    "Column": 0,
    "Value": "Kategori",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Kategori</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

**Felresponser**

- **401 Oauktoriserad**

```json
{
  "Code": "401",
  "Message": "Ogiltig åtkomsttoken."
}
```

- **404 Hittades inte**

```json
{
  "Code": "404",
  "Message": "Den angivna arbetsboken, arbetsbladet eller cellen finns inte."
}
```

- **500 Internt serverfel**

```json
{
  "Code": "500",
  "Message": "Ett oväntat fel uppstod på servern."
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller detaljer om åtgärden. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

{{< /tab >}}

{{< /tabs >}}

- **Moln-SDK-familj**

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}
---