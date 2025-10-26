---
title: Aspose.Cells Cloud Web API - Konvertera data från en kalkylbladstabell till en JSON-fil
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Json file
linktitle: Konvertera tabell till JSO
type: docs
url: /sv/convert-table-to-json/
keywords: Excel API, JSON conversion, spreadsheet to JSON, cloud file conversion, REST API, Aspose.Cell
description: Konvertera en lokal kalkyltabell till JSON-format effektivt med hjälp av Excel API. Den här metoden möjliggör sömlös filbehandling utan behov av molnlagring.
weight: 100
kwords: Excel API, JSON-konvertering, molnfilkonvertering, kalkylblad, REST API, Aspose.Cells, bearbetning av lokal enhet, filformatkonvertering
---
Konvertera en lokal tabell av typen kalkylblad/Excel till en json-fil med Aspose.Cells Cloud Web API.

## **Konvertera tabell till Json API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|-------------|-|-----------------------|----------------------------------------------|
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| arbetsblad|Sträng| Fråga| Ange kalkylbladets namn.|
| tabellnamn|Sträng| Fråga| Ange namnet på tabellen som ska konverteras.|
| utväg|Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras; standardvärdet är null.|
| outStorageName|Sträng| Fråga| Ange namnet på utdatafilens lagringsplats.|
| teckensnittPlats|Sträng| Fråga| Använd anpassade teckensnitt för konvertering.|
| område|Sträng| Fråga|Definiera regioninställningarna för kalkylbladet.|
| lösenord|Sträng| Fråga| Lösenordet som krävs för att öppna kalkylbladsfilen.|

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

## Varför ska du använda Konvertera tabell till Json API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man konverteringstabellen till JSON API med SDK:er?

### Konvertera tabell till Json API Specifikation

 De[Konvertera tabell till Json API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToJson) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera data från en kalkylbladstabell till en JSON-fil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}
{{< /tab >}}
{{< /tabs >}}
