---
title: "Ta bort tomma rader i kalkylark"
ArticleTitle: "Ta bort tomma rader i kalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort tomma rader i kalkylark"
type: docs
url: /cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, ta bort tomma rader, kalkylark, API"
description: "Tar bort alla tomma rader från en kalkylarksfil."
weight: 100
---

## Ta bort tomma rader i kalkylark med Aspose.Cells Cloud-webbtjänster

Denna metod tar bort rader från ett kalkylark som är helt tomma, det vill säga innehåller varken data eller objekt. Den skannar alla kalkylark och identifierar rader där alla celler är tomma. Åtgärden utförs direkt i kalkylarket, vilket säkerställer att endast rader utan något innehåll tas bort. Detta hjälper till att rensa upp kalkylarket och ta bort onödiga tomma rader, vilket gör datat mer organiserat och lättare att hantera. Användare bör säkerställa att kalkylarket är säkerhetskopierat innan de utför denna åtgärd, eftersom borttagna rader inte kan återställas.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parametername | Typ   | Sökväg/Frågesträng/HTTP-body | Beskrivning |
|---------------|-------|------------------------------|-------------|
| Spreadsheet   | Fil   | FormData                     | Ladda upp kalkylarkfil. |
| outPath       | Sträng | Fråga                        | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standard är null. |
| outStorageName| Sträng | Fråga                        | Lagringsnamn för utdatafilen. |
| region        | Sträng | Fråga                        | Region/språkinställning för kalkylarket (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och lokalbaserat beteende. |
| password      | Sträng | Fråga                        | Lösenord för att öppna kalkylarkfilen. |

### Begäronsparametrar för brödtexten

| Parametername | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| Spreadsheet    | Fil | Ladda upp kalkylarkfil. |

### **Svar**

```json
{
  "ResponseFile": "binär filström"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Den bearbetade kalkylarkfilen med borttagna tomma rader returneras. |
| 400 | Felaktig begäran | Ogiltig URL eller begäransparametrar. |
| 401 | Auktorisering misslyckades | Autentiseringen har misslyckats, eller så inga uppgifter har angetts. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | För stor nyttolast | Begärons nyttolast överskrider den tillåtna storleken. |
| 500 | Internt serverfel | Kalkylarket har stött på ett fel vid datahämtning. |

## Hur man använder Ta bort tomma rader i kalkylark med SDK:er

### Specificering för Ta bort tomma rader i kalkylark

[API-specificeringen för Ta bort tomma rader i kalkylark](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}
{< tab tabNum="1" >}
```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=sv-SE&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "binär filström"
}
```
{< /tab >}
{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraherar bort detaljer på lavsnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---