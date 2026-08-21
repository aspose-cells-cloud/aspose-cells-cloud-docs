---
title: "Avancerad konvertering av Excel-fil"
second_title: "Dokument"
linktype: "Avancerad konvertering"
type: docs
url: /sv/advanced-convert-excel/
keywords: "Aspose.Cells, Excel-konvertering, molntjänst-API, SDK"
description: "Aspose.Cells Cloud REST API erbjuder kraftfulla funktioner för att konvertera Excel-arbetsböcker till ett brett utbud av format, samt konfigurera sidinställningar, sparaalternativ och utskriftsinställningar. SDK:er finns tillgängliga för Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift, vilket möjliggör sömlös integration på flera plattformar."
weight: 50
ArticleTitle: "Avancerad konvertering av Excel-fil – Aspose.Cells Cloud API-guide"
---

## Avancerat moln-API för Excel-konvertering

Funktionen Avancerad konvertering gör det möjligt att omvandla en Excel-arbetsbok till olika utdataformat (PDF, HTML, CSV m.fl.) samtidigt som du får detaljerad kontroll över sidinställningar, sparaalternativ och utskriftsinställningar.

**Förutsättningar / Autentisering**  
För att använda detta endpoint måste du erhålla en åtkomsttoken från Aspose.Cells Cloud och inkludera den i `Authorization`-headern som en Bearer-token.

**API-referens**  
- **Metod:** `PUT`  
- **Endpoint:** `/cells/convert`  
- **Parametrar:**  
  - `format` (sträng, obligatoriskt) – Önskat utdataformat (t.ex. `pdf`, `html`).  
  - `outPath` (sträng, valfritt) – Sökväg i molnlagringen dit den konverterade filen ska sparas.  
  - `options` (objekt, valfritt) – JSON-objekt som innehåller avancerade konverteringsalternativ såsom `pageSetup`, `saveOptions` och `printSettings`.  
- **Exempel på begäransnyttja (request body):**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Svar:**  
  - `200 OK` – Konverteringen lyckades; svaret innehåller strömmen för den konverterade filen eller en referens till den sparade filen.  
  - `400 Bad Request` – Ogiltiga parametrar eller felaktigt formaterad begäransnyttja.  
  - `401 Unauthorized` – Autentisering misslyckades eller token saknas.  
  - `500 Internal Server Error` – Serverfel under konverteringen.  

**HTTP-statuskoder**

| Kod | Betydelse                 | Beskrivning                                      |
|-----|---------------------------|--------------------------------------------------|
| 200 | OK                        | Filter tillämpades framgångsrikt; svaret innehåller detaljerad information om åtgärden. |
| 400 | Bad Request               | Saknade eller ogiltiga parametrar (t.ex. filformat som inte stöds). |
| 401 | Unauthorized              | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large         | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error     | Oväntat serverfel. |

**Anteckningar**  
* Vissa utdataformat har specifika begränsningar (t.ex. HTML-konvertering bevarar inte makron). Se format-specifik dokumentation för detaljerad information.

### Möjligheten att ladda kalkylark från flera datakällor

### Ställ in sidinställningar och sparaalternativ

## Moln-SDK-familj

Att använda en SDK hjälper till att påskynda utvecklingen genom att hantera lågnivådetaljer, så att du kan fokusera på dina projektuppgifter. Besök <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förvaret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud avancerad konvertering",
  "description":"Konvertera en Excel-arbetsbok till PDF/HTML/CSV med avancerade alternativ.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Önskat utdataformat (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>
---