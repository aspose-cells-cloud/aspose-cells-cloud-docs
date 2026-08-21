---
title: "Excel till CSV"
second: "Dokument"
linktitle: "Excel till CSV"
type: docs
url: convert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel till CSV, Aspose.Cells Cloud, REST API, kalkylbladskonvertering, CSV-fil, filkonvertering"
description: "Konvertera Excel-kalkylblad till CSV med Aspose.Cells Cloud REST API. Stöder flera SDK:er och programmeringsspråk för enkel integration."
weight: 90
---

Denna REST API konverterar ett kalkylbladsfil till en CSV-formatfil.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Frågeparametrar

| Parameternamn           | Typ    | Beskrivning                                                                                      |
| ----------------------- | ------ | ------------------------------------------------------------------------------------------------ |
| `password`              | sträng | Lösenordet som krävs för att öppna Excel-filen.                                                  |
| `storageName`           | sträng | Namnet på lagringsplatsen där filen finns.                                                       |
| `checkExcelRestriction` | bool   | Om Excel-filbegränsningar ska kontrolleras när användaren redigerar cellrelaterade objekt.       |

### Begäran – brödtextparameter

| Parameternamn | Typ       | Beskrivning                                                         |
| ------------- | --------- | ------------------------------------------------------------------- |
| `datafile`    | datafil   | Datafilen som ingår i första delen av multipart-begärandetexten.    |

### Svar

API:et returnerar ett **FileInfo**-objekt som innehåller den genererade CSV-filen.

| Fält            | Typ    | Beskrivning                                      |
| --------------- | ------ | ------------------------------------------------ |
| **Filename**    | sträng | Namn på CSV-filen (t.ex. `example.csv`).        |
| **FileSize**    | int    | Filens storlek i byte.                           |
| **FileContent** | sträng | Bas64-kodat innehåll i CSV-filen.                |

[FileInfo](/cells/file-info/)


**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 200 | OK                          | Filtrering lyckades; svaret innehåller åtgärdens detaljer.                 |
| 400 | Felaktig begäran            | Saknas eller ogiltiga parametrar (t.ex. filtyp som inte stöds).            |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                                             |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.                          |
| 500 | Internt serverfel           | Oväntat serverfel.                                                          |
## Hur man använder PostConvertWorkbookToCSV API med SDK:er

### PostConvertWorkbookToCSV API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att komma åt Aspose.Cells webbtjänster. Exempel nedan visar hur man anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på ditt projekt. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}