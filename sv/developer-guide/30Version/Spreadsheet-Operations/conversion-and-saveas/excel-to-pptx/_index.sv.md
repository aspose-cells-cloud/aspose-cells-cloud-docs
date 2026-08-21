---
title: "Konvertera Excel till PPTX med Aspose.Cells Cloud API v3.0"
second_title: "Dokument"
linktitle: "Excel till PPTX"
type: docs
url: /convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, konvertering, REST API, moln"
description: "Lär dig hur du konverterar Excel-arbetsböcker till PPTX-presentationer med Aspose.Cells Cloud REST API v3.0. Innehåller cURL-förfrågan, SDK-kodexempel, autentisering och felhantering."
weight: 90
ArticleTitle: "Konvertera Excel till PPTX med Aspose.Cells Cloud API v3.0"
---

Denna REST API konverterar en kalkylarkfil till PPTX-format.

## PostConvertWorkbookToPptx API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Frågeparametrar

| Parameter namn          | Typ    | Beskrivning                                                                                  |
| ----------------------- | ------ | -------------------------------------------------------------------------------------------- |
| `password`              | string | Lösenord som krävs för att öppna Excel-arbetsboken.                                          |
| `storageName`           | string | Namn på lagringsutrymmet där källfilen finns.                                                |
| `checkExcelRestriction` | bool   | Anger om Excel-filbegränsningar ska tvingas på när cellrelaterade objekt ändras.            |

### Parameter för begärandetext

| Parameter namn | Typ       | Beskrivning                                                       |
| -------------- | --------- | ----------------------------------------------------------------- |
| `datafile`     | datafil   | Excel-filen som ingår i första delen av multipart-begärandetexten. |

**Exempel på multipart-begärandetext (förenklad):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<binärt innehåll i input.xlsx>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Svar

API:et returnerar ett **FileInfo**-objekt som innehåller den genererade PPTX-filen.

| Fält            | Typ    | Beskrivning                                      |
| --------------- | ------ | ------------------------------------------------ |
| **Filename**    | string | Namn på PPTX-filen (t.ex. `exempel.pptx`).       |
| **FileSize**    | int    | Filens storlek i byte.                           |
| **FileContent** | string | Base64-kodat innehåll i PPTX-filen.              |

[FileInfo](/cells/file-info/)


**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 200 | OK                          | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).           |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                                             |
| 413 | Begärandetext för stor      | Den uppladdade filen överskrider storleksgränsen.                          |
| 500 | Internt serverfel           | Oväntat serverfel.                                                          |

*Anteckningar:* Slutpunkten stöder vanliga Excel-format (`.xlsx`, `.xls`, `.xlsm`). Den maximala filstorleken är begränsad till 50 MB. Konvertering kan vara begränsad för arbetsböcker som innehåller makron eller skyddade blad om lämpliga parametrar inte tillhandahålls.

## Hur du använder PostConvertWorkbookToPptx API med SDK:er

### PostConvertWorkbookToPptx API-specifikation

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Exemplet nedan visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exempel.pptx",
  "FileSize": 123456,
  "FileContent": "Filinnehåll: base64-kodad_sträng"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på ditt projekt. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API:er som implementerar denna funktion

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Konverterar en Excel-fil till PDF.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Konverterar en Excel-fil till PNG-bilder.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Konverterar en Excel-fil till SVG-format.