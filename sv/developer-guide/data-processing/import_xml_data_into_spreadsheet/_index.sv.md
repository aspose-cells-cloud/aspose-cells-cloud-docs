---
title: "Importera XML-data till kalkylark"
ArticleTitle: "Importera XML-data till kalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Importera XML-data till kalkylark"
type: docs
url: /cells/import/data/xml
aliases: []
keywords: "Importera XML, Aspose.Cells, API"
description: "Importera XML-datafil till lokalt kalkylark med Aspose.Cells Cloud."
weight: 1000
---

## Importera XML-data till kalkylark med Aspose.Cells Cloud-webbtjänster

Importera XML-datafil till lokalt kalkylark. Metoden parserar XML, mappar data till kalkylarkets cellstruktur och sparar filen lokalt. Stödda kalkylarksformat inkluderar .xlsx och .ods.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/xml
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parametername    | Typ     | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                            |
|------------------|---------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| datafile         | Fil     | FormData                     | Ladda upp datafil.                                                                                                                     |
| Spreadsheet      | Fil     | FormData                     | Ladda upp kalkylarksfil.                                                                                                              |
| worksheet        | Sträng  | Fråga                        | Kalkylbladet där XML-data ska importeras.                                                                                             |
| startcell        | Sträng  | Fråga                        | Startposition för dataimport                                                                                                         |
| insert           | Boolean | Fråga                        | Kontrollerar infogningsbeteendet. true: infogar data; false: skriver över befintlig data. Standard: **true**                         |
| outPath          | Sträng  | Fråga                        | (Valfritt) Mappsökvägen där arbetsboken lagras. Standard är null.                                                                    |
| outStorageName   | Sträng  | Fråga                        | Lagringsnamn för utdatafil.                                                                                                           |
| fontsLocation    | Sträng  | Fråga                        | Använd anpassade typsnitt.                                                                                                            |
| region           | Sträng  | Fråga                        | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platsspecifikt beteende. |
| password         | Sträng  | Fråga                        | Lösenord för att öppna kalkylarksfilen.                                                                                               |

### Begärobjektparameter

| Parametername | Typ | Beskrivning |
|---------------|-----|-------------|
| *Ingen*       | -   | -           |

### **Svar**

```json
{
  "file": "<binär ström av den uppdaterade kalkylarksfilen>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse               | Beskrivning                                                                                           |
|-----|-------------------------|-------------------------------------------------------------------------------------------------------|
| 200 | OK                      | XML-data importerades framgångsrikt och den uppdaterade kalkylarksfilen returneras.                 |
| 400 | Felaktig förfrågan      | Ogiltig URL eller saknade obligatoriska parametrar.                                                  |
| 401 | Auktorisering misslyckades | Autentiseringen har misslyckats, eller så fanns inga inloggningsuppgifter.                          |
| 404 | Hittades inte           | Källfilen är inte tillgänglig.                                                                        |
| 413 | Payload för stor        | Den uppladdade filen överskrider den tillåtna storleksgränsen.                                       |
| 500 | Internt serverfel       | Ett fel uppstod i servern vid hämtning av data.                                                      |

## Hur du använder Importera XML-data till kalkylark med SDK:er

### Importera XML-data till kalkylark – specifikation

[Importera XML-data till kalkylark API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{DataProcessingController}/ImportXMLDataIntoSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/xml?worksheet={worksheet}&startcell={startcell}&insert={insert}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@{DataFileName}" \
  -F "Spreadsheet=@{SpreadsheetFileName}"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binär ström av den uppdaterade kalkylarksfilen>"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med diverse SDK:er:
`[TBD]`
---