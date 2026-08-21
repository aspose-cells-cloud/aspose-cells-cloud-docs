---
title: "Konvertera tabell till CSV"
ArticleTitle: "Konvertera tabell till CSV – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Konvertera tabell till CSV"
type: docs
url: /sv/cells/convert/table/csv
aliases: []
keywords: "Konvertera tabell till CSV, Aspose.Cells, molntjänst"
description: "Konverterar en tabell i ett kalkylark på en lokal enhet till en CSV-fil."
weight: 1
---

## Konvertera tabell till CSV med Aspose.Cells Cloud-webbtjänster

Denna metod läser en kalkylarksfil från det lokala filsystemet, konverterar den angivna tabellen till en CSV-fil och returnerar det konverterade resultatet. Den fungerar helt och hållet på molnservern, så ingen mellanliggande uppladdning till molnlagring krävs. Källfilens sökväg och målformat måste anges korrekt, och lämpliga behörigheter krävs för att läsa källfilen. Fel som saknade filer, otillgängliga sökvägar eller misslyckade konverteringar leder till lämpliga undantag.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| ParameterNamn    | Typ    | Sökväg/Frågesträng/HTTP-kropp | Beskrivning |
|------------------|--------|-------------------------------|-------------|
| Spreadsheet      | Fil    | FormData                      | Ladda upp kalkylarksfil. |
| worksheet        | Sträng | Fråga                         | Kalkylbladsnamn för kalkylarket. |
| tableName        | Sträng | Fråga                         | Tabellnamn |
| outPath          | Sträng | Fråga                         | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standardvärdet är null. |
| outStorageName   | Sträng | Fråga                         | Lagringsnamn för utdatafilen. |
| fontsLocation    | Sträng | Fråga                         | Använd anpassade typsnitt. |
| AutoRowsFit      | Boolean| Fråga                         | (Valfritt) Justera automatiskt alla rader i kalkylbladen. |
| AutoColumnsFit   | Boolean| Fråga                         | (Valfritt) Justera automatiskt alla kolumner i kalkylbladen. |
| region           | Sträng | Fråga                         | Inställning för region/språk för kalkylarket (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifika beteenden. |
| password         | Sträng | Fråga                         | Lösenord för att öppna kalkylarksfilen. |

### Parameter för begäronsbruk (Request Body)

| ParameterNamn | Typ | Beskrivning |
| ------------- | --- | ----------- |
| *Ingen* | *Ingen* | *Ingen begärosbruk krävs; filen skickas som multipart/form-data.* |

### **Svar**

```json
{
  "file": "binär ström av den genererade CSV-filen"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Tabellen konverterades framgångsrikt och CSV-filen returneras. |
| 400 | Felaktig begäran | Ogiltiga parametrar eller felaktigt formaterad URL. |
| 401 | Auktorisering krävs | Autentisering misslyckades eller inga autentiseringsuppgifter angavs. |
| 404 | Hittades inte | Källfilen är inte tillgänglig eller existerar inte. |
| 413 | Payload för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett fel uppstod i kalkylarket under konverteringen. |

## Hur man använder Konvertera tabell till CSV med SDK:er

### Specifikation för Konvertera tabell till CSV

[Specifikationen för Konvertera tabell till CSV API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCsv) definierar ett offentligt tillgängligt programmeringsgränssnitt och tillåter dig att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet={worksheet}&tableName={tableName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&AutoRowsFit={AutoRowsFit}&AutoColumnsFit={AutoColumnsFit}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "binär ström av den genererade CSV-filen"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher undan lågnivådetaljer, så att du kan fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells Cloud-webbtjänster med hjälp av olika SDK:er:
`[TBD]`
---