---
title: "Ta bort tecken efter position"
ArticleTitle: "Ta bort tecken efter position – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort tecken efter position"
type: docs
url: /sv/cells/content/remove/characters-by-position
aliases: []
keywords: "Aspose.Cells, Ta bort tecken, API"
description: "Tar bort tecken från celler efter position i ett kalkylark."
weight: 100
---

## Ta bort tecken efter position med Aspose.Cells Cloud Webbtjänster

Tar bort tecken från alla celler i målområdet efter position (första/ista N tecken, före/efter en delsträng eller mellan två avgränsare), samtidigt som formler, formatering och datavalidering bevaras.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameter Name            | Typ     | Path/Query String/HTTP Body | Beskrivning                                                                                                          |
|---------------------------|---------|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| Spreadsheet               | Fil     | FormData                    | Ladda upp kalkylarkfil.                                                                                             |
| theFirstNCharacters       | Heltal  | Query                       | Ange att de första n tecknen ska tas bort från valda celler. Valfritt.                                              |
| theLastNCharacters        | Heltal  | Query                       | Ange att de sista n tecknen ska tas bort från valda celler. Valfritt.                                               |
| allCharactersBeforeText   | Sträng  | Query                       | Ta bort text som finns före en angiven delsträng. Valfritt.                                                         |
| allCharactersAfterText    | Sträng  | Query                       | Ta bort text som finns efter en angiven delsträng. Valfritt.                                                        |
| caseSensitive             | Boolean | Query                       | Påverkar läget `Substring` och `CustomChars` när aktiverat. Valfritt.                                               |
| worksheet                 | Sträng  | Query                       | Ange kalkylblad i kalkylarket. Valfritt.                                                                            |
| range                     | Sträng  | Query                       | Ange kalkylbladsområde i kalkylarket (t.ex. `A1:B10`). Valfritt.                                                   |
| outPath                   | Sträng  | Query                       | (Valfritt) Mappens sökväg där arbetsboken lagras. Standard är null. Valfritt.                                       |
| outStorageName            | Sträng  | Query                       | Lagringsnamn för utdatafil. Valfritt.                                                                               |
| region                    | Sträng  | Query                       | Region/språkinställning för kalkylark (t.ex. `en-US`, `fr-FR`). Valfritt.                                          |
| password                  | Sträng  | Query                       | Lösenord för att öppna kalkylarkfilen. Valfritt.                                                                    |

### Begäran – Brödtextparameter

| Parameter Name | Typ | Beskrivning |
| -------------- | --- | ----------- |
| Spreadsheet    | Fil | Ladda upp kalkylarkfil. |

### **Svar**

```json
{
  "status": "OK",
  "message": "Tecken borttagna framgångsrikt.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Åtgärden slutfördes framgångsrikt och den bearbetade filen returneras. |
| 400 | Ogiltig begäran | Begäran är felaktigt formaterad eller innehåller ogiltiga parametrar. |
| 401 | Oautentiserad | Autentisering misslyckades eller JWT-token saknas eller är ogiltig. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel uppstod på serversidan. |

## Hur du använder Ta bort tecken efter position med SDK:er

### Specification för Ta bort tecken efter position

[Specification för Ta bort tecken efter position API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPosition) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/content/remove/characters-by-position?theFirstNCharacters=5&worksheet=Sheet1&range=A1%3AB10" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "status": "OK",
  "message": "Tecken borttagna framgångsrikt.",
  "downloadUrl": "https://api.aspose.cloud/v4.0/storage/file/sample_output.xlsx"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---