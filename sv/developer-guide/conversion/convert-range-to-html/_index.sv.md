---
title: Aspose.Cells Cloud Web API - Konvertera kalkylbladsområde till HTM
second_title: Documen
ArticleTitle: Converting Spreadsheet Range to Htm
linktitle: Konvertera intervall till HTM
type: docs
url: /sv/convert-range-to-html/
keywords: Convert a spreadsheet range data to a html file, Spreadsheet Conversion, Excel Conversio
description: Konvertera ett intervall från en lokal kalkylbladsfil/Excel till en html-fil med Aspose.Cells Cloud Web API
weight: 100
kwords: Konvertera intervall till html, kalkylblad, Excel
---
Konvertera ett intervalldata från en lokal kalkylbladsfil/Excel till en html-fil.

## **Konvertera intervall till HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/html
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|------------|--|------------------------|-------------------------------------------------|
| Kalkylblad|Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| arbetsblad| Sträng| Fråga| Namnet på kalkylbladet i kalkylbladet.|
| räckvidd| Sträng| Fråga| Cellområdet som ska konverteras, t.ex. A1:C10.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
| outStorageName| Sträng| Fråga| Namn på utdatafilens lagringsplats.|
| teckensnittPlats| Sträng| Fråga| Ange anpassade teckensnitt som ska användas.|
| område| Sträng| Fråga| Inställningen för kalkylbladets region.|
| lösenord| Sträng| Fråga| Lösenord för att öppna kalkylbladsfilen.|

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

## Varför ska du använda Konvertera intervall till Html API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man konvertera intervallet till Html API med SDK:er?

### Konvertera intervall till HTML API Specifikation

 De[Konvertera intervall till HTML API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToHtml) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera intervalldata till en html-fil med kort kod.
 Besök gärna[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en omfattande lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
