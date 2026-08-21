---
title: "Sök efter trasiga länkar i fjärrarbetsblad"
ArticleTitle: "Sök efter trasiga länkar i fjärrarbetsblad – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "SökEfterTrasigaLänkarIJärrarbetsblad"
type: docs
url: /sv/cells/{name}/worksheets/{worksheet}/search/broken-links
aliases: []
keywords: "Aspose.Cells, sök trasiga länkar, fjärrarbetsblad"
description: "Sök efter trasiga länkar i ett arbetsblad i en fjärrlagrad kalkylarksfil."
weight: 100
---

## Sök efter trasiga länkar i fjärrarbetsblad med Aspose.Cells Cloud-webbtjänster

Denna metod söker efter trasiga länkar i ett arbetsblad i en kalkylarksfil som är lagrad i fjärrmolnlagring. Den skannar alla ark och celler för att identifiera hyperlänkar som inte längre pekar på giltiga destinationer, t.ex. ogiltiga URL:er eller saknade externa referenser. Operationen utförs i molnmiljön utan att filen behöver laddas ner till den lokala datorn.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ | Path/Query-sträng/HTTP-kropp | Beskrivning |
|----------------|------|-----------------------------|-------------|
| name | string | Path | Namnet på arbetsbokens fil som ska sökas. |
| worksheet | string | Path | Anger arbetsbladet för sökningen. |
| folder | string | Query | Sökvägen till mappen där arbetsboken är lagrad. (valfritt) |
| storageName | string | Query | (Valfritt) Namnet på lagringen om du använder anpassad molnlagring. Använd standardlagring om utelämnas. |
| region | string | Query | Region/språkinställning för kalkylark (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och platsspecifik beteende. |
| password | string | Query | Lösenord för att öppna kalkylarksfilen. |

### Begäarkroppparametrar

| Parameternamn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| — | — | Ingen begäarkropp krävs för denna operation. |

### **Svar**

```json
{
  "Links": [
    {
      "SheetName": "Blad1",
      "CellName": "A1",
      "Url": "http://ogiltig.example.com"
    }
  ],
  "Count": 1
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|-----------|-------------|
| 200 | OK | Listan över trasiga länkar hämtades framgångsrikt. |
| 400 | Felaktig begäran | Ogiltiga begärparametrar eller felaktig URL. |
| 401 | Autentisering misslyckades | Autentisering har misslyckats eller inga autentiseringsuppgifter tillhandahölls. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | Payload för stor | Begärens entitet är för stor. |
| 500 | Internt serverfel | Kalkylarket stötte på ett fel vid datahämtning. |

## Hur du använder sökning efter trasiga länkar i fjärrarbetsblad med SDK:er

### Specifikation för sökning efter trasiga länkar i fjärrarbetsblad

[API-specifikation för Sök trasiga länkar i fjärrarbetsblad](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links?folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Links": [
    {
      "SheetName": "Blad1",
      "CellName": "A1",
      "Url": "http://ogiltig.example.com"
    }
  ],
  "Count": 1
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att snabba upp utvecklingen. En SDK abstraherar från de lågnivådetaljer som krävs, så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---