---
title: "Sammanfoga flera Excel-filer till en kalkylarkfil – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Kombinera flera Excel-filer till en – Batch-sammanfoga kalkylark till 30+ format"
linktitle: "Sammanfoga kalkylark"
type: docs
url: /sv/merge-spreadsheets/
keywords: "Aspose.Cells, sammanfoga kalkylark, Excel API, molnkalkylark, batch-sammanfogning, PDF-konvertering, CSV-sammanfogning, ODS-sammanfogning, API-referens, SDK"
description: "Kombinera flera lokala Excel-, CSV- eller ODS-filer till en enda arbetsbok och konvertera resultatet till 30+ format (PDF, HTML, m.fl.) med Aspose.Cells Cloud. Innehåller endpoint, parametrar, autentiseringsguide och SDK-exempel."
weight: 100
---

Sammanfoga flera lokala Excel-, CSV- eller ODS-filer till en enda arbetsbok och konvertera den till 30+ utdataformat med Aspose.Cells Cloud API.

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begäranparametrar**

| Parameter Namn   | Typ     | Plats            | Beskrivning                                                                                         |
| ---------------- | ------- | ---------------- | --------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fil     | FormData         | Den lokala kalkylarkfil som ska laddas upp. Stöder XLSX, XLS, CSV, ODS m.m.                        |
| outFormat        | Sträng  | Frågeparameter   | Önskat utdataformat (t.ex. `XLSX`, `PDF`, `CSV`, `HTML`). Stöder 30+ format.                        |
| mergeInOneSheet  | Boolean | Frågeparameter   | `true` → all data sammanfogas till ett enda kalkylblad; `false` → varje originalkalkylblad bevaras. |
| outPath          | Sträng  | Frågeparameter (valfritt) | Molkatalogsökväg där den sammanfogade filen ska sparas. Om utelämnas används standardplatsen.     |
| outStorageName   | Sträng  | Frågeparameter   | Namn på den molnlagring som ska användas (standard eller anpassad).                                |
| fontsLocation    | Sträng  | Frågeparameter (valfritt) | Molkatalog som innehåller anpassade typsnitt för korrekt PDF/bildrendering.                       |
| region           | Sträng  | Frågeparameter (valfritt) | Lokalisering för nummer-, datum- och valutainställningar (t.ex. `sv-SE`, `en-US`, `zh-CN`).        |
| password         | Sträng  | Frågeparameter (valfritt) | Lösenord för att öppna ett skyddat kalkylark.                                                      |

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

Filen kan laddas ner direkt eller sparas till den plats som anges i `outPath`.

**Detaljer för lyckad respons**

| Statuskod | Innehållstyp               | Beskrivning                                 |
| --------- | -------------------------- | ------------------------------------------- |
| 200 OK    | `application/octet-stream` | Binär ström för den sammanfogade arbetsboksfilen. |

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Sammanfogningen lyckades; svaret innehåller åtgärdens detaljer.  |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad         | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda API:et för kalkylarksammanfogning?

### **Utbildning och akademiska tillämpningar**

- **Studentuppgiftsbetygssättning** – Sammanfoga flera studentuppgiftsfiler för enhetliga kommentarer och betygssättning.
- **Forskningsdatainsamling** – Konsolidera datasamlingar från olika experimentgrupper.
- **Lärmaterialsskapande** – Kombinera övningar från flera kapitel till en enda frågesamlingsarbetsbok.

### **Datahantering och analys**

- **Integrering av mindre datamängder** – Sammanfoga CSV- eller Excel-filer som exporterats från olika källor.
- **Förbehandling inför dataanalys** – Kombinera relevanta datafiler innan analys görs.
- **Fylla i mallar med data** – Fylla förinställda rapportmallar med sammanfogad data.

### **Utveckling och teknisk support**

- **Förberedelse av testdata** – Sammanfoga flera testfallsfiler för automatiserad testning.
- **Loggfilanalys** – Konsolidera Excel-rapporter över systemloggar från olika tidsperioder.
- **Konfigurationshantering** – Sammanfoga flera konfigurationskalkylark till en enhetlig konfigurationsfil.

## Varför bör du använda API:et för kalkylarksammanfogning?

- **Utvecklarvänlig** – SDK-bibliotek finns tillgängliga för många språk, vilket minskar utvecklingsarbetet jämfört med att bygga en egen lösning.
- **Sänkta arbetskostnader** – Upphäver behovet av särskilt personal för manuell dokumentkonsolidering.
- **Betala per användning** – Betala endast för de API-anrop du faktiskt gör; inga förstainvesteringar.
- **Inga underhållskostnader** – Inga servrar att underhålla, inga programuppdateringar och inga kompatibilitetsproblem.

## Hur används API:et för kalkylarksammanfogning med SDK:er?

### OpenAPI-specifikation

<a href="https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets" rel="noopener noreferrer">OpenAPI-specifikationen</a> tillhandahåller en maskinläsbar beskrivning av API:t, vilket möjliggör direkta REST-interaktioner.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/merge/spreadsheet?outFormat=PDF&mergeInOneSheet=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/sökväg/till/Book1.xlsx" \
  -F "Spreadsheet=@/sökväg/till/Book2.xlsx"
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och låter dig importera data till ett kalkylarksblad med kort kod. Kontrollera <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{</tab>}}
{{< /tabs >}}

---