---
title: "ConvertRangeToPdf"
ArticleTitle: "Konvertera intervall till PDF – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "ConvertRangeToPdf"
type: docs
url: /sv/cells/convert/range/pdf
aliases: []
keywords: "Aspose.Cells, Konvertera intervall till PDF, API"
description: "Konverterar ett angivet intervall i ett kalkylark till PDF med Aspose.Cells Cloud."
weight: 1
---

## ConvertRangeToPdf hos Aspose.Cells Cloud Webbtjänster

Konverterar ett intervall i ett kalkylark från en lokal enhet till en PDF-fil.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn     | Typ    | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                                     |
|-------------------|--------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet       | Fil    | FormData                     | Ladda upp kalkylarksfil.                                                                                                                        |
| worksheet         | Sträng | Fråga                        | Kalkylarkets namn.                                                                                                                             |
| range             | Sträng | Fråga                        | Cellområde. t.ex. A1:C10                                                                                                                        |
| outPath           | Sträng | Fråga                        | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standardvärdet är null.                                                                |
| outStorageName    | Sträng | Fråga                        | Lagringsnamn för utdatafilen.                                                                                                                   |
| fontsLocation     | Sträng | Fråga                        | Använd anpassade typsnitt.                                                                                                                      |
| AutoRowsFit       | Boolean| Fråga                        | (Valfritt) Justera automatiskt alla rader i kalkylarken.                                                                                       |
| AutoColumnsFit    | Boolean| Fråga                        | (Valfritt) Justera automatiskt alla kolumner i kalkylarken.                                                                                    |
| region            | Sträng | Fråga                        | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och lokalbaserat beteende.     |
| password          | Sträng | Fråga                        | Lösenord för att öppna kalkylarksfilen.                                                                                                        |

### Begärcodeparametrar

| Parameternamn | Typ | Beskrivning |
|---------------|-----|-------------|
| Spreadsheet   | Fil | Ladda upp kalkylarksfil. |

### **Svar**

```json
{
  "file": "<binärt PDF-innehåll>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Lyckad konvertering; returnerar den genererade PDF-filströmmen. |
| 400 | Felaktig begäran | Ogiltig URL. |
| 401 | Otillåten | Autentisering misslyckades, eller så angavs inga autentiseringsuppgifter. |
| 413 | Payload för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid hämtning av konverteringsdata. |

## Hur du använder ConvertRangeToPdf med SDK:er

### ConvertRangeToPdf-specifikation

[ConvertRangeToPdf API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPdf) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för att enkelt komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Blad1&range=A1:C10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binärt PDF-innehåll>"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher undan lågnivådetaljer och låter dig fokusera på dina projekts uppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:

```csharp
// SDK-exempelkod för C#
var apiInstance = new ConversionApi();
var file = File.OpenRead("sample.xlsx");
var result = apiInstance.ConvertRangeToPdf(file, "Blad1", "A1:C10", outPath: null, outStorageName: null, fontsLocation: null, autoRowsFit: null, autoColumnsFit: null, region: null, password: null);
File.WriteAllBytes("output.pdf", result);
```

```java
// SDK-exempelkod för Java
ConversionApi api = new ConversionApi();
File file = new File("sample.xlsx");
byte[] result = api.convertRangeToPdf(file, "Blad1", "A1:C10", null, null, null, null, null, null, null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# SDK-exempelkod för Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    result = api_instance.convert_range_to_pdf(f, worksheet="Blad1", range="A1:C10")
    with open("output.pdf", "wb") as out_file:
        out_file.write(result)
```

```javascript
// SDK-exempelkod för JavaScript/Node.js
const fs = require('fs');
const { ConversionApi } = require('asposecellscloud');
const apiInstance = new ConversionApi();

let file = fs.createReadStream('sample.xlsx');
apiInstance.convertRangeToPdf(file, { worksheet: 'Blad1', range: 'A1:C10' })
    .then((result) => {
        fs.writeFileSync('output.pdf', result);
    })
    .catch((error) => console.error(error));
```

`[TBD]`