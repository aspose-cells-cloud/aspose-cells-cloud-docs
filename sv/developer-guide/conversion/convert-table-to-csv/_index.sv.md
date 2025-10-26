---
title: Aspose.Cells Cloud Web API - Konvertera data från en kalkylbladstabell till en CSV-fil
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Csv file
linktitle: Konvertera tabell till CS
type: docs
url: /sv/convert-table-to-csv/
keywords: convert table to csv, convert spreadsheet to csv, Excel to CSV conversion, cloud conversio
description: Konverterar effektivt en tabell från ett kalkylblad på din lokala hårddisk till en CSV-fil med hjälp av vår API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Tabell till CSV, Lokal till molnkonvertering
---
Konvertera en lokal tabell av typen kalkylblad/Excel till en CSV-fil.

## **Konvertera tabell till CSV API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|-------------|-|------------------------|-------------------------------------------|
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| arbetsblad|Sträng| Fråga| Namn på kalkylbladet i kalkylbladet.|
| tabellnamn|Sträng| Fråga|Namn på tabellen som ska konverteras.|
| utväg|Sträng| Fråga| (Valfritt) Mappsökväg där arbetsboken lagras; standardvärdet är null.|
| outStorageName|Sträng| Fråga| Namn på utdatafilens lagringsplats.|
| teckensnittPlats|Sträng| Fråga| Sökväg för att använda anpassade teckensnitt.|
| område|Sträng| Fråga| Definierar kalkylbladets regioninställning.|
| lösenord|Sträng| Fråga| Lösenord för att öppna kalkylbladsfilen.|

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

## Varför ska du använda Konvertera tabell till Csv API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man konverteringstabellen till CSV API med SDK:er?

### Konvertera tabell till Csv API Specifikation

 De[Konvertera tabell till Csv API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToCsv) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera data från en kalkylbladstabell till en CSV-fil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCsv.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCsv.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCsv.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCsv.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCsv.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCsv.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCsv.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCsv.go" >}}
{{< /tab >}}
{{< /tabs >}}
