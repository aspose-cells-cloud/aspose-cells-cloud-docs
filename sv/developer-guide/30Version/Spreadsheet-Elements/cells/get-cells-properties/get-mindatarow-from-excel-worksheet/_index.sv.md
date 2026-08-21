---
title: "Hämta MinDataRow från Excel-arbetsblad"
type: docs
url: /sv/get-mindatarow-from-excel-worksheet/
weight: 90
keywords: "Aspose Cells, MinDataRow, Excel API, molntjänst"
description: "Hämta det minsta dataradindexet för ett arbetsblad med Aspose.Cells molntjänst v3.0. Inkluderar begäransmönster, parametrar, exempel på cURL, svarsexempel, HTTP-statuskoder och SDK-fragment."
ArticleTitle: "Hämta MinDataRow från Excel-arbetsblad – Aspose.Cells molntjänst"
---

**Get MinDataRow**-ändpunkten i **Aspose.Cells molntjänst v3.0** returnerar indexet för den första raden som innehåller data i ett angivet arbetsblad. Operationen kräver en giltig åtkomsttoken (Bearer-autentisering) och frågeparametern `cellOrMethodName` inställd på `mindatarow`.

**API-version: 3.0**

### cURL-exempel

Begäran använder HTTP-metoden GET. Ersätt platshållarna `{fileName}` och `{sheetName}` med faktiska namn på arbetsboken och arbetsbladet.

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/cells/mindatarow?cellOrMethodName=mindatarow" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Begäranparametrar**

| Parameter          | Plats   | Typ    | Obligatorisk | Beskrivning                                              |
|--------------------|---------|--------|--------------|----------------------------------------------------------|
| `fileName`         | Sökväg  | sträng | Ja           | Namn på Excel-arbetsboken (inklusive filtillägg).       |
| `sheetName`        | Sökväg  | sträng | Ja           | Namn på arbetsbladet inom arbetsboken.                   |
| `cellOrMethodName` | Fråga   | sträng | Ja           | Måste vara inställt på `mindatarow` för att köra operationen. |

**Svarsexempel**

```json
{
  "MinDataRow": 5
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller detaljer om operationen. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel inträffade. |

### SDK-exempel

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på din projektlogik. Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener">GitHub-repositoriet</a> för en fullständig lista över Aspose.Cells molntjänst-SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-GetMinDataRowWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-GetWorksheetMinDataRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-get_worksheet_min_data_row.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetMinDataRowFromExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-GetMinDataRowWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-cells-GetMinDataRowWorksheet-get-min-data-row.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-GetMinDataRowWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "85f2a886ba296b8abf640c0638b4eec1" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även**

- [Hämta MaxDataRow](https://docs.aspose.cloud/cells/get-maxdatarow-from-excel-worksheet/)
- [Hämta MinColumn](https://docs.aspose.cloud/cells/get-mincolumn-from-excel-worksheet/)
- [Hämta MaxColumn](https://docs.aspose.cloud/cells/get-maxcolumn-from-excel-worksheet/)