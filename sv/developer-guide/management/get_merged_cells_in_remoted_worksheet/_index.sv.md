---
title: "GetMergedCellsInRemotedWorksheet"
ArticleTitle: "Hämta sammanfogade celler i fjärrarbetsblad – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "Hämta sammanfogade celler i fjärrarbetsblad"
type: docs
url: /cells/mergedcells/get
aliases: []
keywords: "Aspose Cells, hämta sammanfogade celler, fjärrarbetsblad, API"
description: "Hämtar alla sammanfogade cellområden från ett fjärrarbetsblad i ett kalkylark."
weight: 10
---

## GetMergedCellsInRemotedWorksheet i Aspose.Cells Cloud Webbtjänster

Hämta alla sammanfogade cellområden från ett fjärrkalkylarksarbetsblad.

### Webb-API-slutpunkt

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/mergedcells
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parametername | Typ   | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning |
|---------------|-------|----------------------------------|-------------|
| name | sträng | Sökväg | Kalkylarksnamn |
| worksheet | sträng | Sökväg | Arbetsbladsnamn |
| folder | sträng | Fråga | Molnlagrings sökvägen till kalkylarket. |
| storageName | sträng | Fråga | (Valfritt) Namnet på lagringen om du använder anpassad molnlagring. Använd standardlagring om utelämnas. |
| region | sträng | Fråga | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platsbaserat beteende. |
| password | sträng | Fråga | Lösenord för att öppna kalkylarksfilen. |

### Brödtextparameter för begäran

| Parametername | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| — | — | *Inga* |

### **Svar**

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Begäran lyckades och listan över sammanfogade cellområden returneras. |
| 400 | Felaktig begäran | Ogiltig URL eller felaktiga begärparametrar. |
| 401 | Otillåten | Autentisering misslyckades eller inga autentiseringsuppgifter angavs. |
| 413 | För stor nyttolast | Begärans nyttolast överskrider den tillåtna storleken. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid datahämtning. |

## Hur du använder GetMergedCellsInRemotedWorksheet med SDK:er

### GetMergedCellsInRemotedWorksheet-specifikation

[GetMergedCellsInRemotedWorksheet API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInRemotedWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/Exempel.xlsx/worksheets/Blad1/mergedcells?folder=MittMapp&storageName=MittLager&region=sv-SE&password=1234" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
[
  {
    "FirstRow": 0,
    "FirstColumn": 0,
    "TotalRows": 2,
    "TotalColumns": 3
  },
  {
    "FirstRow": 5,
    "FirstColumn": 1,
    "TotalRows": 1,
    "TotalColumns": 4
  }
]
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med diverse SDK:er:
`[TBD]`
---