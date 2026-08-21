---
title: "Aspose.Cells Cloud – Konvertera tabell till HTML"
description: "Konvertera Excel-tabeller snabbt till HTML med Aspose.Cells Cloud API – säkert, formatbevarande och lätt att integrera."
keywords: "Aspose.Cells, Excel till HTML, konvertera tabell till HTML, moln-API, kalkylbladskonvertering"
weight: 100
date: 2026-07-30
last_updated: 2026-07-30
version: "v4.0"
url: /sv/convert-table-to-html/
type: docs
---

**Snabb sammanfattning** – Detta slutställe läser en lokal Excel-arbetsbok, extraherar den angivna **tabellen**, konverterar den till en **HTML**-fil och returnerar resultatet som en hämtningsbar ström. Ingen mellanliggande uppladdning till Aspose Cloud-lagring krävs.

## ConvertTableToHTML API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Namn               | Plats     | Typ       | Krävs   | Beskrivning                                                                                      |
| ------------------ | --------- | --------- | ------- | ------------------------------------------------------------------------------------------------ |
| **Spreadsheet**    | Form‑Data | `File`    | **Ja**  | Excel-arbetsboken som innehåller tabellen som ska konverteras.                                  |
| **worksheet**      | Fråga     | `String`  | **Ja**  | Namn på kalkylbladet som innehåller tabellen.                                                   |
| **tableName**      | Fråga     | `String`  | **Ja**  | Exakt namn på tabellen som ska konverteras.                                                     |
| **outPath**        | Fråga     | `String`  | Nej     | Mappväg i Aspose Cloud-lagring där HTML-filen ska sparas (valfritt).                            |
| **outStorageName** | Fråga     | `String`  | Nej     | Lagringsnamn för utdatafilen (valfritt).                                                        |
| **fontsLocation**  | Fråga     | `String`  | Nej     | Sökväg till en mapp med anpassade teckensnitt som krävs för konverteringen.                     |
| **region**         | Fråga     | `String`  | Nej     | Språkidentifikator (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummer- och datumformat.        |
| **password**       | Fråga     | `String`  | Nej     | Lösenord för att öppna en skyddad arbetsbok.                                                    |
| **AutoRowsFit**    | Fråga     | `Boolean` | Nej     | Justera automatiskt alla rader i kalkylbladet (`true`/`false`).                                 |
| **AutoColumnsFit** | Fråga     | `Boolean` | Nej     | Justera automatiskt alla kolumner i kalkylbladet (`true`/`false`).                              |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-statuskoder**

| Kod | Betydelse              | Beskrivning                                                        |
| --- | ---------------------- | ------------------------------------------------------------------ |
| 200 | OK                     | Filter applicerades framgångsrikt; svaret innehåller åtgärdsg detaljer. |
| 400 | Felaktig förfrågan     | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).   |
| 401 | Ej auktoriserad        | Ogiltig eller saknad JWT-token.                                    |
| 413 | För stor nyttolast     | Den uppladdade filen överskrider storleksgränsen.                  |
| 500 | Internt serverfel      | Oväntat serverfel.                                                 |

## När ska man använda Convert Table to HTML API?

- **Dynamiskt webbinnehåll** – Infoga prislistor, scheman eller produktlistor direkt i webbsidor eller CMS.
- **E-postmallar** – Skapa HTML-fragment för order Sammanfattningar eller rapporter som visas konsekvent i olika e-postklienter.
- **Instrumentpaneler och rapportverktyg** – Visa live-kalkylbladsdata utan att ladda hela arbetsboken eller använda tunga rutnätskomponenter.
- **Dokumentförhandsvisningar** – Ge snabba, formatbevarande förhandsvisningar av specifika delar av kalkylblad.

## Hur används Convert Table to HTML API med SDK:er?

### Convert Table to HTML API-specifikation

[Convert Table to HTML API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToHTML) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att REST-interaktioner kan utföras direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/html?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljer på låg nivå och gör att du enkelt kan konvertera kalkylbladstabelldata till en CSV-fil med minimal kod. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er: