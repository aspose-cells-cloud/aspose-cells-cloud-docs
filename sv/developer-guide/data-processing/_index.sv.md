---
title: "Aspose.Cells Cloud – Sammanfoga, dela upp & importera kalkylbladsdata"
second_title: "Dokument"
ArticleTitle: "Bearbetning av kalkylbladsdata – Sammanfoga, dela upp & importera"
linktitle: "Datahantering"
type: docs
url: /sv/data-processing/
keywords: "Aspose.Cells Cloud, bearbetning av kalkylbladsdata, sammanfoga Excel, dela upp Excel, CSV-import, JSON-import, API"
description: "Detaljerad guide för import av CSV/JSON-data, sammanfogning av Excel-arbetsböcker i molnet och delning av stora kalkylblad med Aspose.Cells Cloud REST API, inklusive exempel på begäran/svar."
weight: 30
---

**Aspose.Cells Cloud** – en REST-baserad tjänst som möjliggör programmatiserad manipulering av Excel-filer i molnet. Den stöder import av data från olika format, sammanfogning av arbetsböcker och delning av stora kalkylblad.

**Datahantering**-avsnittet i Aspose.Cells Cloud API tillåter dig att importera, sammanfoga och dela kalkylbladsdata programmatiserat. Använd följande slutpunkter för att hantera CSV/JSON-import, kombinera arbetsböcker eller dela stora filer i hanterbara delar.

## Dataimport och hantering

- **[Importera CSV-, JSON- och XML-data till Excel-filer](https://docs.aspose.cloud/cells/import-data-into-spreadsheet/)**  

Importåtgärden tar emot CSV-, JSON- eller XML-innehåll i begärandetexten och skapar ett nytt kalkylblad (eller uppdaterar ett befintligt) i målarbetsboken.

**Detaljerad information om slutpunkter**

| HTTP-metod | Slutpunkt | Begärandetext | Lyckad svarskod |
|------------|-----------|--------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/import` | `application/json` eller `text/csv` (beroende på format) | `200 OK` med JSON som innehåller metadata för den uppdaterade arbetsboken |
| GET | `https://api.aspose.cloud/v3.0/cells/{fileName}?format=excel` | *ingen* | Returnerar den bearbetade arbetsboksfilen |

**Exempel på cURL-begäran (CSV-import)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/MinArbetsbok.xlsx/import" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: text/csv" \
     --data-binary @data.csv
```

**Exempel på JSON-svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "Workbook": {
    "FileName": "MinArbetsbok.xlsx",
    "Worksheets": 3
  }
}
```

> **Krav**: Ett OAuth2-åtkomsttoken krävs. Källfilen måste finnas i Aspose Cloud-lagring eller tillhandahållas via en multipart-uppladdning.

## Sammanfogningsåtgärd

- **[Sammanfoga fjärr-Excel-filer till en angiven arbetsbok](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)**
- **[Sammanfoga flera Excel-filer till en enda arbetsbok](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Sammanfoga Excel-filer som matchar i en fjärrmapp](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)**  

Sammanfogning kombinerar två eller flera arbetsböcker till en enda målarbetsbok. API:t stöder både explicita fillistor och mönsterbaserade sammanfogningar i ett lagringsmapp.

**Detaljerad information om slutpunkter**

| HTTP-metod | Slutpunkt | Parametrar | Lyckad svarskod |
|------------|-----------|------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/merge` | `files` (array med filnamn), `target` (valfritt målarbetsboksnamn) | `200 OK` med JSON som beskriver den sammanfogade arbetsboken |
| POST | `https://api.aspose.cloud/v3.0/cells/merge/remote` | `sourceFolder`, `pattern`, `target` | `200 OK` med metadata för den sammanfogade arbetsboken |

**Exempel på cURL-begäran (sammanfoga explicit lista)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/merge" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "files": ["Book1.xlsx", "Book2.xlsx"],
           "target": "Combined.xlsx"
         }'
```

**Exempel på JSON-svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "MergedWorkbook": {
    "FileName": "Combined.xlsx",
    "Worksheets": 10
  }
}
```

> **Krav**: Alla källarbetsböcker måste lagras på samma molnlagringsplats och den som anropar måste ha läs- och skrivbehörighet.

## Delningsåtgärd

- **[Dela en Excel-fil i flera filer baserat på kalkylblad](https://docs.aspose.cloud/cells/split-remote-spreadsheet/)**
- **[Dela Excel-fil enligt anpassade regler](https://docs.aspose.cloud/cells/split-spreadsheet/)**  

Delning extraherar individuella kalkylblad eller grupper av rader/kolumner till separata arbetsboksfiler.

**Detaljerad information om slutpunkter**

| HTTP-metod | Slutpunkt | Parametrar | Lyckad svarskod |
|------------|-----------|------------|----------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split` | `splitBy` (t.ex. `worksheet`), `outputFolder` | `200 OK` med lista över genererade fil-URL:er |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/split/custom` | JSON för anpassade regler (sidstorlek, radintervall, etc.) | `200 OK` med detaljerad information om delade filer |

**Exempel på cURL-begäran (dela efter kalkylblad)**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/StorRapport.xlsx/split" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "splitBy": "worksheet",
           "outputFolder": "Splits/"
         }'
```

**Exempel på JSON-svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "Splits": [
    {"FileName": "StorRapport_Sheet1.xlsx", "Url": "https://storage.aspose.cloud/..."},
    {"FileName": "StorRapport_Sheet2.xlsx", "Url": "https://storage.aspose.cloud/..."}
  ]
}
```

> **Krav**: Källarbetsboken måste vara tillgänglig i Aspose Cloud-lagring, och den som anropar måste ha skrivbehörighet till målmappen.