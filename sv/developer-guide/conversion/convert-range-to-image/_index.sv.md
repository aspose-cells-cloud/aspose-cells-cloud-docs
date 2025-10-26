---
title: Aspose.Cells Cloud Web API - Konvertera ett kalkylbladsintervalldata till en bild
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to an Imag
linktitle: Konvertera intervall till bild
type: docs
url: /sv/convert-range-to-image/
keywords: Aspose.Cells Cloud Web API, Convert Range to Image, Spreadsheet to Image, Cloud Conversion, Image Format
description: Konvertera ett intervalldata från en lokal kalkylbladsfil/Excel till en bildfil
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, Bildkonvertering, PNG, SVG, TIFF, JSON, Markdown
---
Konvertera ett intervalldata från en lokal kalkylbladsfil/Excel till en bildfil. Stöds.**BILDFORMAT:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Konvertera intervall till bild API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen för konvertering.|
|arbetsblad|Sträng|Fråga|Arbetsbladets namn Spreadsheet/Excel|
|räckvidd|Sträng|Fråga|Definiera cellområdet som ska konverteras (t.ex. A1:C10).|
|formatera|Sträng|Fråga|Ange utdatafilformatet (t.ex. png, svg, tiff).|
|skriv utRubriker|Booleansk|Fråga|Ange om rad- och kolumnrubriker ska skrivas ut.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras; standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namn på utdatafilens lagringsplats.|
|teckensnittPlats|Sträng|Fråga|Anpassade teckensnitt att använda för konverteringen.|
|återgå|Sträng|Fråga|Definiera kalkylbladets regioninställning.|
|lösenord|Sträng|Fråga|Lösenord för att öppna kalkylbladsfilen om den är skyddad.|

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

## Varför ska du använda Konvertera intervall till bild API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man funktionen Konvertera intervall till bild API med SDK:er?

### Konvertera intervall till bild API Specifikation

 De[Konvertera intervall till bild API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToImage) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från din webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan konvertera intervalldata till en bild med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
