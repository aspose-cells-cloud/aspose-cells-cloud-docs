---
---
title: "GetSpreadsheetStructure"
ArticleTitle: "GetSpreadsheetStructure – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "GetSpreadsheetStructure"
type: docs
url: /cells/spreadsheet/structure
aliases: []
keywords: "Aspose.Cells, kalkylarkstruktur, API"
description: "Konvertera strukturellt kärnmetadata, kalkylblad, tabeller, pivotdiagram, diagram, former och annan information i en Excel-arbetsbok till ett JSON-objekt av typen JObject."
weight: 1000
---

## GetSpreadsheetStructure hos Aspose.Cells Cloud-webbtjänster

Konvertera strukturellt kärnmetadata, kalkylblad, tabeller, pivotdiagram, diagram, former och annan information i en Excel-arbetsbok till ett JSON-objekt av typen JObject, för scenario som dataexport, API-svar och loggning.

### Slutpunkt för webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/structure
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameter namn | Typ   | Sökväg/Frågesträng/HTTP-body | Beskrivning |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | Fil   | FormData (body)             | Ladda upp kalkylarkfil. |
| region         | Sträng | Fråga                       | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platsbaserat beteende. |
| password       | Sträng | Fråga                       | Lösenord för att öppna kalkylarkfilen. |

### Begärandebody-parameter

| Parameter namn | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| Spreadsheet    | Fil | Ladda upp kalkylarkfil. |

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
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

**Statuskoder för svar**

| Kod | Betydelse | Beskrivning |
|------|-----------|-------------|
| 200 | OK | Kalkylarkstrukturen har hämtats framgångsrikt. |
| 400 | Ogiltig begäran | Ogiltiga begärparametrar eller filformat. |
| 401 | Inte auktoriserad | Autentisering misslyckades eller JWT-token saknas. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel inträffade på servern. |

## Hur man använder GetSpreadsheetStructure med SDK:er

### GetSpreadsheetStructure-specifikation

[GetSpreadsheetStructure API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetSpreadsheetStructure) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för enkelt att komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/structure?region=sv-SE&password=dittLösenord" \
  -X PUT \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@exempel.xlsx'
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
  "DocumentProperties": {
    "Author": "John Doe",
    "Created": "2023-01-01T12:00:00Z"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med hjälp av olika SDK:er:
`[TBD]`
---