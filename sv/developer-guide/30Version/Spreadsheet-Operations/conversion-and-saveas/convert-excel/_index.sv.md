---
title: "Konvertera en Excel-fil till olika format"
ArticleTitle: "Konvertera en Excel-fil till olika format"
second_title: "Dokument"
linktitle: "Konvertera Excel"
type: docs
url: /sv/convert-an-excel-file-to-different-formats/
aliases:
  [
    /convert-excel-workbook-to-different-file-formats/,
    /convert/excel-to-different-formats/,
  ]
keywords: "Aspose.Cells Cloud, Excel-konvertering, filformatkonvertering, REST API, SDK, CSV, PDF, HTML, JSON, Markdown"
description: "Konvertera Excel-arbetsböcker till format som CSV, PDF, HTML, JSON, Markdown och mer med Aspose.Cells Cloud REST API."
weight: 10
---

Innan du anropar den här slutpunkten, se till att du har erhållit en giltig JWT-token och att källarbetsboken lagras på en stödd lagringsplats (t.ex. Aspose Cloud Storage). Inkludera token i `Authorization`-headern och, om nödvändigt, ange frågeparametern `storageName`.

Denna REST API konverterar en Excel-fil till olika utgångsformat.

## PutConvertWorkBook API

```http
PUT https://api.aspose.cloud/v3.0/cells/convert
```

Begäran är en HTTP **PUT** med multipart-innehåll (se [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Den första delen av multipart-bodyn innehåller **datafilen**, och den andra delen innehåller **sparaalternativen**.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Frågeparametrar

| Parameternamn           | Typ    | Beskrivning                                                                                                                 |
| ----------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------- |
| `format`                | string | Målfilformat (t.ex. CSV, XLS, HTML, PDF, XML, TXT, TIFF, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG etc.).              |
| `password`              | string | Lösenord som krävs för att öppna käll-Excel-filen.                                                                          |
| `outPath`               | string | Fullständig sökväg (inklusive filnamn och filtillägg) för en enda utdatafil, eller en mapp sökväg när flera filer genereras. |
| `storageName`           | string | Namn på lagringsplatsen där källfilen finns.                                                                                |
| `checkExcelRestriction` | bool   | När **true** valideras Excel-begränsningar innan celler eller relaterade objekt ändras.                                    |
| `streamFormat`          | string | Format för indataströmmen.                                                                                                  |
| `region`                | string | regionala inställningar som tillämpas på arbetsboken.                                                                      |
| `pageWideFitOnPerSheet` | bool   | Justerar sidbredden så att den passar varje kalkylblad vid konvertering till PDF.                                          |
| `pageTallFitOnPerSheet` | bool   | Justerar sidhöjden så att den passar varje kalkylblad vid konvertering till PDF.                                           |
| `sheetName`             | string | Namn på kalkylbladet som ska konverteras.                                                                                   |
| `pageIndex`             | string | Index för sidan som ska konverteras (kräver `sheetName`).                                                                   |
| `onePagePerSheet`       | bool   | När **true** genereras en PDF-sida per kalkylblad.                                                                          |
| `AutoRowsFit`           | bool   | Auto-passar alla rader i arbetsboken.                                                                                       |
| `AutoColumnsFit`        | bool   | Auto-passar kolumnbredder i arbetsboken.                                                                                    |

### Begärandetextparametrar

| Parameternamn | Typ       | Beskrivning                                                    |
| ------------- | --------- | -------------------------------------------------------------- |
| `datafile`    | datafil   | Excel-filen placerad i den första delen av multipart-bodyn.   |
| `SaveOptions` | objekt    | Sparaalternativ placerade i den andra delen av multipart-bodyn. |

### **Svar**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                      |
|-----|-----------------------------|------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Bad Request                 | Saknas eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                                  |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.                |
| 500 | Internal Server Error       | Oväntat serverfel.                                               |

## Hur du använder PutConvertWorkBook API med SDK:er

### PutConvertWorkBook API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) definierar ett offentligt tillgängligt gränssnitt som möjliggör direkt REST-interaktion från en webbläsare.

### cURL-exempel

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/convert?format=html" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Använd Aspose.Cells Cloud SDK:er

Genom att använda ett SDK accelererar du utvecklingen eftersom det hanterar detaljer på låg nivå, så att du kan fokusera på affärslogiken. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "ExamplePutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExamplePutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExamplePutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExamplePutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExamplePutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExamplePutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}