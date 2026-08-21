---
title: "Konvertera diagram till PDF"
ArticleTitle: "Konvertera diagram till PDF – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /cells/convert/chart/pdf
aliases: []
keywords: "Konvertera diagram till PDF, Aspose.Cells, PDF, diagramkonvertering"
description: "Konverterar ett diagram i ett kalkylark på en lokal enhet till PDF."
weight: 100
---

## Aspose.Cells Cloud Webbtjänst för att konvertera diagram till PDF

Denna metod läser ett diagram från en kalkylarksfil som skickas via lokal filuppladdning, konverterar det till PDF-format och returnerar det konverterade resultatet. Det fungerar helt på molnservern, så ingen mellanlagring krävs. Källfilens sökväg och målformat måste vara korrekta, och lämpliga behörigheter krävs för att läsa källfilen. Fel som saknade filer, åtkomstproblem eller konverteringsfel kommer att resultera i lämpliga HTTP-felsvar.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäran parametrar

| Parameter namn   | Typ    | Path/Query String/HTTP Body | Beskrivning |
|------------------|--------|-----------------------------|-------------|
| Spreadsheet      | Fil    | FormData                    | Ladda upp kalkylarkfil. |
| worksheet        | Sträng | Query                       | Kalkylbladsnamn för kalkylarket. |
| chartIndex       | Heltal | Query                       | Diagramindex i kalkylbladet. |
| outPath          | Sträng | Query                       | (Valfritt) Mappens sökväg där kalkylarket lagras. Standard är null. |
| outStorageName   | Sträng | Query                       | Lagringsnamn för utdatafilen. |
| fontsLocation    | Sträng | Query                       | Använd anpassade typsnitt. |
| region           | Sträng | Query                       | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platsspecifikt beteende. |
| password         | Sträng | Query                       | Lösenord för att öppna kalkylarkfilen. |

### Begäran kroppsparameter

| Parameter namn | Typ | Beskrivning |
| -------------- | --- | ----------- |
| Spreadsheet    | Fil | Ladda upp kalkylarkfil. |

### **Svar**

```json
{
  "ResponseFile": "binär PDF-filström"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Diagrammet konverterades framgångsrikt till PDF; binär PDF-fil returnerades. |
| 400 | Felaktig begäran | Ogiltiga begärningsparametrar eller felaktig URL. |
| 401 | Auktorisering misslyckades | Autentisering har misslyckats eller inga uppgifter har angetts. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett fel uppstod vid bearbetning av konverteringen. |

## Hur man använder Konvertera diagram till PDF med SDK:n

### Specifikation för att konvertera diagram till PDF

[Specifikationen för Konvertera diagram till PDF API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}
{< tab tabNum="1" >}
```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
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
  "ResponseFile": "binär PDF-filström"
}
```
{< /tab >}
{< /tabs >}

### Använd Aspose Cells Cloud SDK:n

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå, så att du kan fokusera på dina projektuppgifter. Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagret</a> för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:n:

`[TBD]`
---