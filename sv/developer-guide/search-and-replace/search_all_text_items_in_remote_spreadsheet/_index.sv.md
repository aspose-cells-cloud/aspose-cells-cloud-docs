---
title: "SearchAllTextItemsInRemoteSpreadsheet"
ArticleTitle: "SearchAllTextItemsInRemoteSpreadsheet – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "SearchAllTextItemsInRemoteSpreadsheet"
type: docs
url: /cells/{name}/search/content/all-textitems
aliases: []
keywords: "sök, textobjekt, Aspose.Cells"
description: "Sök efter alla textobjekt i en extern kalkylarkfil med Aspose.Cells Cloud."
weight: 100
---

## SearchAllTextItemsInRemoteSpreadsheet i Aspose.Cells Cloud Webbtjänster

Denna metod söker efter alla textobjekt i en extern kalkylarkfil. Den stöder sökning genom alla arbetstablellblad och celler i arbetsboken och identifierar förekomster av söktermen. Operationen utförs i molnet och kräver ingen lokal lagring. Se till att du har nödvändiga behörigheter för att läsa källfilen. Om källfilen inte går att nå eller om ett fel uppstår under sökningen (t.ex. ett filformat som inte stöds), kommer ett lämpligt undantag att kastas. Metoden kan returnera platserna för matchningarna (t.ex. arknamn, cellkoordinater), beroende på implementeringsdetaljer.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäran parametrar

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-kropp | Beskrivning |
|---------------|-------|-------------------------------|-------------|
| name          | string | Sökväg                       | Namnet på arbetsboksfilen. |
| folder        | string | Fråga                        | Sökvägen till mappen där arbetsboken lagras. |
| storageName   | string | Fråga                        | (Valfritt) Namnet på lagringsutrymmet om du använder anpassat molnlagring. Använd standardlagring om utelämnas. |
| region        | string | Fråga                        | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av nummer, tolkning av datum och lokalbaserat beteende. |
| password      | string | Fråga                        | Lösenordet för att öppna kalkylarkfilen. |

### Begärandekroppens parameter

| Parameternamn | Typ | Beskrivning |
| ------------- | ---- | ----------- |
| [TBD]         |      | [TBD]       |

### **Svar**

```json
{
  "TextItems": [
    {
      "SheetName": "string",
      "CellAddress": "string",
      "Text": "string"
    }
  ],
  "TotalCount": 0
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK        | Begäran lyckades och svaret innehåller alla textobjekt som hittades i kalkylarket. |
| 400 | Felaktig begäran | Ogiltig URL eller begäransparametrar. |
| 401 | Otillåten   | Autentisering misslyckades eller inga uppgifter har angetts. |
| 404 | Hittades inte | Källfilen går inte att nå. |
| 413 | Payload för stor | Begärans payload överskrider den tillåtna storleken. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid datahämtning. |

## Hur du använder SearchAllTextItemsInRemoteSpreadsheet med SDK:er

### Specifikation för SearchAllTextItemsInRemoteSpreadsheet

[Specifikationen för SearchAllTextItemsInRemoteSpreadsheet API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchAllTextItemsInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/search/content/all-textitems?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "TextItems": [
    {
      "SheetName": "Blad1",
      "CellAddress": "A1",
      "Text": "Exempeltext"
    }
  ],
  "TotalCount": 1
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud webbtjänster med olika SDK:er:
`[TBD]`
---