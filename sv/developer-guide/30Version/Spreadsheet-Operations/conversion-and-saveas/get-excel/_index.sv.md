---
title: "Aspose.Cells Cloud – Konvertera Excel-arbetsbok till PDF, CSV, HTML och mer (GET /cells/{name})"
second_title: "Dokument"
linktitle: "Konvertera Excel"
type: docs
url: /get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel-konvertering, konvertera Excel, PDF, CSV, HTML, ODS, JSON, bildformat, kalkylarksexport, API, REST"
description: "Lär dig hur du hämtar en Excel-arbetsbok i valfritt format (PDF, CSV, HTML, PNG, etc.) med Aspose.Cells Cloud REST API. Inkluderar cURL- och SDK-exempel, autentisering och svarsinformation."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Konvertera Excel-arbetsbok till PDF, CSV, HTML och mer (GET /cells/{name})"
---

Denna REST API hämtar en Excel-arbetsbok i ett annat format.

## GetWorkBook API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Frågeparametrar**

| Parameter_name        | Typ    | Beskrivning                                                                                                                                                           | Standardvärde |
| --------------------- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| format                | string | Mål-filformat (t.ex. CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG, etc.).      | –             |
| password              | string | Lösenord som krävs för att öppna Excel-filen.                                                                                                                         | –             |
| isAutoFit             | bool   | Justerar automatiskt rad- och kolumnbredd.                                                                                                                            | false         |
| onlySaveTable         | bool   | När **true** sparas endast tabelldata. Accepterar `true` eller `false`.                                                                                              | false         |
| outPath               | string | Sökväg för att spara resultatet. För en enskild fil inkludera filnamn och filtillägg; för flera filer ange endast mappnamn.                                          | –             |
| outStorageName        | string | Namn på lagringen dit utdatafilen ska sparas.                                                                                                                        | –             |
| checkExcelRestriction | bool   | Kontrollerar Excel-begränsningar vid ändring av celler eller relaterade objekt.                                                                                      | false         |
| region                | string | Regionala inställningar som tillämpas på arbetsboken.                                                                                                                 | –             |
| pageWideFitOnPerSheet | bool   | Anpassar sidbredden till varje kalkylblad vid konvertering till PDF.                                                                                                 | false         |
| pageTallFitOnPerSheet | bool   | Anpassar sidhöjden till varje kalkylblad vid konvertering till PDF.                                                                                                  | false         |
| onePagePerSheet       | bool   | Skapar en PDF-sida per kalkylblad.                                                                                                                                    | false         |
| folder                | string | Mappsökväg för den ursprungliga arbetsboken.                                                                                                                          | –             |
| storageName           | string | Namn på lagringen där källfilen finns.                                                                                                                                | –             |

### Svar

**Lyckades (200)**

- API:n returnerar ett **[Workbook](/cells/workbook/)**-objekt som innehåller arbetsbokens strukturinformation när `format`-frågeparametern utelämnas.

- API:n returnerar den konverterade filen i det begärda formatet när `format`-frågeparametern anger ett filtyp.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(binär PDF-data)
```

**HTTP-statuskoder**

| Kod | Betydelse                  | Beskrivning                                              |
|-----|----------------------------|----------------------------------------------------------|
| 200 | OK                         | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Ogiltig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. ej stött filformat). |
| 401 | Auktorisering misslyckades | Ogiltig eller saknad JWT-token.                          |
| 413 | För stor nyttolast         | Uppladdad fil överskrider storleksgränsen.               |
| 500 | Internt serverfel          | Oväntat serverfel.                                       |

> **Anteckningar:**  
> - Stora arbetsböcker kan ta längre tid att konvertera; överväg att öka förfrågningstimeout.  
> - Vissa format (t.ex. `ODS`) stöds inte för vissa Excel-funktioner såsom makron.

## Hur du använder GetWorkBook API med SDK:er

> **Förutsättningar:**  
> - En giltig **JWT-åtkomsttoken** erhållen via Aspose.Cells-autentisering.  
> - Källarbetsboken måste lagras i en stödd Aspose-lagring eller direkt anges i förfrågan.  
> - Kontrollera att API-versionen (`v3.0`) matchar den senast släppta versionen.

### GetWorkBook API-specificering

<a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI-specificeringen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Exempelförfrågan

Du kan använda kommandoradsverktyget **cURL** för att komma åt Aspose.Cells webbtjänster. Följande exempel visar en korrekt GET-förfrågan med nödvändigt auktoriseringshuvud.

{{< tabs tabTotal="1" tabID="11" tabName11="Förfrågan" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Konvertera arbetsbok (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Spara som (GET)</a>

---

**Senast uppdaterad: 2024-12-01**

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Konvertera Excel-arbetsbok till PDF, CSV, HTML och mer (GET /cells/{name})",
  "description": "Dokumentation för Aspose.Cells Cloud GET /cells/{name}-slutpunkten som konverterar Excel-arbetsböcker till olika format såsom PDF, CSV, HTML och mer.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel-konvertering, PDF, CSV, HTML, API, REST, moln",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>
---