---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Dokument"
linktype: "docs"
url: /cells/flip
aliases: []
keywords: "FlipData, Transponera, Aspose.Cells"
description: "Transponerar ett angivet dataområde i en kalkylarksfil."
weight: 100
---

## FlipData hos Aspose.Cells Cloud Webbtjänster

Denna API vänder på orienteringen för en given datamatris. Till exempel blir ett 3x2-område (3 rader, 2 kolumner) till ett 2x3-område (2 rader, 3 kolumner) i utdata. Det används vanligtvis för att omstrukturera data för att uppfylla indatakraven hos olika diagram, rapporter eller datamodeller.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ    | Path/Query String/HTTP Body | Beskrivning |
|---------------|--------|-----------------------------|-------------|
| Spreadsheet   | Fil    | FormData                    | Ladda upp kalkylarksfil. |
| worksheet     | Sträng | Query                       | Namnet på kalkylbladet. |
| cellArea      | Sträng | Query                       | Ett angivet dataområde. |
| Horizontal    | Boolean | Query                      | Horisontell/Vertikal spegling. Standard: true |
| outPath       | Sträng | Query                       | (Valfritt) Mappsökvägen där arbetsboken lagras. Standard är null. |
| outStorageName| Sträng | Query                       | Lagringsnamn för utdatafilen. |
| region        | Sträng | Query                       | Region/språkinställning för kalkylarket (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifik beteende. |
| password      | Sträng | Query                       | Lösenord för att öppna kalkylarksfilen. |

### Begärcodeparametrar

| Parameternamn | Typ | Beskrivning |
| ------------- | --- | ----------- |
| *Ingen*       | *N/A* | *Ingen ytterligare JSON-kropp krävs; filen skickas som multipart/form-data.* |

### **Svar**

```json
{
  "File": "<binär ström av den omvandlade arbetsboken>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Operationen slutfördes framgångsrikt och den omvandlade kalkylarksfilen returneras. |
| 400 | Felaktig begäran | En eller flera obligatoriska parametrar saknas eller är ogiltiga. |
| 401 | Obehörig | Autentisering misslyckades – JWT-token saknas eller är ogiltig. |
| 413 | Payload för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel uppstod på servern. |

## Hur du använder FlipData med SDK:er

### FlipData-specifikation

[FlipData API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=sv-SE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<binär ström av den omvandlade arbetsboken>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher undan lågnivådetaljer och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---