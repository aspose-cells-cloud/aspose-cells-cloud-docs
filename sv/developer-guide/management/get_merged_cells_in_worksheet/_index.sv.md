---
title: "GetMergedCellsInWorksheet"
ArticleTitle: "Hämta sammanfogade celler i kalkylblad – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "GetMergedCellsInWorksheet"
type: docs
url: /sv/cells/spreadsheet/mergedcells
aliases: []
keywords: "Aspose Cells, sammanfogade celler, kalkylblad, API"
description: "Hämta alla sammanfogade cellområden från ett lokalt kalkylarkskalkylblad."
weight: 1000
---

## Get Merged Cells In Worksheet med Aspose.Cells Cloud Webbtjänster

Hämta alla sammanfogade cellområden från ett lokalt kalkylarkskalkylblad.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameter Name | Typ | Path/Query String/HTTP Body | Beskrivning |
|----------------|------|-----------------------------|-------------|
| Spreadsheet | Fil | FormData | Ladda upp kalkylarksfil. |
| worksheet | Sträng | Query | Kalkylbladsnamn. |
| region | Sträng | Query | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och plats-specifik beteende. |
| password | Sträng | Query | Lösenord för att öppna kalkylarksfilen. |

### Begärandetextparameter

| Parameter Name | Typ | Beskrivning |
| -------------- | ---- | ----------- |
| N/A | N/A | Denna åtgärd accepterar inte en JSON-kropp; kalkylarksfilen skickas via `multipart/form-data`. |

### **Svar**

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|------|---------|-------------|
| 200 | OK | Sammanfogade cellområden har hämtats framgångsrikt. |
| 400 | Felaktig begäran | En eller flera begäranparametrar är ogiltiga eller saknas. |
| 401 | Ej auktoriserad | Autentisering misslyckades – ogiltig eller saknad JWT-token. |
| 413 | Payload för stor | Uppladdad kalkylarksfil överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel uppstod på servern. |

## Hur man använder Get Merged Cells In Worksheet med SDK:er

### Get Merged Cells In Worksheet-specifikation

[Get Merged Cells In Worksheet API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/GetMergedCellsInWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/mergedcells?worksheet=Blad1&region=sv-SE&password=MittLösenord" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@exempel.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
[
  {
    "Column": 1,
    "ColumnCount": 3,
    "Row": 5,
    "RowCount": 2
  },
  {
    "Column": 6,
    "ColumnCount": 2,
    "Row": 10,
    "RowCount": 4
  }
]
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraherar lågnivådetaljer så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---