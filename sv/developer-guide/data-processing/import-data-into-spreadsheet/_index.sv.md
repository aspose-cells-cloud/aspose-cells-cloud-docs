---
title: "Aspose.Cells Cloud Data Import API – En molnlösning för automatisk import av CSV-, JSON- och XML-data till Excel-arbetsblad."
second_title: "Dokument"
ArticleTitle: "Excel-plattform för dataintegriering från flera källor – Aspose.Cells Clouds API för automatisk dataimport och -transformation."
linktitle: "Importera data till kalkylblad"
type: docs
url: /sv/import-data-into-spreadsheet/
keywords: "Aspose Cells, dataimport-API, CSV till Excel, JSON till Excel, XML till Excel, molnbaserat kalkylblad, REST-API"
description: "Importera CSV-, JSON- eller XML-data till Excel-arbetsblad med Aspose.Cells Clouds REST-API. Lär dig om begärandeformat, parametrar, exempel på SDK-kod och felhantering."
weight: 100
---

## Grundläggande funktioner

### Stöd för flera dataformat

- **<a href="https://docs.fileformat.com/spreadsheet/csv/" rel="noopener noreferrer">CSV</a>-dataimport**: Stöder flera avgränsare och identifierar automatiskt kodning.
- **<a href="https://docs.fileformat.com/web/json/" rel="noopener noreferrer">JSON</a>-datahantering**: Flattar komplexa JSON-strukturer till Excel-tabeller.
- **<a href="https://docs.fileformat.com/web/xml/" rel="noopener noreferrer">XML</a>-filkonvertering**: Knyter noddata till Excel-rad- och kolumnstruktur.

## **Beskrivning av API:et för import av data till kalkylblad**

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/import/data
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| ParameterNamn      | Typ    | Plats            | Beskrivning                                                               |
| ------------------ | ------ | ---------------- | ------------------------------------------------------------------------- |
| datafile           | Fil    | FormData         | Datafilen (CSV, JSON eller XML) som ska importeras.                      |
| spreadsheet        | Fil    | FormData         | Målarbetsboken som ska ta emot den importerade datan.                     |
| worksheet          | sträng | Query            | Namn på arbetsbladet där datan ska placeras.                              |
| startCell          | sträng | Query            | Översta vänstra cellen (t.ex. `A1`) som markerar startpositionen för importen. |
| insert             | bool   | Query            | `true` för att infoga rader; `false` för att skriva över befintlig data. |
| convertNumericData | bool   | Query            | `true` för att konvertera numeriska strängar till siffror vid import.    |
| splitter           | sträng | Query            | Enkeltecken för CSV-avgränsare (standard är `,`).                         |
| outPath            | sträng | Query (valfritt) | Mappkväll för den uppdaterade arbetsboken.                               |
| outStorageName     | sträng | Query (valfritt) | Namn på lagringsplatsen för utfil.                                        |
| fontsLocation      | sträng | Query (valfritt) | Sökväg till en anpassad teckensnittsmapp, om sådan krävs.                |
| region             | sträng | Query (valfritt) | Konfiguration av kalkylbladsregion (t.ex. `sv-SE`).                      |
| password           | sträng | Query (valfritt) | Lösenord för att öppna en skyddad arbetsbok.                             |

### Svar

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

| Kod | Betydelse               | Beskrivning                                                     |
| --- | ----------------------- | --------------------------------------------------------------- |
| 200 | OK                      | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran        | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad           | Ogiltig eller saknad JWT-token.                                 |
| 413 | Payload för stor        | Uppladdad fil överskrider storleksgränsen.                      |
| 500 | Internt serverfel       | Oväntat serverfel.                                              |

## Varför du bör använda detta API

- **Effektiv dataladdning** – Möjliggör bulkimport av stora dataset direkt till en arbetsbok utan att skapa mellanliggande filer.
- **Brett SDK-stöd** – Erhåller klientsbibliotek för .NET, Java, PHP, Ruby, Node.js, Python, Go och Perl, vilket förenklar integrationen.
- **Bearbetning i minnet** – Utför transformationer i minnet, vilket minskar kraven på temporär lagring.

## Hur du använder API:et för import av data till kalkylblad med SDK:er

**Anteckningar / begränsningar:** API:et stöder upp till 1 000 000 rader per import. Komma är standardavgränsare för CSV; andra enkeltolkade avgränsare kan anges via parametern `splitter`. Stora XML-filer kan öka bearbetningstiden.

För relaterade åtgärder såsom export av data eller konvertering av arbetsboksformat, se dokumentationen för **Export Data** och **Convert Workbook**.

### API-specifikation för import av data till kalkylblad

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet" rel="noopener noreferrer">API-specifikationen för import av data till kalkylblad</a> tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från din webbläsare.
Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/import/data?worksheet=Sheet1&startCell=A1&insert=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "datafile=@/path/to/data.csv" \
  -F "spreadsheet=@/path/to/workbook.xlsx"
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den döljer detaljer på låg nivå och låter dig importera data till ett kalkylblad med kort kod. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

---