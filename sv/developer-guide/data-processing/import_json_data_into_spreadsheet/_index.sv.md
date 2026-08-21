---
title: "Importera JSON-data till kalkylark"
ArticleTitle: "Importera JSON-data till kalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Importera JSON-data till kalkylark"
type: docs
url: /cells/import/data/json
aliases: []
keywords: "Importera JSON, Aspose.Cells, Kalkylark, API"
description: "Importera JSON-datafil till det lokala kalkylarket."
weight: 1
---

## Importera JSON-data till kalkylark med Aspose.Cells Cloud-webbtjänster

Importera JSON-datafil till det lokala kalkylarket. Metoden tolkar JSON, mappar data till kalkylarkets cellstruktur och sparar filen lokalt. Stödda kalkylarksformat inkluderar .xlsx och .ods.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/json
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-body | Beskrivning |
|--------------|-------|------------------------------|-------------|
| datafile     | Fil   | FormData                     | Ladda upp datafil. |
| Spreadsheet  | Fil   | FormData                     | Ladda upp kalkylarkfil. |
| worksheet    | sträng | Fråga                        | Kalkylarket där JSON-data ska importeras. |
| startcell    | sträng | Fråga                        | Startposition för dataimport |
| insert       | boolean | Fråga                      | Kontrollerar infogningsbeteende. true: infogar data; false: skriver över befintlig data. (Standard: true) |
| outPath      | sträng | Fråga                        | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standardvärdet är null. |
| outStorageName | sträng | Fråga                     | Lagringsnamn för utdatafil. |
| fontsLocation | sträng | Fråga                       | Använd anpassade typsnitt. |
| region       | sträng | Fråga                        | Kalkylarkets region/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifikt beteende. |
| password     | sträng | Fråga                        | Lösenord för att öppna kalkylarkfilen. |

### Begärobjektparameter

| Parameternamn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Svar**

```json
{
  "file": "binär ström"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Filen genererades och returnerades utan fel. |
| 400 | Felaktig begäran | Ogiltig URL. |
| 401 | Otillåten | Autentiseringen misslyckades, eller så angavs inga autentiseringsuppgifter. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | För stor nyttolast | [TBD] |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid hämtning av data. |

## Hur du använder Importera JSON-data till kalkylark med SDK:er

### Importera JSON-data till kalkylark – specifikation

[Importera JSON-data till kalkylark API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportJSONDataIntoSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för enkelt att komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}
{< tab tabNum="1" >}
```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/json?worksheet=Blad1&startcell=A1&insert=true&outPath=output%2F&outStorageName=MyStorage&fontsLocation=%2Ffonts&region=sv-SE&password=Secret" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "datafile=@data.json" \
  -F "Spreadsheet=@workbook.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "file": "binär ström"
}
```
{< /tab >}
{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher undan lågnivådetaljer och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---