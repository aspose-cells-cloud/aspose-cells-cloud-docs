---
title: "Exportera Excel-diagram – Aspose.Cells Cloud API"
second_title: "Dokument"
description: "Konvertera ett diagram från en Excel-arbetsbok som finns lagrad i molnet till PDF, PNG, SVG eller andra format med ett enda REST-anrop."
ArticleTitle: "Så här konverterar du ett lokalt kalkylblad till en PDF-fil: Steg-för-steg-guide"
linktitle: "Konvertera kalkylblad till PDF"
type: docs
url: /sv/export-chart-as-format/
keywords: "Aspose.Cells Cloud, exportera diagram, API, PDF, PNG, SVG, Excel, REST, molnkonvertering"
weight: 100
---

Exportera ett diagram som finns i en arbetsbok som lagras i Aspose Cloud Storage till ett annat filformat (PDF, PNG, SVG, …) utan att ladda ner källfilen.

## ExportChartAsFormat API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### 📦 Parametrar för begäran

| Namn               | Typ     | Plats  | Obligatorisk | Beskrivning                                                  |
| ------------------ | ------- | ------ | ------------ | ------------------------------------------------------------ |
| **name**           | sträng  | Sökväg | Ja           | Filnamn för arbetsboken.                                     |
| **worksheet**      | sträng  | Sökväg | Ja           | Kalkylbladsnamn som innehåller diagrammet.                   |
| **chartIndex**     | heltal  | Sökväg | Ja           | Nollbaserat index för diagrammet som ska exporteras.         |
| **format**         | sträng  | Fråga  | Ja           | Önskat utdataformat (t.ex. `png`, `pdf`, `svg`).             |
| **folder**         | sträng  | Fråga  | Nej          | Sökväg till mappen där arbetsboken finns lagrad (standard: rot). |
| **storageName**    | sträng  | Fråga  | Nej          | Anpassat lagringsnamn; utelämna för att använda standardlagring. |
| **outPath**        | sträng  | Fråga  | Nej          | Sökväg till mappen där den konverterade filen ska sparas.    |
| **outStorageName** | sträng  | Fråga  | Nej          | Lagringsnamn för utdatafilen.                                |
| **fontsLocation**  | sträng  | Fråga  | Nej          | Sökväg till en mapp som innehåller anpassade typsnitt.       |
| **region**         | sträng  | Fråga  | Nej          | Lokalt inställningsvärde (t.ex. `sv-SE`, `en-US`, `fr-FR`).  |
| **password**       | sträng  | Fråga  | Nej          | Lösenord för att öppna en skyddad arbetsbok.                 |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP-statuskoder**

| Kod | Betydelse                | Beskrivning                                                    |
| --- | ------------------------ | -------------------------------------------------------------- |
| 200 | OK                       | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran         | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad           | Ogiltig eller saknad JWT-token.                                |
| 413 | För stor nyttolast        | Den uppladdade filen överskrider storleksgränsen.              |
| 500 | Internt serverfel         | Oväntat serverfel.                                             |

## Hur använder man API:et för att exportera diagram som format med SDK:er?

### Export Chart as Format API-specifikation

[Export Chart as Format API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportChartAsFormat) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/charts/{chartIndex}?format={format}" \
  -H "Authorization: Bearer {access_token}"
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

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och låter dig konvertera kalkylbladsdatatabeller till en PDF-fil med minimal kod. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er: