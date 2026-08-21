---
title: "Konvertera kalkylblad till PDF, PNG, CSV och mer – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Konvertera kalkylblad"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, konvertering av kalkylblad, REST API, cURL, SDK, PDF, PNG, CSV"
description: "Lär dig hur du konverterar ett enskilt kalkylblad från en Excel-arbetsbok till PDF, PNG, CSV och mer än 15 andra format med Aspose.Cells Cloud REST API. Inkluderar cURL-exempel, SDK-utdrag och en komplett parameterreferens."
weight: 130
ArticleTitle: "Konvertera kalkylblad till PDF, PNG, CSV och mer – Aspose.Cells Cloud API"
---

**API för kalkylbladskonvertering** – slutpunkten `GET /cells/{name}/worksheets/{sheetName}` konverterar ett enskilt kalkylblad (ett ark i en Excel-arbetsbok) till en annan filtyp.

> **Förutsättning:** Du måste ha en giltig JWT-token och arbetsboken lagrad på en stödd Aspose Cloud-lagringsplats innan du anropar denna slutpunkt.

Stödda **inläsningsbara** format (kalkylbladet kan läsas från):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Stödda **endast-utmatningsbara** format (kalkylbladet kan sparas som):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## REST API

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) beskriver det offentligt tillgängliga gränssnittet.

### **Begärparametrar**

| Parameter                | Typ     | Krävs  | Standard | Tillåtna värden                                                       | Beskrivning                                      |
| ------------------------ | ------- | ------ | -------- | --------------------------------------------------------------------- | ------------------------------------------------ |
| **format**               | sträng  | Ja     | –        | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (se stödd lista)    | Målutmatningsformat.                             |
| **verticalResolution**   | heltal  | Nej    | 96       | 72‑600                                                                | Vertikal DPI för bildutmatning.                 |
| **horizontalResolution** | heltal  | Nej    | 96       | 72‑600                                                                | Horisontell DPI för bildutmatning.              |
| **password**             | sträng  | Nej    | –        | –                                                                     | Lösenord för att öppna en skyddad arbetsbok.    |
| **folder**               | sträng  | Nej    | –        | –                                                                     | Mapp i molnet där källarbetsboken lagras.        |
| **storage**              | sträng  | Nej    | –        | –                                                                     | Namn på lagringen (t.ex. "Default").             |

### Svar

| Statuskod | Beskrivning                                                            | Returtyp                   |
| --------- | ---------------------------------------------------------------------- | -------------------------- |
| **200**   | Konverteringen lyckades; binär ström av den konverterade filen returneras. | `application/octet-stream` |
| **400**   | Felaktig begäran – saknade eller ogiltiga parametrar.                 | JSON-felobjekt             |
| **401**   | Otillåten – ogiltig eller saknad JWT-token.                           | JSON-felobjekt             |
| **404**   | Hittades inte – arbetsbok eller kalkylblad finns inte.                | JSON-felobjekt             |
| **500**   | Internt serverfel – oväntat misslyckande.                              | JSON-felobjekt             |

#### Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Exempel på svar

```
Konverterad bild (binär ström)
```

## Molnsdk-familj

Att använda en sdk är det snabbaste sättet att utveckla. En sdk hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera [GitHub-repositoryt](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud sdks.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika sdks:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}
---