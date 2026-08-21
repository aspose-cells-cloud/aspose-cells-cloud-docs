---
title: "Konvertera intervall till CSV"
ArticleTitle: "Konvertera intervall till CSV – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Konvertera intervall till CSV"
type: docs
url: /cells/convert/range/csv
aliases: []
keywords: "konvertera, csv, intervall, Aspose.Cells"
description: "Konverterar ett intervall i ett kalkylark på en lokal enhet till CSV-fil."
weight: 1
---

## Konvertera intervall till CSV med Aspose.Cells Cloud-webbtjänster

Denna åtgärd läser en kalkylarksfil från det lokala filsystemet, konverterar ett angivet intervall till CSV-format och returnerar det konverterade resultatet direkt. Det fungerar helt på molnservern, så ingen mellanliggande uppladdning till molnlagring krävs. API:t stöder valfria parametrar såsom anpassade typsnitt, automatisk justering av rader/kolumner, lokaliseringsinställningar och lösenordsskyddade arbetsböcker.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### Begärparametrar

| Parameternamn    | Typ     | Path/Query String/HTTP Body | Beskrivning                                                                                                                              |
|------------------|---------|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil     | FormData                    | Ladda upp kalkylarksfil.                                                                                                                 |
| worksheet        | Sträng  | Query                       | Kalkylbladsnamn för kalkylarket. **Krävs**.                                                                                             |
| range            | Sträng  | Query                       | Cellområde. t.ex. `A1:C10`. **Krävs**.                                                                                                   |
| outPath          | Sträng  | Query                       | (Valfritt) Mappvägen där arbetsboken lagras. Standard är null.                                                                           |
| outStorageName   | Sträng  | Query                       | Lagringsnamn för utdatafilen.                                                                                                             |
| fontsLocation    | Sträng  | Query                       | Använd anpassade typsnitt.                                                                                                                |
| AutoRowsFit      | Boolean | Query                       | (Valfritt) Autojusterar alla rader i kalkylbladen.                                                                                       |
| AutoColumnsFit   | Boolean | Query                       | (Valfritt) Autojusterar alla kolumner i kalkylbladen.                                                                                    |
| region           | Sträng  | Query                       | Kalkylarkets regionspråkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifik beteende. |
| password         | Sträng  | Query                       | Lösenord för att öppna kalkylarksfilen.                                                                                                  |

### Begärandetextparameter

| Parameternamn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| Ingen | N/A | Inga parametrar i begärandetexten. |

### **Svar**

```json
{
  "ResponseFile": "binär filström (CSV-innehåll)"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|---------|-------------|
| 200 | OK | Intervallet konverterades framgångsrikt och CSV-filen returneras i svarstexten. |
| 400 | Felaktig begäran | Ogiltig URL eller saknade obligatoriska parametrar. |
| 401 | Oauktorisering | Autentisering misslyckades, eller så tillhandahölls inga autentiseringsuppgifter. |
| 413 | Payload för stor | Begärandepayloaden överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Kalkylarket stötte på ett undantag vid hämtning av konverteringsdata. |

## Hur man använder Konvertera intervall till CSV med SDK:er

### Specifikation för Konvertera intervall till CSV

[Specifikationen för Konvertera intervall till CSV API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Blad1&range=A1:C10&outPath=outputFolder&outStorageName=MinLagring&fontsLocation=/anpassade/typsnitt&AutoRowsFit=true&AutoColumnsFit=true&region=sv-SE&password=MittLösenord" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt-token>" \
  -F 'Spreadsheet=@exempel.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "Base64-kodat CSV-innehåll"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---