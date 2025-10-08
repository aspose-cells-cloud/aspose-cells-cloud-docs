---
title: Aspose.Cells Cloud Web API - Konvertera ett kalkylblad till en PDF-fil
second_title: Documen
ArticleTitle: Converting a Spreadsheet Chart to a Pdf file
linktitle: Konvertera diagram till PD
type: docs
url: /sv/convert-chart-to-pdf/
keywords: convert an Excel chart to pdf, convert spreadsheet to pdf, Aspose Cloud Web  API, cloud conversion, Excel to PD
description: Denna API konverterar diagram från kalkylblad som finns på en lokal hårddisk till PDF-filer sömlöst.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylbladskonvertering, PDF, CSV, JSON, Markdown, Konvertera diagram till PDF, Molnkonvertering
---
 Konvertera ett diagram från en lokal kalkylbladsfil/Excel till en[PDF](https://docs.fileformat.com/pdf/) fil.

## **Konvertera diagram till PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|-------------- ||--------------------- |--------------------------------------------------- |
| Kalkylblad|Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| arbetsblad| Sträng| Fråga| Namnet på kalkylbladet som innehåller diagrammet.|
| diagramindex|Heltal| Fråga| Indexet för diagrammet som ska konverteras.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där den konverterade filen lagras. Standardvärdet är null.|
| outStorageName| Sträng| Fråga| Namn på utdatafilens lagringsplats.|
| teckensnittPlats| Sträng| Fråga| Använd anpassade teckensnitt om det behövs.|
| område| Sträng| Fråga| Inställningen för kalkylbladets region.|
| lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen.|

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

## Var ska du använda Konvertera diagram till PDF API?

- Exportera diagrammen i kalkylbladet som PDF.

## Varför ska du använda Konvertera diagram till PDF API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man funktionen Konvertera diagram till PDF API med SDK:er?

### Konvertera diagram till PDF API Specifikation

 De[Konvertera diagram till PDF API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertChartToPdf) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan konvertera ett diagram till en PDF-fil med kort kod.
Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
