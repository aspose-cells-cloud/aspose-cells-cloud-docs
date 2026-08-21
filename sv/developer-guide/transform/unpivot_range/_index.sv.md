---
title: "UnpivotRange"
ArticleTitle: "UnpivotRange – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "UnpivotRange"
type: docs
url: /cells/unpivot/range
aliases: []
keywords: "Aspose.Cells, UnpivotRange, API"
description: "Växla rader och kolumner i kalkylbladet."
weight: 10
---

## UnpivotRange för Aspose.Cells Cloud-webbtjänster

Växla rader och kolumner i kalkylbladet.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/range
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parametername    | Typ    | Sökväg/frågesträng/HTTP-kropp | Beskrivning                                                                                                                                                     |
|------------------|--------|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil    | FormData                      | Ladda upp kalkylbladsfil.                                                                                                                                       |
| worksheet        | sträng | Fråga                         | Kalkylbladsnamnet.                                                                                                                                              |
| cellArea         | sträng | Fråga                         | Ett angivet dataintervall.                                                                                                                                      |
| skipEmptyValue   | boolean| Fråga                         | Om true, hoppar över tomma värden. Standard: true.                                                                                                              |
| outPath          | sträng | Fråga                         | (Valfritt) Mappens sökväg där arbetsboken lagras. Standard är null.                                                                                             |
| outStorageName   | sträng | Fråga                         | Lagringsnamn för utdatafil.                                                                                                                                     |
| region           | sträng | Fråga                         | Kalkylbladsregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och lokalbaserad beteende.                   |
| password         | sträng | Fråga                         | Lösenord för att öppna kalkylbladsfilen.                                                                                                                       |

### Begärons Kropp-Parameter

| Parametername | Typ | Beskrivning |
|---------------|-----|-------------|
| — | — | — |

### **Svar**

```json
{
  "File": "binär ström"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Den oomvandlade (unpivoted) kalkylbladsfilen returneras. |
| 400 | Felaktig begäran | Ogiltiga begäransparametrar. |
| 401 | Otillåten | Autentisering misslyckades. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel | Servern stötte på ett oväntat tillstånd. |

## Hur du använder UnpivotRange med SDK:er

### UnpivotRange-specifikation

[UnpivotRange API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{UnpivotRange}) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/range?worksheet=Blad1&cellArea=A1:C10&skipEmptyValue=true&outPath=output%2Fmapp&outStorageName=MinLagring&region=sv-SE&password=dittLösenord" -X PUT -H "Content-Type: multipart/form-data" -H "Accept: application/octet-stream" -H "Authorization: Bearer <jwt-token>" -F 'Spreadsheet=@exempel.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "FileUrl": "https://example.com/output/omvandlad.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---