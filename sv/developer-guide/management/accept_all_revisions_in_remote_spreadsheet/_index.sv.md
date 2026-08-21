---
title: "Acceptera alla ändringar i externt kalkylark"
ArticleTitle: "Acceptera alla ändringar i externt kalkylark – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Acceptera alla ändringar i externt kalkylark"
type: docs
url: /sv/cells/accept-all-revisions
aliases: [  /sv/cells/accept-all-revisions ]
keywords: "Aspose.Cells, AcceptAllRevisions, externt kalkylark"
description: "Acceptera alla spårade ändringar (revideringar) i ett externt kalkylark och returnera den uppdaterade arbetsboken som fil."
weight: 1000
---

## Acceptera alla ändringar i externt kalkylark – Aspose.Cells Cloud-webbtjänster

Accepterar alla spårade ändringar (revideringar) i den angivna arbetsboken som finns lagrad i externt lagring. Operationen kan valfritt skriva den resulterande arbetsboken till en annan plats eller lagring och returnerar den uppdaterade filen som en binär ström.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parametername | Typ | Path/Query String/HTTP Body | Beskrivning |
|---------------|------|-----------------------------|-------------|
| name | string | Path | Namnet på arbetsboksfilen som finns lagrad i externt lagring. |
| folder | string | Query | (Valfritt) Mapp i lagringen där arbetsboken finns. |
| storageName | string | Query | (Valfritt) Namnet på lagringen vid användning av anpassad molnlagring. Använd standardlagring om utelämnas. |
| outPath | string | Query | (Valfritt) Mappsökvägen dit den uppdaterade arbetsboken ska sparas. Standard är null. |
| outStorageName | string | Query | (Valfritt) Lagringsnamn för utdatafilen. |
| fontsLocation | string | Query | (Valfritt) Sökväg till anpassad plats för typsnitt. |
| region | string | Query | (Valfritt) Region/språkinställning för kalkylark (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och lokalspecifika beteenden. |
| password | string | Query | (Valfritt) Lösenord för att öppna kalkylarksfilen. |

### Begäranbrukarens innehåll (request body)

| Parametername | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| *Ingen* | *Ingen* | Denna operation kräver inte ett begäraninnehåll. |

### **Svar**

```json
{
  "File": "Binär ström av den uppdaterade arbetsboken (t.ex. .xlsx), returnerad som svarskropp."
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Arbetsboken med alla revideringar accepterade returneras som en binär filström. |
| 400 | Felaktig begäran | Saknade obligatoriska parametrar eller ogiltigt begäranformat. |
| 401 | Otillåten | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast | Begäran överskrider tillåtna storleksgränser. |
| 500 | Internt serverfel | Ett oväntat fel uppstod på servern. |

## Hur man använder Acceptera alla ändringar i externt kalkylark med SDK:er

### Acceptera alla ändringar i externt kalkylark – specifikation

[Acceptera alla ändringar i externt kalkylark API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisionsInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/accept-all-revisions?folder=myFolder&storageName=MyStorage&outPath=output%2Fupdated.xlsx&outStorageName=OutStorage&fontsLocation=%2Fcustom%2Ffonts&region=sv-SE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "Binär ström av den uppdaterade arbetsboken (t.ex. .xlsx)."
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---