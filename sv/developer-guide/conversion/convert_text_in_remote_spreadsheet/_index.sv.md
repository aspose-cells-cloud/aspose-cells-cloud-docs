---
title: "Konvertera text i fjärrarket"
ArticleTitle: "Konvertera text i fjärrarket – Aspose.Cells Cloud"
second_title: "Dokument"
linktype: "Konvertera text i fjärrarket"
type: docs
url: /sv/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Textkonvertering, API"
description: "Konverterar text i ett angivet intervall i ett kalkylblad, inklusive omvandling av nummer, teckenersättning, radbrytningshantering och normalisering av accenterade tecken."
weight: 1000
---

## Aspose.Cells Cloud Webbtjänstens funktion för att konvertera text i fjärrarket

Anger omvandling av nummer lagrade som text till korrekt nummerformat, ersättning av oönskade tecken och radbrytningar med önskade tecken samt omvandling av accenterade tecken till deras ekvivalenter utan accenter.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parametername    | Typ    | Sökväg/Frågesträng/HTTP-body | Beskrivning |
|------------------|--------|------------------------------|-------------|
| name             | string | Sökväg | (Obligatoriskt) Namnet på arbetsbokens fil som ska hämtas. |
| worksheet        | string | Sökväg | Anger kalkylbladet i kalkylarket. |
| range            | string | Sökväg | Anger intervallet i kalkylbladet i kalkylarket. |
| convertTextType  | string | Frågesträng | Anger typ av textomvandling. (Obligatoriskt) |
| sourceCharacters | string | Frågesträng | Anger källtecknen. (Valfritt) |
| targetCharacters | string | Frågesträng | Anger måltecknen. (Valfritt) |
| folder           | string | Frågesträng | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standard är null. |
| storageName      | string | Frågesträng | (Valfritt) Namnet på lagringen om du använder anpassad molnlagring. Använd standardlagring om utelämnas. |
| region           | string | Frågesträng | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifik beteende. (Valfritt) |
| password         | string | Frågesträng | Lösenordet för att öppna kalkylarksfilen. (Valfritt) |

### Begärcodeparameter

| Parametername | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| - | - | - |

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Textomvandlingen slutfördes framgångsrikt.",
  "Data": {
    // Detaljer om omvandlingsresultatet, t.ex. antal uppdaterade celler, kan läggas till här.
  }
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Textomvandlingsåtgärden slutfördes framgångsrikt. |
| 400 | Felaktig begäran | Begäran var felformaterad eller saknade obligatoriska parametrar. |
| 401 | Ej auktoriserad | Autentisering misslyckades eller JWT-token saknas eller är ogiltig. |
| 413 | För stor nyttolast | Begärans nyttolast överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel inträffade på servern. |

## Hur man använder Konvertera text i fjärrarket med SDK:er

### Specifikation för Konvertera text i fjärrarket

[Specifikationen för Konvertera text i fjärrarket API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för enkelt att komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Textomvandlingen slutfördes framgångsrikt.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Nummer konverterade, tecken ersatta, radbrytningar normaliserade."
  }
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att snabba upp utvecklingen. En SDK abstraherar lågnivådetaljer och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---