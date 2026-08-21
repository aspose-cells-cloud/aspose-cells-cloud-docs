---
title: "Ta bort dubbletter av delsträngar i fjärrkalkylark"
ArticleTitle: "Ta bort dubbletter av delsträngar i fjärrkalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort dubbletter av delsträngar i fjärrkalkylark"
type: docs
url: /sv/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, Ta bort dubbletter av delsträngar, API"
description: "API för att hitta och ta bort upprepade delsträngar i celler inom ett angivet intervall i en arbetsbok."
weight: 1
---

## Ta bort dubbletter av delsträngar i fjärrkalkylark via Aspose.Cells Cloud-webbtjänster

Hittar och tar bort upprepade delsträngar i varje cell i det valda intervallet, med hjälp av användardefinierade eller förinställda avgränsare, samtidigt som formler, format och dataval bevaras.

**Hur dubbletter upptäcks**  
1. Varje cellvärde delas upp i delsträngar med hjälp av den valda avgränsaren/n.  
2. Verktyget jämför delsträngarna **inom samma cell** och behåller endast den **första förekomsten** av varje dubblett.  
3. Renade delsträngar sammanfogas igen med samma avgränsare/er och skrivs tillbaka till cellen.  

**Alternativ för avgränsare**  
- Förinställd lista: komma, semikolon, blanksteg, tabb, radbrytning  
- `Custom` (Anpassad) – ange valfritt tecken eller tecken; flera tecken behandlas som en sammansatt avgränsare  
- `TreatConsecutiveDelimitersAsOne` (Behandla på varandra följande avgränsare som en) – slå samman intilliggande avgränsare till en enda separator  

Endast celler av typen sträng bearbetas; tal, booleska värden och formler konverteras till sträng innan delning (formler kasseras). Returnerar antalet renade celler och den uppdaterade arbetsboksströmmen.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ    | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning |
|---------------|--------|----------------------------------|-------------|
| name | sträng | Sökväg | (Obligatoriskt) Namnet på arbetsboksfilen som ska hämtas. |
| worksheet | sträng | Sökväg | Anger kalkylbladet i kalkylarket. |
| range | sträng | Sökväg | Anger intervallet i kalkylbladet. |
| delimiters | sträng | Frågesträng | Avgränsare som används för att dela upp cellvärden (t.ex. komma, semikolon, blanksteg, tabb, radbrytning). Obligatoriskt. |
| treatConsecutiveDelimitersAsOne | boolesk | Frågesträng | Slår ihop intilliggande avgränsare till en enda separator. Standard: true. Valfritt. |
| caseSensitive | boolesk | Frågesträng | Utför skiftlägeskänslig jämförelse vid upptäckt av dubbletter. Valfritt. |
| folder | sträng | Frågesträng | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standard: null. |
| storageName | sträng | Frågesträng | (Valfritt) Namnet på lagringen om anpassad molnlagring används. |
| region | sträng | Frågesträng | Region/språkinställning för kalkylarket (t.ex. `sv-SE`, `en-US`, `fr-FR`). Valfritt. |
| password | sträng | Frågesträng | Lösenordet för att öppna kalkylarksfilen. Valfritt. |

### Brödtextparameter för begäran

| Parameternamn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| - | - | Ingen brödtext krävs för denna åtgärd. |

### **Svar**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-kodad arbetsboksström"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Åtgärden lyckades; returnerar antalet renade celler och den uppdaterade arbetsboksströmmen. |
| 400 | Felaktig begäran | En eller flera begärparametrar saknas eller är ogiltiga. |
| 401 | Otillåten | Autentisering misslyckades eller JWT-token saknas/är ogiltig. |
| 413 | För stor nyttolast | Begäran överskrider tillåtna storleksgränser. |
| 500 | Internt serverfel | Ett oväntat fel inträffade på servern. |

## Hur du använder Ta bort dubbletter av delsträngar i fjärrkalkylark med SDK:er

### Specifikation för Ta bort dubbletter av delsträngar i fjärrkalkylark

[Specifikationen för Ta bort dubbletter av delsträngar i fjärrkalkylark API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}
{< tab tabNum="1" >}
```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-kodad arbetsboksström"
}
```
{< /tab >}
{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---