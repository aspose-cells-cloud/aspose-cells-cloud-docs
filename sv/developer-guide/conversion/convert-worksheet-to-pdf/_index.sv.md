---
title: "Aspose.Cells Cloud Web API – Konvertera ett lokalt Excel-ark till en PDF-fil – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar ett lokalt kalkylblad till en PDF-fil: Steg-för-steg-guide"
linktitle: "Konvertera kalkylblad till PDF"
type: docs
url: /sv/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel till PDF, kalkylbladkonvertering, REST API, molnkonvertering, kalkylark PDF, API-slutpunkt, PDF-generering"
description: "Använd Aspose.Cells Cloud API för att snabbt och säkert konvertera ett kalkylblad från en lokal Excel-fil till ett PDF-dokument."
weight: 100
---

Exportera ett kalkylblad från en lokal Excel-fil till en [PDF](https://docs.fileformat.com/pdf/)-fil med hjälp av Cloud API.

## **Konvertera kalkylblad till PDF API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar:**

| Parameternamn   | Typ    | Path/Query String/HTTPBody | Beskrivning                                                      |
| --------------- | ------ | -------------------------- | ---------------------------------------------------------------- |
| Spreadsheet     | Fil    | FormData                   | Ladda upp kalkylarkfilen.                                        |
| worksheet       | Sträng | Query                      | Namn på kalkylbladet i kalkylarket.                              |
| outPath         | Sträng | Query                      | (Valfritt) Mappens sökväg för att lagra arbetsboken; standard är null. |
| outStorageName  | Sträng | Query                      | Namnet på lagringsplatsen för utdatafilen.                       |
| fontsLocation   | Sträng | Query                      | Använd anpassade typsnitt för PDF:en.                            |
| region          | Sträng | Query                      | Definiera inställningen för kalkylarkregion.                     |
| password        | Sträng | Query                      | Lösenordet som krävs för att öppna kalkylarkfilen.               |

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

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## **Var bör du använda API:et för att konvertera kalkylblad till PDF?**

- **Finansiella rapporter**: Konvertera balansräkningar, resultaträkningar (specifika tabeller) till PDF för revisionsklar dokumentation.
- **Försäljningsrapporter**: Omvandla dashboards eller provisionberäkningar till distribuerbara PDF-filer.
- **Operativa metricer**: Exportera KPI-tabeller och prestandametricer som formella PDF-rapporter.
- **Kontraktdata**: Exportera prislistor och serviceavtal från kalkylark till PDF-bilagor.
- **Revisionsspår**: Bevara finansiella kalkylblad som oredigerbara PDF-bevis.
- **Portföljsummeringar**: Exportera tabeller över investeringsprestanda som PDF-rapporter redo för kundanvändning.
- **Kvalitetskontrollrapporter**: Exportera inspektionskalkylblad till PDF för att spara i efterlevnadsdokumentation.
- **Lagersummeringar**: Omvandla lagerkalkylblad till PDF för ledningsöversikt.

## **Varför bör du använda API:et för att konvertera kalkylblad till PDF?**

- **Utvecklarvänlig**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskar detta utvecklingsarbetet avsevärt.
- **Kostnadseffektiv**: Du kan konvertera tabelldata utan att först ladda upp hela arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Formatbevarande**: Bevarar komplexa Excel-formateringar i ett universellt tillgängligt PDF-format.

## **Hur använder du API:et för att konvertera kalkylblad till PDF med SDK:er?**

### Specifikation för API:et för att konvertera kalkylblad till PDF

[Specifikation för API:et för att konvertera kalkylblad till PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och gör det möjligt att konvertera tabelldata i kalkylark till en PDF-fil med minimal kod. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}