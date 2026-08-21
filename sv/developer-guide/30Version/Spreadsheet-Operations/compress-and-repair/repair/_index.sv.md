---
title: "Reparera Excel-filer"
second_title: "Dokument"
type: docs
linktitle: "Reparera Excel-filer"
url: /sv/repair-excel-files/
keywords: "Aspose Cells, Excel-reparations-API, korrupt XLSX, återställning av kalkylark, moln-API"
description: "Använd Aspose.Cells Cloud REST API för att reparera korrupta Excel-filer (XLS, XLSX, XLSM, XLSB, ODS). Ladda upp en eller flera filer, välj utdataformat och få tillbaka reparerade filer i Base64-format. Ingen installation krävs."
weight: 39
---

Detta REST API låter dig **reparera** Excel-filer.

- Reparera XLS, XLSX, XLSM, XLSB, ODS och andra kalkylarksformat.  
- Stöder uppladdning av flera filer i en enda begäran.

Aspose.Cells Cloud Excel-reparation återställer data från korrupta Excel-filer online utan någon installation. Korrupta Excel-filer är problematiska eftersom de inte kan öppnas. Du kan testa Aspose.Cells Cloud Excel-reparationsappen för att återställa data från sådana filer.

## REST API

Endpointen **Repair Excel Files** reparerar korrupta kalkylarksfiler och returnerar det reparerade innehållet.


```bash
POST https://api.aspose.cloud/v3.0/cells/repair
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameternamn | Typ   | Plats                        | Beskrivning |
|---------------|-------|------------------------------|-------------|
| file          | fil   | formData (multipart)         | Fil att ladda upp |
| format        | sträng | frågeparameter                | Önskat utdataformat. Om den utelämnas (null) blir utdataformatet samma som indatafilens format. |

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[sammanfogat filnamn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                     |
|-----|-----------------------------|-------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |
## Hur man använder PostRepair API med SDK:er

### PostRepair API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/LightCells/PostRepair) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/repair" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@file1.xlsx' \
  -F 'file2=@file2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    },
    {
      "Filename": "file2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

Vid lyckad åtgärd returnerar tjänsten HTTP 200 med en JSON-payload som innehåller en `Files`-array. Vid felaktiga situationer använder API:et standard HTTP-statuskoder:

- **400 Bad Request** – Ogiltiga parametrar eller fil som inte går att återställa.  
- **401 Unauthorized** – Saknad eller ogiltig JWT-token.  
- **413 Payload Too Large** – Den uppladdade filen överskrider den tillåtna storleken.  
- **500 Internal Server Error** – Oväntat serverfel.

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostRepair.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostRepair.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostRepair.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostRepair.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostRepair.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostRepair.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostRepair.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostRepair.go" >}}

{{< /tab >}}

{{< /tabs >}}