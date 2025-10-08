---
title: Aspose.Cells Cloud Web API - Konvertera ett kalkylbladsdiagram till en bild
second_title: Documen
ArticleTitle: Convert a Spreadsheet Chart to an Imag
linktitle: Konvertera diagram till bild
type: docs
url: /sv/convert-chart-to-image/
keywords: convert chart to image, png, svg, tiff, jpg, bmp, convert a Spreadsheet chart to png,convert an Excel chart to svg, convert an Excel chart to jpg, convert a Spreadsheet chart to bmp, convert an Excel chart to tif
description: Konvertera ett diagram från ett lokalt kalkylblad/Excel-fil till en bildfil med Aspose.Cells Cloud Web API
weight: 100
kwords: konvertera ett Excel-diagram till bild, png, svg, tiff, jpg, bmp, kalkylblad
---
Konvertera ett diagram från en lokal kalkylbladsfil/Excel till en bildfil. Stöds.**BILDFORMAT:** [PNG](https://docs.fileformat.com/image/png/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/)

## **Konvertera diagram till bild API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/image
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen som innehåller diagrammet.|
|arbetsblad|Sträng|Fråga|Ange kalkylbladets namn om tillämpligt.|
|diagramindex|Heltal|Fråga|Index för diagrammet som ska konverteras.|
|formatera|Sträng|Fråga|(Obligatoriskt) Önskad bildtyp (t.ex. svg, png, jpg).|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras; standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namn på lagringsplatsen för utdatafilen.|
|teckensnittPlats|Sträng|Fråga|Ange anpassade teckensnitt om det behövs.|
|område|Sträng|Fråga|Ange kalkylbladsregionen.|
|lösenord|Sträng|Fråga|Lösenordet för att öppna kalkylbladsfilen.|

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

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Var ska du använda Konvertera diagram till bild API?

- Exportera diagrammen i kalkylbladet som bilder.

## Varför ska du använda Konvertera diagram till bild API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man funktionen Konvertera diagram till bild API med SDK:er?

### Konvertera diagram till bild API Specifikation

 De[Konvertera diagram till bild API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToImage) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan konvertera ett diagram till en bild med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{< /tab >}}
{{< /tabs >}}
