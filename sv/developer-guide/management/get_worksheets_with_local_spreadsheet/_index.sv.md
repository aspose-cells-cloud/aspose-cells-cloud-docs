---
title: "Hämta kalkylblad med lokal kalkylark"
ArticleTitle: "Hämta kalkylblad med lokal kalkylark – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Hämta kalkylblad med lokal kalkylark"
type: docs
url: /cells/spreadsheet/worksheets
aliases: []
keywords: "Aspose.Cells, Kalkylblad, Lokalt kalkylark, API"
description: "Hämtar en komplett lista över kalkylblad från det aktuella aktiva lokala kalkylarket."
weight: 1000
---

## Hämta kalkylblad med lokal kalkylark för Aspose.Cells Cloud-webbtjänster

Detta slutpunktspunkt tillåter åtkomst till det lokala kalkylarksprogrammet (t.ex. Excel) via interop eller en lokal API, samlar namn och typ (t.ex. standard, diagram, makro) för varje kalkylblad och returnerar samlingen som en strukturerad JSON-array. Det används vanligtvis för att fylla i ett användargränssnitt för kalkylbladsväljare eller för att granska innehållet i kalkylark.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameter Name | Typ   | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet    | Fil   | FormData (HTTP-brödtext)        | Ladda upp kalkylarkfil. |
| region         | Sträng | Frågesträng                       | Inställning för kalkylarksregion/språk (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platsberoende beteende. *(valfritt)* |
| password       | Sträng | Frågesträng                       | Lösenord för att öppna kalkylarkfilen. *(valfritt)* |

### Begäranbrödtextparameter

| Parameter Name | Typ | Beskrivning |
|----------------|-----|-------------|
| Spreadsheet    | Fil | Ladda upp kalkylarkfil. |

### **Svar**

```json
{
  "Worksheets": [
    {
      "Name": "Blad1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Diagram1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... ytterligare kalkylblad
  ]
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|---------|-------------|
| 200 | OK | Listan över kalkylblad hämtades framgångsrikt. |
| 400 | Felaktig begäran | Ogiltig begäran (t.ex. felaktig URL eller saknad obligatorisk data). |
| 401 | Autentisering misslyckades | Autentisering har misslyckats, eller inga autentiseringsuppgifter har tillhandahållits. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | Nyttolast för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Kalkylarket har stött på ett undantag vid datahämtning. |

## Hur du använder Hämta kalkylblad med lokal kalkylark med SDK:er

### Specificering för Hämta kalkylblad med lokal kalkylark

[API-specifikation för Hämta kalkylblad med lokal kalkylark](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetWorksheetsWithLocalSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/worksheets?region=sv-SE&password=dittLösenord" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F 'Spreadsheet=@exempel.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Worksheets": [
    {
      "Name": "Blad1",
      "Id": 0,
      "Type": "Standard"
    },
    {
      "Name": "Diagram1",
      "Id": 1,
      "Type": "Chart"
    }
    // ... ytterligare kalkylblad
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---