---
title: Aspose.Cells Cloud Web API - Konvertera ett kalkylbladsområde till en CSV-fil
second_title: Documen
ArticleTitle: Convert a Spreadsheet Range data to a CSV file.
linktitle: Konvertera intervall till CS
type: docs
url: /sv/convert-range-to-csv/
keywords: Convert range to csv, convert spreadsheet to csv, Aspose Cloud Web API, cloud conversion, Excel to cs
description: Konvertera ett angivet intervall från en lokal kalkylbladsfil till ett CSV-format med hjälp av Excel API, vilket säkerställer sömlös molnkörning.
weight: 100
kwords: intervall till csv, konvertera kalkylblad till csv, Aspose Cloud Web API, molnkonvertering, Excel till csv
---
 Konvertera ett intervalldata från en lokal kalkylbladsfil/Excel till en[CSV-fil](https://docs.fileformat.com/spreadsheet/csv/) fil.

## **Konvertera intervall till CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen.|
|arbetsblad|Sträng|Fråga|Arbetsbladets namn Spreadsheet/Excel|
|räckvidd|Sträng|Fråga|Ange cellområdet (t.ex. A1:C10).|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken ska lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namn på utdatafilens lagringsplats.|
|teckensnittPlats|Sträng|Fråga|Ange anpassade teckensnitt om det behövs.|
|område|Sträng|Fråga|Definierar kalkylbladets regioninställning.|
|lösenord|Sträng|Fråga|Lösenord krävs för att öppna kalkylbladsfilen.|

### **Svar**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream",
        }
    }
]
```

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Varför ska du använda Konvertera diagram till Csv API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man funktionen Konvertera diagram till CSV API med SDK:er?

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertRangeToCsv) beskriver en offentligt tillgänglig API, som möjliggör REST-interaktioner direkt från en webbläsare.

## Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera intervalldata till en CSV-fil med kort kod.
 Utforska den kompletta listan över Aspose.Cells Cloud SDK:er i vår[GitHub-arkiv](https://github.com/aspose-cells-cloud).

Följande kodexempel illustrerar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
