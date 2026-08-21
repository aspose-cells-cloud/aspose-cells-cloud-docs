---
title: "Konvertera tabell till PDF"
ArticleTitle: "Konvertera tabell till PDF – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Konvertera tabell till PDF"
type: docs
url: /cells/convert/table/pdf
aliases: []
keywords: "Konvertera tabell till PDF, Aspose.Cells, API"
description: "Konverterar en tabell i ett kalkylark på en lokal enhet till en PDF-fil med Aspose.Cells Cloud."
weight: 1000
---

## Aspose.Cells Clouds webbtjänst för att konvertera tabell till PDF

Denna åtgärd läser en kalkylarksfil från det lokala filsystemet, konverterar den angivna tabellen till ett PDF-dokument och returnerar det konverterade resultatet. Det fungerar helt på molnservern, så ingen mellanliggande uppladdning till molnlagring krävs. API:t stöder valfria parametrar för utdataplats, anpassade typsnitt, automatisk justering av rader/kolumner, regionala inställningar och lösenordsskyddade arbetsböcker.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Clouds API är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### Begärparametrar

| Parameternamn    | Typ    | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                                                     |
|------------------|--------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil    | FormData                     | Ladda upp kalkylarksfil.                                                                                                                                        |
| worksheet        | Sträng | Fråga                        | Kalkylbladsnamn för kalkylarket.                                                                                                                                |
| tableName        | Sträng | Fråga                        | Tabellnamn.                                                                                                                                                      |
| outPath          | Sträng | Fråga                        | (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.                                                                                         |
| outStorageName   | Sträng | Fråga                        | Lagringsnamn för utdatafilen.                                                                                                                                    |
| fontsLocation    | Sträng | Fråga                        | Använd anpassade typsnitt.                                                                                                                                       |
| AutoRowsFit      | Boolean| Fråga                        | (Valfritt) Autojusterar alla rader i kalkylblad.                                                                                                               |
| AutoColumnsFit   | Boolean| Fråga                        | (Valfritt) Autojusterar alla kolumner i kalkylblad.                                                                                                            |
| region           | Sträng | Fråga                        | Region/språkinställning för kalkylarket (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och lokalberoende beteende.              |
| password         | Sträng | Fråga                        | Lösenord för att öppna kalkylarksfilen.                                                                                                                         |

### Begärandetextparameter

| Parameternamn | Typ | Beskrivning |
|---------------|-----|-------------|
| *Ingen*       | *Ingen* | *Ingen JSON-body krävs; filen skickas via multipart/form-data.* |

### **Svar**

```json
{
  "file": "<binärt PDF-innehåll>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Tabellen konverterades framgångsrikt till PDF; svarstexten innehåller PDF-filströmmen. |
| 400 | Ogiltig begäran | Ogiltiga begärparametrar eller felaktig URL. |
| 401 | Otillåten | Autentiseringen misslyckades eller inga uppgifter angavs. |
| 404 | Hittades inte | Källfilen är inte tillgänglig eller så kunde kalkylbladet/tabellen inte hittas. |
| 413 | För stor nyttoinformation | Den uppladdade kalkylarksfilen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett fel uppstod vid konvertering av kalkylarket till PDF. |

## Hur man använder konvertering av tabell till PDF med SDK:er

### Specifikation för konvertering av tabell till PDF

[API-specifikationen för konvertering av tabell till PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPdf) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells Clouds webbtjänster. Följande exempel visar hur du gör anrop till moln-API:t med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells Clouds webbtjänster med olika SDK:er:
```csharp
// Exempelkod för SDK i C#
var apiInstance = new ConversionApi();
var file = File.ReadAllBytes("sample.xlsx");
var response = apiInstance.ConvertTableToPdf(
    file,
    worksheet: "Sheet1",
    tableName: "Table1",
    outPath: null,
    outStorageName: null,
    fontsLocation: null,
    AutoRowsFit: null,
    AutoColumnsFit: null,
    region: null,
    password: null);
File.WriteAllBytes("output.pdf", response);
```

```java
// Exempelkod för SDK i Java
ConversionApi apiInstance = new ConversionApi();
byte[] file = Files.readAllBytes(Paths.get("sample.xlsx"));
byte[] result = apiInstance.convertTableToPdf(
    file,
    "Sheet1",
    "Table1",
    null,
    null,
    null,
    null,
    null,
    null,
    null);
Files.write(Paths.get("output.pdf"), result);
```

```python
# Exempelkod för SDK i Python
api_instance = conversion_api.ConversionApi()
with open("sample.xlsx", "rb") as f:
    file_bytes = f.read()
pdf_bytes = api_instance.convert_table_to_pdf(
    file=file_bytes,
    worksheet="Sheet1",
    table_name="Table1")
with open("output.pdf", "wb") as out_file:
    out_file.write(pdf_bytes)
```

`[TBD]`
---