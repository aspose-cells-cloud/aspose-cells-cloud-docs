---
title: "Komprimera data i en Excel-fil"
ArticleTitle: "Komprimera data i en Excel-fil – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Komprimera Excel-filer"
type: docs
url: /compress-excel-files/
aliases: [/compress/]
keywords: "komprimera excel-fil, aspose cells cloud, excel-komprimering, kalkylarkskomprimering, rest-api, filkomprimering"
description: "Komprimera Excel-filer (XLS, XLSX, XLSM, XLSB, ODS) med Aspose.Cells Cloud REST API. Ställ in komprimeringsnivå, hantera flera filer och integrera via SDK:er."
weight: 39
---

## PostCompress API för Aspose.Cells Cloud Webbtjänster

**Förutsättningar:**  
- Ett giltigt JWT-token krävs för autentisering.  
- Stödda filformat är XLS, XLSX, XLSM, XLSB och ODS.  
- Den maximalt tillåtna filstorleken är 500 MB per förfrågan (beroende på tjänstebegränsningar).

Denna REST API komprimerar data i en Excel-fil.

- Komprimera XLS, XLSX, XLSM, XLSB, ODS  
- Komprimera snabbt flera Excel-kalkylarksfiler  
- Välj komprimeringsnivå  
- Stöd för flera filer

### Web API-slutpunkt

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Förfrågningsparametrar

| Parametername   | Typ   | Path/Query String/HTTP Body | Beskrivning                                        |
|-----------------|-------|-----------------------------|----------------------------------------------------|
| file            | fil   | formData                    | Fil som ska laddas upp                             |
| CompressLevel   | heltal | query                       | Komprimeringsnivå (0‑100); högre värden betyder starkare komprimering |

### Parameter i begärandetexten

| Parametername | Typ | Beskrivning                                   |
| ------------- | --- | --------------------------------------------- |
| data          | fil | Binärt innehåll i arbetsbokensfil som ska komprimeras. |

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[sammanslagningsfilnamn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

*Obs:* `FileContent` innehåller den komprimerade arbetsboken kodad som en Base64-sträng. Strängens längd motsvarar storleken på den komprimerade filen; du kan avkoda den med standardverktyg för Base64 för att få tillbaka den binära Excel-filen.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltigt eller saknat JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## Hur du använder PostCompress API med SDK:er

### PostCompress API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraherar lågnivådetaljer så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}