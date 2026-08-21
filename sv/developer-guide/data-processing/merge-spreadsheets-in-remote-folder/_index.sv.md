---
title: "Sammanfoga matchande kalkylblad i fjärrmapp"
description: "Kombinera kalkylark som lagras i Aspose Cloud-lagring till en enda fil. Stöder 30+ utgångsformat som PDF, CSV, JSON, XLSX, ODS, XPS med mera."
keywords: "Aspose.Cells, sammanfoga kalkylblad, fjärrmapp, API, PDF, CSV, JSON, XLSX, ODS, XPS"
weight: 100
type: docs
url: /sv/merge-spreadsheets-in-remote-folder/
---

Kombinera flera kalkylarksfiler som finns i en fjärrmapp i Aspose Cloud-lagring till en enda utdatafil. Åtgärden körs helt i molnet, vilket eliminierar behovet av att ladda ner källfilerna lokalt. Mer än 30 utgångsformat stöds (PDF, CSV, JSON, XLSX, ODS, XPS, …).

## MergeSpreadsheetsInRemoteFolder API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar <a id="request-parameters"></a>

| Namn                    | Typ     | Plats  | Krävs   | Beskrivning                                                                                          |
| ----------------------- | ------- | ------ | ------- | ---------------------------------------------------------------------------------------------------- |
| **folder**              | sträng  | fråga  | **Ja**  | Mapp i molnlagring som innehåller källkalkylbladen.                                                 |
| **fileMatchExpression** | sträng  | fråga  | **Ja**  | Mönster för att välja filer (t.ex. `*rapport*.xlsx`). Stöder jokertecken `*` och `?`.                |
| **outFormat**           | sträng  | fråga  | **Ja**  | Önskat utdataformat (`PDF`, `CSV`, `JSON`, `XLSX`, `ODS`, `XPS`, …).                                |
| **mergeInOneSheet**     | boolean | fråga  | **Ja**  | `true` – all data sammanfogas till ett enda kalkylblad. `false` – varje källfil får sitt eget kalkylblad. |
| **storageName**         | sträng  | fråga  | Nej     | Anpassat lagringsnamn; standard är primär lagring om utelämnat.                                      |
| **outPath**             | sträng  | fråga  | Nej     | Målmapp för den sammanfogade filen. Om utelämnad sparas filen i källmappen.                          |
| **outStorageName**      | sträng  | fråga  | Nej     | Lagringsnamn där den sammanfogade filen ska skrivas.                                                 |
| **fontsLocation**       | sträng  | fråga  | Nej     | Sökväg till en mapp med anpassade typsnitt (krävs för PDF/bildexport).                               |
| **region**              | sträng  | fråga  | Nej     | Språkinställning för formatering av tal, datum och valuta (t.ex. `sv-SE`, `en-US`, `de-DE`).          |
| **password**            | sträng  | fråga  | Nej     | Lösenord för att öppna eventuella skyddade källkalkylblad.                                          |

## Exempel på begäran (cURL) <a id="request-example"></a>

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "Accept: application/json"
```

### **Svar**

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

Filen kan laddas ner direkt från `FileUrl` eller sparas till den plats som anges i `outPath`.

**Detaljerad lyckad svarshandling**

| Statuskod    | Innehållstyp               | Beskrivning                                |
| ------------ | -------------------------- | ------------------------------------------ |
| 200 OK       | `application/octet-stream` | Binär ström för den sammanfogade arbetsboksfilen. |
| 202 Accepted | `application/json`         | JSON som innehåller `FileUrl`, `FileName` med mera. |

**HTTP-statuskoder**

| Kod | Betydelse               | Beskrivning                                                       |
| --- | ----------------------- | ----------------------------------------------------------------- |
| 200 | OK                      | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Ogiltig begäran         | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Oauktoriserad           | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast      | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel       | Oväntat serverfel.                                                |

## Hur man använder API:et för sammanfogning av kalkylblad med SDK:er

### OpenAPI-specifikation

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder" rel="noopener noreferrer">OpenAPI-specifikationen</a> tillhandahåller en maskinläsbar beskrivning av API:et, vilket möjliggör direkta REST-interaktioner.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets?folder=MyFolder&fileMatchExpression=*.xlsx&outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/Book1.xlsx" \
  -F "Spreadsheet=@/path/to/Book2.xlsx"
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och tillåter dig att importera data till ett kalkylblad med kort kod. Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.