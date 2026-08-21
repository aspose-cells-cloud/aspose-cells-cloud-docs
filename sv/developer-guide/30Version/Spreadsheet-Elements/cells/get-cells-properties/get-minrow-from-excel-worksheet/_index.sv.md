---
title: "Hämta MinRow från Excel-arbetsblad – Aspose.Cells Cloud API-referens"
type: docs
url: /sv/get-minrow-from-excel-worksheet/
weight: 80
keywords: "Aspose.Cells, GetMinRow, Excel-arbetsblad, REST API, minsta radindex, moln-SDK"
description: "Lär dig hur du hämtar minsta radindex för ett arbetsblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar fullständig cURL-begäran med autentisering, svarsschema och SDK-exempel för flera språk."
ArticleTitle: "Hämta MinRow från Excel-arbetsblad – Aspose.Cells Cloud API-referens"
---

Denna REST API returnerar det minsta radindexet i ett Excel-arbetsblad när parametern `cellOrMethodName` är inställd på `minrow`. slutpunkten kan användas för att fastställa den första icke-tomma raden (nollbaserad) i ett givet arbetsblad.

- **cURL-exempel:**

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/minrow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "MinRow": 0
}
```

{{< /tab >}}

{{< /tabs >}}

**Begäran**

```
GET https://api.aspose.com/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/minrow
```

| Egenskap          | Typ    | Obligatorisk | Beskrivning                                         |
|-------------------|--------|--------------|-----------------------------------------------------|
| `fileName`        | sträng | Ja           | Namn på arbetsboken (t.ex. `myWorkbook.xlsx`).      |
| `sheetName`       | sträng | Ja           | Målarbetsblad (t.ex. `Sheet1`).                      |
| `cellOrMethodName`| sträng | Ja           | Fixerat värde `minrow`.                              |
| `folder`          | sträng | Nej          | Sökväg till mapp i molnlagring.                     |
| `storageName`     | sträng | Nej          | Lagringsnamn om en icke-standardlagring används.   |

**Svar**

Tjänsten returnerar ett JSON-objekt som innehåller egenskapen `MinRow`, vilket anger indexet för den första icke-tomma raden (nollbaserad).

| HTTP-status | Betydelse                                |
|-------------|-------------------------------------------|
| 200         | Lyckades – JSON-payload med `MinRow`.     |
| 401         | Obehörig – ogiltig eller saknad token.    |
| 404         | Arbetsbok eller arbetsblad hittades inte.|
| 500         | Internt serverfel.                        |

Värdet `MinRow` är användbart när du behöver snabbt hitta början på data i ett blad.

- **Använd Aspose.Cells Cloud SDK:n**

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förvaret</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:n:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinRowWorksheet-get-min-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "d9497c39cde5cecb6709ff5feb2ab2b8" >}}

{{< /tab >}}

{{< /tabs >}}