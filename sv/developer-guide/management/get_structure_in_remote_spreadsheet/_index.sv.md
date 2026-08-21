---
title: "GetStructureInRemoteSpreadsheet"
ArticleTitle: "Hämta struktur i fjärrkalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "GetStructureInRemoteSpreadsheet"
type: docs
url: /cells/{name}/structure
aliases: []
keywords: "Aspose.Cells, GetStructure, kalkylark, struktur"
description: "Hämta den strukturella metadata för en fjärr-Excel-arbetsbok, inklusive kalkylblad, tabeller, pivottabeller, diagram, former och annan central information."
weight: 100
---

## Aspose.Cells Cloud-webbtjänstens funktion för att hämta struktur i fjärrkalkylark

Konvertera strukturellt den centrala metadata, kalkylblad, tabeller, pivottabeller, diagram, former och annan information i en Excel-arbetsbok till ett JSON-objekt av typen JObject, för användningsområden såsom dataexport, API-svar och loggning.

### Slutpunkt för webb-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/structure
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameternamn | Typ | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning |
|----------------|------|-----------------------------|-------------|
| name | string | Sökväg | Namn på kalkylarkfilen. |
| folder | string | Fråga | Mapp där filen finns. (Valfritt) |
| storageName | string | Fråga | (Valfritt) Namnet på lagringsplatsen vid användning av anpassad molnlagring. Använd standardlagring om utelämnas. |
| region | string | Fråga | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och plats-specifik beteendefunktion. |
| password | string | Fråga | Lösenord för att öppna kalkylarkfilen. |

### Begäranbrådtextparameter

| Parameternamn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Svar**

```json
{
  "Worksheets": [
    {
      "Name": "Blad1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "string",
    "Created": "string",
    "Version": "string"
  },
  "DocumentProperties": {
    "Title": "string",
    "Subject": "string",
    "Keywords": "string"
  }
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|---------|-------------|
| 200 | OK | Arbetsboksstruktur har hämtats utan problem. |
| 400 | Ogiltig begäran | Ogiltiga begäransparametrar. |
| 401 | Otillåten | Autentisering misslyckades eller token saknas. |
| 413 | För stor nyttolast | Begärans nyttolast överskrider tillåten storlek. |
| 500 | Internt serverfel | Oväntat serverfel. |

## Hur du använder funktionen för att hämta struktur i fjärrkalkylark med SDK:er

### Specificering för att hämta struktur i fjärrkalkylark

[API-specificering för att hämta struktur i fjärrkalkylark](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetStructureInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/structure?folder=myFolder&storageName=MyStorage&region=en-US&password=SecretPwd" \
  -X GET \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Blad1",
      "Tables": [],
      "PivotTables": [],
      "Charts": [],
      "Shapes": []
    }
  ],
  "WorkbookProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z",
    "Version": "16.0"
  },
  "DocumentProperties": {
    "Title": "SalesReport",
    "Subject": "Kvartalsvis försäljning",
    "Keywords": "försäljning,rapport,2023"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose Cells Cloud-webbtjänster med hjälp av olika SDK:er:
`[TBD]`
---