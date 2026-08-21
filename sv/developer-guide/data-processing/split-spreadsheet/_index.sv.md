---
title: "Aspose.Cells Cloud Split Excel Web API – Dela lokalt Excel till flera filer & exportera till 30+ format"
second_title: "Dokument"
ArticleTitle: "Excel-delningsverktyg – Dela lokal kalkylarkfil i filer i 30+ format"
linktitle: "Dela kalkylark"
type: docs
url: /sv/split-spreadsheet/
keywords: "dela, excel, aspose cells, kalkylarks-API, exportera till pdf, csv, json"
description: "Dela ett lokalt Excel-arbetsboksfil i separata filer med Aspose.Cells Cloud API. Exportera till 30+ format (PDF, CSV, JSON, XLSX, HTML) utan att ladda upp till molnet."
weight: 100
---

Dela en lokal Excel-arbetsbok i separata filer helt — inget molnlagring krävs. Utdata stöder 30+ filformat såsom PDF, CSV, JSON, ODS och XPS.

## **API för att dela kalkylark**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begärparametrar:**

| Parameternamn | Typ     | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                                                    |
| :------------ | :------ | :-------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Fil     | FormData                    | Den lokala kalkylarkfil som ska delas. Format som stöds inkluderar XLSX, XLS, ODS, CSV, etc. Filen bearbetas helt på servern utan att kräva molnlagring.                       |
| from          | Heltal  | Frågesträng                 | Den nollbaserade startindexet för arbetsbladsintervallet som ska delas (t.ex. `0` för det första arbetsbladet).                                                               |
| to            | Heltal  | Frågesträng                 | Den nollbaserade slutindexet för arbetsbladsintervallet som ska delas (t.ex. `2` delar arbetsblad 0, 1 och 2).                                                                |
| outFormat     | Sträng  | Frågesträng                 | Utdataformatet för de delade filerna. Stöder 30+ format såsom `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`.                                                                            |
| outPath       | Sträng  | Frågesträng                 | _(Valfritt)_ Den lokala mappens sökväg där de delade utdatafilerna kommer att sparas. Om utelämnad sparas filerna i en standard temporär plats.                               |
| outStorageName| Sträng  | Frågesträng                 | Lagringsidentifieraren för att organisera utdatafiler. I lokalt bearbetningsläge hänvisar detta oftast till en sessionsbaserad eller användardefinierad lagringsetikett.     |
| fontsLocation | Sträng  | Frågesträng                 | _(Valfritt)_ Anger en lokal eller anpassad teckensnittsmapp för att säkerställa exakt textrendering vid export till PDF- eller bildformat.                                     |
| region        | Sträng  | Frågesträng                 | _(Valfritt)_ Anger lokalen för nummer-, datum- och valutautformning i utdatafilerna (t.ex. `"en-US"`, `"de-DE"`).                                                             |
| password      | Sträng  | Frågesträng                 | _(Valfritt)_ Om den uppladdade kalkylarkfilen är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                                         |

## **Svar**

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

Filen kan laddas ner direkt eller sparas till platsen som anges av `outPath`.

**Detaljerad lyckad svarshändelse**

| Statuskod | Content-Type               | Beskrivning                                     |
| --------- | -------------------------- | ----------------------------------------------- |
| 200 OK    | `application/octet-stream` | Binär ström av den sammanfogade arbetsboksfilen. |

**HTTP-statuskoder**

| Kod | Betydelse               | Beskrivning                                                       |
| --- | ----------------------- | ----------------------------------------------------------------- |
| 200 | OK                      | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran        | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs     | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast      | Den uppladdade filen överskrider storleksgränsen.                |
| 500 | Internt serverfel       | Oväntat serverfel.                                                |

## Var bör vi använda API:et för att dela kalkylark?

- **Avdelningars datafördelning**: Dela en enhetlig arbetsbok som innehåller data från flera avdelningar i avdelningsspecifika filer.
- **Regionell rapportfördelning**: Dela nationella försäljningsrapporter i separata regionella rapportfiler.
- **Kunddataskyddad fördelning**: Dela en arbetsbok som innehåller känslig information i en bearbetad kundvynsfil.
- **Periodisk rapportdelning**: Dela automatiskt sammanfattande rapporter i veckovisa eller dagliga rapporter månadsvis.
- **Multiformatfördelning**: Dela en enda Excel-fil i flera formatversioner såsom PDF, CSV, JSON, etc., samtidigt.
- **Mallbaserad delning**: Dela datafiler i standardiserade utdatafiler baserat på fördefinierade mallar.
- **Datakällans förbearbetning**: Dela Excel-filen i en standardiserad CSV-fil innan data läses in i en databas.
- **API-datoförberedelse**: Dela stora dataset i mindre bitar lämpliga för API-överföring.

## Varför bör du använda API:et för att dela kalkylark?

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och tillhandahåller omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskas utvecklingsarbete betydligt.
- **Lägre arbetskostnader**: Minskar behovet av tjänster dedikerade till dokumentkonsolidering.
- **Betala per användning**: Inga förhandsutgiftskostnader; du betalar endast för API-anrop som faktiskt används.
- **Inga underhållskostnader**: Inget behov av att underhålla servrar, uppdatera programvara eller hantera kompatibilitetsproblem.
- **Bevarar komplexa Excel-formateringar** i universellt tillgängligt PDF-format.

## Hur man använder API:et för att dela kalkylark med SDK:er

### API-specifikation för att dela kalkylark

[API-specifikationen för att dela kalkylark](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.
Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljerna på låg nivå, vilket gör det möjligt att dela kalkylarket i separata filer med kort kod.  
Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}