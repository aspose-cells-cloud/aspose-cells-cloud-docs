---
title: Aspose.Cells Cloud Web API - Konvertera data från en kalkylbladstabell till en bild
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to an Imag
linktitle: Konvertera tabell till bild
type: docs
url: /sv/convert-table-to-image/
keywords: table to image, Aspose.Cells Cloud Web API, cloud conversion, spreadsheet to image, image format
description: Konvertera en lokal kalkyltabell till en bildfil effektivt med hjälp av Aspose.Cells Cloud Web API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, konvertera tabell till bild, molnkonvertering, bildfilformat, kalkylbladskonvertering
---
 Konvertera data från ett lokalt kalkylblad/en Excel-tabell till en bild. Stöds.**BILDFORMAT:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Konvertera tabell till bild API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/image
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen.|
|arbetsblad|Sträng|Fråga|Arbetsbladets namn Spreadsheet/Excel|
|tabellnamn|Sträng|Fråga|Namn på tabellen som ska konverteras.|
|formatera|Sträng|Fråga|Önskat bildfilformat (t.ex. png, svg).|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där den konverterade bilden ska lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Ange namnet på utdatafilens lagringsplats.|
|teckensnittPlats|Sträng|Fråga|Använd anpassade teckensnitt om det behövs.|
|område|Sträng|Fråga|Definierar inställningarna för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenord krävs för att komma åt kalkylbladsfilen.|

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

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Varför ska du använda Konvertera tabell till bild API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man funktionen Konvertera tabell till bild API med SDK:er?

### Konvertera tabell till bild API Specifikation

 De[Konvertera tabell till bild API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToImage) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan konvertera data från ett kalkylblad till en bild med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToSvg.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToSvg.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToSvg.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToSvg.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToSvg.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToSvg.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToSvg.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToSvg.go" >}}
{{< /tab >}}
{{< /tabs >}}
