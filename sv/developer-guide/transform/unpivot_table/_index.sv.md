---
title: "Unpivot Table"
ArticleTitle: "Unpivot Table – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Unpivot Table"
type: docs
url: /cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Unpivot, Transformera"
description: "Byt rader och kolumner i kalkylbladet."
weight: 1
---

## Aspose.Cells Cloud Webbtjänsters Unpivot Table

Byt rader och kolumner i kalkylbladet.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parametername    | Typ     | Sökväg/Frågesträng/HTTP-kropp | Beskrivning                                                                                                             |
|------------------|---------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil     | FormData                      | Ladda upp kalkylbladsfil.                                                                                               |
| worksheet        | Sträng  | Fråga                         | Kalkylbladsnamnet.                                                                                                      |
| index            | Heltal  | Fråga                         | Ett angivet dataområde.                                                                                                |
| skipEmptyValue   | Boolesk | Fråga                         | Hoppa över tomma värden (standard: true).                                                                              |
| outPath          | Sträng  | Fråga                         | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standardvärdet är null.                                        |
| outStorageName   | Sträng  | Fråga                         | Lagringsnamn för utdatafilen.                                                                                           |
| region           | Sträng  | Fråga                         | Kalkylbladsregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifik beteende. |
| password         | Sträng  | Fråga                         | Lösenord för att öppna kalkylbladsfilen.                                                                               |

### Begärandekroppsparameter

| Parametername | Typ | Beskrivning |
| ------------- | --- | ----------- |
| N/A           | N/A | Inga begärandekroppsparametrar. |

### **Svar**

```json
{
  "File": "binär ström med det unpivot:ade kalkylbladet"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Det unpivot:ade kalkylbladet returneras. |
| 400 | Felaktig begäran | Ogiltiga begärandeparametrar. |
| 401 | Autentisering misslyckades | Autentisering misslyckades eller JWT-token saknas/ogiltig. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Oväntat serverfel. |

## Hur man använder Unpivot Table med SDK:er

### Unpivot Table-specifikation

[Unpivot Table API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
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
  "File": "binär ström med det unpivot:ade kalkylbladet"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att snabba upp utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---