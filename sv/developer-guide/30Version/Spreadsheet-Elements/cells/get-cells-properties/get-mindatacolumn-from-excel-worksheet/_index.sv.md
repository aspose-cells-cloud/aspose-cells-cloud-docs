---
title: "Hämta MinDataColumn – Aspose.Cells Cloud API-referens (v3.0)"
type: docs
url: /sv/get-mindatacolumn-from-excel-worksheet/
weight: 110
keywords: "Aspose.Cells Cloud, MinDataColumn, Excel-arbetsblad, REST API, API-referens, v3.0, dataspalt, moln-API"
description: "Hämta den mest vänstra kolumnen som innehåller data i ett Excel-arbetsblad via Aspose.Cells Cloud REST API (v3.0). Inkluderar autentiseringsinformation, begärsyntax, exempel på JSON-svar, felkoder och SDK-utdrag."
ArticleTitle: "Hämta MinDataColumn – Aspose.Cells Cloud API-referens (v3.0)"
---

**`mindatacolumn`**-ändpunkten returnerar det nollbaserade indexet för den mest vänstra kolumnen som innehåller någon celldata i ett angivet arbetsblad.  
Med andra ord anger den vilken kolumn som är den första som faktiskt innehåller data.

> **Definition** – `mindatacolumn`: indexet (börjar vid 0) för den första kolumnen som innehåller data i arbetsbladet.

**Förutsättningar**  
- Ett giltigt OAuth2-åtkomsttoken krävs.  
- Excel-filen måste vara uppladdad till Aspose Cloud-lagring.

**Begärparametrar**

| Parameter                | Typ    | Obligatorisk | Beskrivning                                      |
|--------------------------|--------|--------------|--------------------------------------------------|
| `fileName`               | sträng | Ja           | Namn på Excel-filen som finns lagrad i molnlagring. |
| `sheetName`              | sträng | Ja           | Namn på arbetsbladet från vilket kolumnindexet ska hämtas. |
| `Authorization` (huvud)  | sträng | Ja           | Bearer-token för OAuth2-autentisering.          |

- **cURL-exempel**

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/mindatacolumn" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MinDataColumn": 2
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP-statuskoder**

| Kod | Betydelse                 | Beskrivning                                         |
|-----|---------------------------|-----------------------------------------------------|
| 200 | OK                        | Filtrering lyckades; svaret innehåller åtgärdens information. |
| 400 | Felaktig begäran          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad         | Ogiltig eller saknad JWT-token.                     |
| 413 | För stor nyttolast        | Den uppladdade filen överskrider storleksgränsen.   |
| 500 | Internt serverfel         | Oväntat serverfel.                                  |
---

- Använd Aspose.Cells Cloud SDK:n

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på din projektlogik. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataColumnWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataColumn.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_column.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataColumnFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataColumnWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataColumnWorksheet-get-min-data-column.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataColumnWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48105eac1e6a64ad3ae4f269c32f3a88" >}}

{{< /tab >}}

{{< /tabs >}}
---