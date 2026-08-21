---
title: "Sök alla textobjekt i kalkylark"
ArticleTitle: "Sök alla textobjekt i kalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /sv/cells/search/content/all-textitems
aliases: []
keywords: "Aspose.Cells, sökning, textobjekt, API"
description: "Sök efter alla textobjekt i ett kalkylark med Aspose.Cells Cloud API."
weight: 100
---

## Sökning efter alla textobjekt i kalkylark med Aspose.Cells Cloud-webbtjänster

Denna metod söker efter alla textobjekt i ett lokalt kalkylark. Den stöder sökning genom alla ark och celler i arbetsboken och identifierar förekomster av söktermen. Operationen utförs på molnside och kräver inget molnlagringsutrymme. Se till att du har nödvändiga behörigheter för att läsa källfilen. Om källfilen inte kan nås eller om ett fel uppstår under sökningen (t.ex. ett filformat som inte stöds), kommer ett lämpligt undantag att kastas. Metoden kan returnera platserna för träffarna (t.ex. arknamn, cellkoordinater) beroende på implementationsdetaljer.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/search/content/all-textitems
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Parametrar för begäran

| Parametername | Typ | Path/Query String/HTTP Body | Beskrivning |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | Fil | FormData | Ladda upp kalkylarkfil. |
| region | Sträng | Query | Inställning för kalkylarksregion/språk (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifika beteenden. |
| password | Sträng | Query | Lösenord för att öppna kalkylarkfilen. |

### Parametrar för begärandetext

| Parametername | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Svar**

```json
{
  "SearchResults": [
    {
      "SheetName": "Ark1",
      "CellName": "A1",
      "Text": "Exempeltext"
    }
    // ... fler objekt
  ],
  "TotalCount": 42
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|---------|-------------|
| 200 | OK | Begäran lyckades och svaret innehåller alla hittade textobjekt. |
| 400 | Felaktig begäran | Ogiltig URL eller felaktiga parametrar i begäran. |
| 401 | Oautentiserad | Autentisering misslyckades, eller så angavs inga autentiseringsuppgifter. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | Payload för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid datahämtning. |

## Hur du använder sökning efter alla textobjekt i kalkylark med SDK:er

### Specifikation för sökning efter alla textobjekt i kalkylark

[Specifikationen för API:et Sök alla textobjekt i kalkylark](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{SearchController}/{SearchSpreadsheetAllTextItems}) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/search/content/all-textitems?region=sv-SE&password=myPassword" \
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
  "SearchResults": [
    {
      "SheetName": "Ark1",
      "CellName": "A1",
      "Text": "Exempeltext"
    }
    // ... fler objekt
  ],
  "TotalCount": 42
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att snabba upp utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---