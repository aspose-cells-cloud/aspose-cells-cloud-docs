---
title: Aspose.Cells Cloud Web API - Konvertera kalkylblad till PDF
second_title: Documen
ArticleTitle: Convert Spreadsheet Worksheet to Pd
linktitle: Konvertera arbetsblad till Pd
type: docs
url: /sv/convert-worksheet-to-pdf/
keywords: worksheet to pdf, Excel PDF conversion, REST API, cloud-based conversion, spreadsheet to PD
description: Konvertera ett kalkylblad från ett kalkylblad på din lokala hårddisk till en PDF-fil med hjälp av vår molnbaserade API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, konvertera kalkylblad till PDF, molnkonvertering, lokal filkonvertering
---
Konvertera ett lokalt kalkylblad/Excel-arbetsblad till en PDF-fil med Aspose.Cells Cloud Web API.

## **Konvertera arbetsblad till PDF API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|-----------------|-|-----------------------|------------------------------------|
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| arbetsblad|Sträng| Fråga|Namn på kalkylbladet i kalkylbladet.|
| utväg|Sträng| Fråga|(Valfritt) Mappsökvägen för att lagra arbetsboken; standardvärdet är null.|
| outStorageName|Sträng| Fråga| Namnet på utdatafilens lagringsplats.|
| teckensnittPlats|Sträng| Fråga| Ange anpassade teckensnitt.|
| område|Sträng| Fråga| Definiera kalkylbladets regioninställning.|
|lösenord|Sträng| Fråga|Lösenordet som krävs för att öppna kalkylbladsfilen.|

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

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Varför ska du använda Konvertera tabell till PDF API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man Konvertera tabellen till PDF API med SDK:er?

### Konvertera tabell till PDF API Specifikation

 De[Konvertera tabell till PDF API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertWorksheetToPdf) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera data från en kalkylbladstabell till en PDF-fil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPdf.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPdf.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPdf.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPdf.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPdf.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPdf.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPdf.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPdf.go" >}}
{{< /tab >}}
{{< /tabs >}}
