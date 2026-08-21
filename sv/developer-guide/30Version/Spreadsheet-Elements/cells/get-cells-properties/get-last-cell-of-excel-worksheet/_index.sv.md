---
title: "Hämta sista cellen i ett Excel-arbetsblad – Aspose.Cells Cloud API (v4.0)"
type: docs
url: /sv/get-last-cell-of-excel-worksheet/
weight: 30
keywords: "Aspose.Cells, Excel API, hämta sista cellen, kalkylark, moln"
description: "Hämta adressen till slutcellen i ett Excel-arbetsblad med Aspose.Cells Cloud REST API v4.0. Inkluderar begärandeinformation, cURL-exempel, JSON-svar och SDK-exempel."
ArticleTitle: "Hämta slutcellen i ett Excel-arbetsblad – Aspose.Cells Cloud API v4.0"
---

Denna REST API returnerar **endcellen** i ett Excel-arbetsblad när parametern `cellOrMethodName` är inställd på `endcell`.

**Översikt**  
Åtgärden **Get Last Cell** (Hämta sista cellen) returnerar adressen till den sista använda cellen i ett angivet arbetsblad. Detta är användbart för att fastställa det faktiska dataomfånget i ett ark utan att behöva skanna hela arbetsboken.

- **cURL-exempel.**

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/endcell" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "F341",
    "Row": 340,
    "Column": 5,
    "Value": "<Mer information>",
    "Type": "IsString",
    "Formula": "=HYPERLINK(SUBSTITUTE(HelpURLTemplate,\"xxxxxxxxxx\",[Help Topic]),\"<Mer information>\")",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"TEXT-DECORATION: underline;FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">&lt;Mer information&gt;</Font>",
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

{{< /tab >}}

{{< /tabs >}}

### Parametrar
| Parameter            | Typ    | Krävs  | Beskrivning |
|----------------------|--------|--------|-------------|
| `fileName`           | string | Ja     | Namn på Excel-filen som är lagrad i molnet. |
| `worksheetName`      | string | Ja     | Namn på arbetsbladet vars sista cell ska hämtas. |
| `cellOrMethodName`   | string | Ja     | Måste vara inställd på **`endcell`** för att utföra denna åtgärd. |
| `folder` *(valfri)*  | string | Nej    | Molkatalogsökväg där arbetsboken finns. |
| `storageName` *(valfri)*| string | Nej | Namn på lagringen. Om utelämnas används standardlagring. |

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller information om åtgärden. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering misslyckades  | Ogiltigt eller saknat JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

- **Använd Aspose.Cells Cloud SDK:er**

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå, så att du kan fokusera på dina projektuppgifter. Besök <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetLastCellWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetLastCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_last_cell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetLastCellOfExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetLastCellWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetEndCellWorksheet-get-last-cell-excel-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

_Kommer snart._

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetLastCellWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3cf3e145c223fd6f6f3d9f6377092db5" >}}

{{< /tab >}}

{{< /tabs >}}

För ytterligare åtgärder relaterade till cellnavigering, se ämnena **[Get First Cell](/sv/get-first-cell-of-excel-worksheet/)** och **[Get Max Row](/sv/get-max-row-of-worksheet/)**.