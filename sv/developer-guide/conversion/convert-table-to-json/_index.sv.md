---
title: "Aspose.Cells Cloud Web API – Konvertera lokalt Excel-tabelldata till en JSON-fil"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar lokalt kalkylbladstabelldata till en JSON-fil: Steg-för-steg-guide"
linktitle: "Konvertera tabell till JSON"
type: docs
url: /convert-table-to-json/
keywords: "Excel, API, JSON, konvertering, moln, fil, kalkylark"
description: "Använd Aspose.Cells Cloud API för att omvandla en lokal Excel-tabell till en JSON-fil med ett enda PUT-anrop. Inkluderar cURL-exempel, parametrar och SDK-utdrag för C#, Java, Python och mer."
weight: 100
---

Konvertera lokalt kalkylark/Excel-tabell till en **JSON**-fil med Aspose.Cells Cloud Web API.

## **Konvertera tabell till JSON – API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parametername      | Typ    | Plats     | Beskrivning                                                                                      |
| ------------------ | ------ | --------- | ------------------------------------------------------------------------------------------------ |
| **Spreadsheet**    | Fil    | FormData  | Den Excel-fil som ska laddas upp.                                                               |
| **worksheet**      | Sträng | Fråga     | Namn på kalkylbladet som innehåller tabellen.                                                   |
| **tableName**      | Sträng | Fråga     | Namn på tabellen som ska konverteras.                                                            |
| **outPath**        | Sträng | Fråga     | (Valfritt) Mappens sökväg där den resulterande JSON-filen ska lagras; standardvärdet är **null**. |
| **outStorageName** | Sträng | Fråga     | (Valfritt) Namn på lagringsutrymmet där utdatafilen ska placeras.                               |
| **fontsLocation**  | Sträng | Fråga     | (Valfritt) Sökväg till anpassade teckensnitt som används vid konvertering.                      |
| **region**         | Sträng | Fråga     | (Valfritt) Regioninställningar för arbetsboken.                                                 |
| **password**       | Sträng | Fråga     | (Valfritt) Lösenord för att öppna en skyddad arbetsbok.                                         |

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

| Kod | Betydelse              | Beskrivning                                                    |
| --- | ---------------------- | -------------------------------------------------------------- |
| 200 | OK                     | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan     | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig               | Ogiltig eller saknad JWT-token.                                |
| 413 | För stor nyttolast     | Den uppladdade filen överskrider storleksgränsen.              |
| 500 | Internt serverfel      | Oväntat serverfel.                                             |

## **Var bör du använda API:t för att konvertera tabell till JSON?**

- **Realtidsinstrumentpaneler** – Konvertera live-Excel-data till JSON för diagrambibliotek såsom Chart.js eller D3.js.
- **Kalkylark som tjänst** – Exponera Excel-tabeller som JSON-slutpunkter för andra mikrotjänster.
- **Webhook-nyttolast** – Omvandla kalkylarkdata till JSON för webhook-meddelanden.
- **Snabb dataprotypning** – Konvertera snabbt rensad Excel-data till JSON för Python- eller R-analys.
- **Maskininlärningspiprader** – Förbehandla träningsdata som lagras i affärsrelaterade kalkylark.
- **E-handelsoperationer** – Synkronisera produktkataloger eller prislistor till webbplatser via JSON.
- **Rapporteringsautomatisering** – Generera JSON-strömmar från finansiella modeller för automatisk rapportering.
- **Appkonfiguration** – Hantera funktionsswitchar, inställningar eller A/B-testparametrar i Excel → JSON.
- **Stöd för flera språk** – Konvertera lokaliseringsspråkark till JSON för i18n-bibliotek.
- **Dynamiska menyer/navigering** – Lagra webbplatsens navigeringsstrukturer i Excel och distribuera dem som JSON.

## Varför bör du använda API:t för att konvertera tabell till JSON?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK för många språk, vilket minskar utvecklingsarbetet och erbjuder omfattande dokumentation.
- **Kostnadseffektivt** – Konvertera tabelldata utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Modern webb- och mobilt kompatibilitet** – JSON är det ursprungliga dataspåket för webben; API:t låter dig mata live-kalkylarkdata direkt till React, Vue, Angular, mobila appar eller en-sidiga applikationer utan komplex tolkning.
- **Brett språkstöd** – JSON fungerar med nästan alla programmeringsspråk, databaser och webbtjänster.
- **Bevarande av strukturerad data**
  - **Intelligent strukturerkänning** – Konverterar automatiskt tabelldata till korrekta JSON-arrayer/objekt.
  - **Rubrikavbildning** – Använder första raden som JSON-nycklar för rena objektstrukturer.
  - **Datatyper bevaras** – Bevarar tal, datum och booleska värden (inte bara text).

_Versionshistorik:_ Slutpunkten för att konvertera tabell till JSON introducerades med API-version **v4.0** (2024) och är fortfarande den aktuella stabila utgåvan. Tidigare v3.x-slutpunkter är föråldrade.

## Hur använder man API:t för att konvertera tabell till JSON med SDK:er?

### API-specifikation för att konvertera tabell till JSON

[API-specifikation för att konvertera tabell till JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"} tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:t med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
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

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK abstraher lågnivådetaljer, vilket gör att du kan konvertera en kalkylarkstabell till en JSON-fil med minimal kod. Se den officiella GitHub-förrådet för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}