---
title: "Hämta MaxRow från ett Excel-arbetsblad"
type: docs
url: /sv/get-maxrow-from-excel-worksheet/
weight: 40
ArticleTitle: "Hämta det högsta radnumret i ett Excel-arbetsblad – Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel, MaxRow, REST API, Molntjänst SDK, kalkylark, arbetsblad, GetMaxRow"
description: "Lär dig hur du hämtar det högsta radnumret i ett arbetsblad i en Excel-fil med Aspose.Cells Cloud REST API. Inkluderar begäran syntax, svarsschema, SDK-exempel och användningsnoteringar."
---

Denna REST API returnerar **högsta radnumret** i ett Excel-arbetsblad när parametern `cellOrMethodName` är inställd på `maxrow`.

- **cURL-exempel**

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/maxrow" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "MaxRow": 1048576
}
```

{{< /tab >}}

{{< /tabs >}}

- **Använd Aspose.Cells Cloud SDK:n**

Att använda ett SDK är det mest effektiva sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivånivå, så att du kan fokusera på din projektlogik. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMaxRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMaxRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_max_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMaxRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMaxRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMaxRowWorksheet-get-max-row-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMaxRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "afcfd72b172e9c3e2d283a9ac059c8c7" >}}

{{< /tab >}}

{{< /tabs >}}

**API-referens**

| Objekt | Detaljer |
|--------|----------|
| **Metod** | `GET` |
| **Endpoint** | `/cells/{fileName}/worksheets/{sheetName}/cells/maxrow` |
| **Sökvägsparametrar** | `fileName` – namn på Excel-filen (obligatoriskt) <br> `sheetName` – namn på arbetsbladet (obligatoriskt) |
| **Frågeparametrar** | `folder` – mappsökväg i lagring (valfritt) <br> `storageName` – lagringsnamn (valfritt) |
| **Lyckat svar** | `200 OK` <br> ```json { "MaxRow": heltal } ``` |
| **Felaktiga svar** | `400 Bad Request` – ogiltiga parametrar <br> `401 Unauthorized` – autentiseringsfel <br> `404 Not Found` – fil eller arbetsblad hittades inte |

**Förutsättningar**

- En giltig Aspose Cloud-autentiseringstoken.  
- Målarboksmappen måste vara uppladdad till Aspose Cloud-lagring eller tillgänglig via en offentlig URL.  

**Noteringar**

- Åtgärden finns tillgänglig i API-version **v3.0** och senare.  
- Det returnerade värdet `MaxRow` motsvarar det högsta använda radindexet (1-baserat). För ett tomt arbetsblad är värdet vanligtvis `1`.  

Följande SDK-exempel illustrerar hur du anropar operationen i olika programmeringsspråk.  
---