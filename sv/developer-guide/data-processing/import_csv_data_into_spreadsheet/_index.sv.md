---
title: "Importera CSV-data till kalkylark"
ArticleTitle: "Importera CSV-data till kalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Importera CSV-data till kalkylark"
type: docs
url: /sv/cells/import/data/csv
aliases: []
keywords: "Aspose.Cells, CSV-import, kalkylark, API"
description: "Importera CSV-datafil till lokalt kalkylark med Aspose.Cells Cloud API."
weight: 100
---

## Importera CSV-data till kalkylark via Aspose.Cells Cloud-webbtjänster

Importera CSV-datafil till lokalt kalkylark. Metoden parsar CSV-filen, mappar data till kalkylarkets cellstruktur och sparar filen lokalt. Stödda kalkylarksformat inkluderar .xlsx och .ods.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data/csv
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärningsparametrar

| Parameternamn         | Typ    | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning                                                                                                                          |
|-----------------------|--------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| datafile              | Fil    | FormData                         | Ladda upp datafil.                                                                                                                    |
| Spreadsheet           | Fil    | FormData                         | Ladda upp kalkylarksfil.                                                                                                             |
| worksheet             | Sträng | Frågesträng                      | Kalkylarket som CSV-data ska importeras till. (obligatorisk)                                                                        |
| startcell             | Sträng | Frågesträng                      | Startposition för dataimport. (obligatorisk)                                                                                        |
| insert                | Boolean | Frågesträng                     | Styr insättningsbeteendet. true: infogar data; false: skriver över befintlig data. Standard: true (valfritt)                        |
| convertNumericData    | Boolean | Frågesträng                     | Om strängar i textfilen ska konverteras till numerisk data. Standard: true (valfritt)                                               |
| splitter              | Sträng | Frågesträng                      | Avgränsare som används för att dela upp CSV-fält. Standard: "," (valfritt)                                                           |
| outPath               | Sträng | Frågesträng                      | (Valfritt) Mappsökvägen där arbetsboken lagras. Standard är null (valfritt).                                                        |
| outStorageName        | Sträng | Frågesträng                      | Lagringsnamn för utdatafil. (valfritt)                                                                                               |
| fontsLocation         | Sträng | Frågesträng                      | Använd anpassade typsnitt. (valfritt)                                                                                                |
| region                | Sträng | Frågesträng                      | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och regional beteende. (valfritt) |
| password              | Sträng | Frågesträng                      | Lösenord för att öppna kalkylarksfilen. (valfritt)                                                                                  |

### Brödtextparameter för begäran

| Parameternamn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Svar**

```json
{
  "file": "<binär ström för det resulterande kalkylarket>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|-----------|-------------|
| 200 | OK | CSV-data har importerats utan problem och det resulterande kalkylarksfilen returneras. |
| 400 | Felaktig begäran | Ogiltiga begärningsparametrar eller felaktig URL. |
| 401 | Ej auktoriserad | Autentiseringen misslyckades, eller inga autentiseringsuppgifter har angivits. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | Payload för stor | De uppladdade filerna överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid hämtning av data. |

## Hur du använder Importera CSV-data till kalkylark med SDK:er

### Specifikation för Importera CSV-data till kalkylark

[Importera CSV-data till kalkylark API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/ImportCSVDataIntoSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/import/data/csv?worksheet=Blad1&startcell=A1&insert=true&convertNumericData=true&splitter=,&outPath=utdataMapp&outStorageName=MinLagring&fontsLocation=/anpassade/typsnitt&region=sv-SE&password=MittLösenord" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "datafile=@exempel.csv" \
  -F "Spreadsheet=@arbetsbok.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binär ström för det resulterande kalkylarket>"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher undan de lågnivådetaljer som gör att du kan fokusera på dina projektoppgifter. Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---