---
title: "Lägg till vattenmärke i Excel-filer"
second_title: "Dokument"
linktitle: "Lägg till vattenmärke i Excel-filer"
type: docs
url: /sv/add-watermark-into-excel-files/
aliases: [  /sv/watermark/ ]
keywords: "lägg till vattenmärke i Excel, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Lär dig hur du lägger till ett textvattenmärke i Excel-arbetsböcker med Aspose.Cells Cloud REST API (v3.0). Innehåller cURL-exempel, nödvändiga parametrar och svarsinformation."
weight: 39
ArticleTitle: "Lägg till vattenmärke i Excel-filer – Aspose.Cells Cloud-dokumentation"
---

Detta REST API lägger till ett **vattenmärke** i Excel-filer.

**Förutsättningar:** Du måste skaffa en giltig JWT-åtkomsttoken och se till att Excel-filen är i ett format som stöds (t.ex. `.xlsx`, `.xls`).  
**Bakgrund:** Ett vattenmärke är en halvtransparent textöverlagring som appliceras på varje kalkylblad för att indikera ägarskap eller sekretess.

## PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameternamn | Typ   | Plats                     | Beskrivning                                                 |
| ------------- | ----- | ------------------------- | ----------------------------------------------------------- |
| `file`        | fil   | formData (multipart body) | Excel-filen som vattenmärket ska appliceras på.             |
| `text`        | sträng | query                     | Den text som ska visas som vattenmärke.                     |
| `color`       | sträng | query                     | Vattenmärkets färg i ARGB-hexformat (t.ex. `004433ff`).     |

### **Svar**

JSON-svaret innehåller en **Files**-array. För varje filobjekt:

- **Filename** – namn på den bearbetade arbetsboken.  
- **FileSize** – filens storlek i byte.  
- **FileContent** – Base64-kodat innehåll i den vattenmärkta Excel-filen; avkoda denna för att få fram den faktiska filen.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[fil1-namn]",
            "Filesize" : [filstorlek],
            "FileContent" : "[Base64-sträng]"
        },
        {
            "Filename" : "[fil2-namn]",
            "Filesize" : [filstorlek],
            "FileContent" : "[Base64-sträng]"
        },
        {
            "Filename" : "[fil3-namn]",
            "Filesize" : [filstorlek],
            "FileContent" : "[Base64-sträng]"
        }
    ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Vattenmärket tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttoinformation   | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur man använder PostWatermark API med SDK:er

### PostWatermark API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells webbtjänster. Exemplet nedan visar en komplett begäran, inklusive den nödvändiga autentiseringshuvudet. Ersätt `<your-jwt-token>` med en giltig JWT-åtkomsttoken som du har erhållit från Asposes autentiseringsändpunkt.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att utveckla på. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på din affärslogik. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}