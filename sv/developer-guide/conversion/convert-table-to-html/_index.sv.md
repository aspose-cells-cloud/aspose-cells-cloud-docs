---
title: Aspose.Cells Cloud Web API - Konvertera data från en kalkylbladstabell till en HTML-fil
second_title: Documen
ArticleTitle: Convert a Spreadsheet Table data to a Html fil
linktitle: Konvertera tabell till HTM
type: docs
url: /sv/convert-table-to-html/
keywords: Excel Table to HTML, Spreadsheet Conversion, Aspose.Cells Cloud Web API, REST, Convert Excel to HTML, Table to HTML, Document Conversion, Cloud Service
description: Konvertera enkelt tabeller från lokala kalkylbladsfiler till HTML-format med hjälp av vårt molnbaserade API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, HTML, PDF, CSV, JSON, Markdown, Matcha tomma celler i Excel
---
Konvertera data från ett lokalt kalkylblad/en tabell med Excel till en html-fil.

## **Konvertera tabell till HTML API**

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/html
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen som ska konverteras.|
| arbetsblad| Sträng| Fråga| Arbetsbladets namn Spreadsheet/Excel|
| tabellnamn| Sträng| Fråga| Namnet på tabellen som ska konverteras.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där den konverterade filen ska lagras. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Det angivna lagringsnamnet för utdatafilen.|
| teckensnittPlats| Sträng| Fråga| Ange anpassade teckensnitt för konverteringen.|
| område| Sträng| Fråga| Definiera inställningarna för kalkylbladets region.|
| lösenord| Sträng| Fråga| Lösenordet som krävs för att komma åt kalkylbladsfilen.|

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

## Varför ska du använda Konvertera tabell till HTML API?

- Inget behov av molnlagring, vilket minskar belastningen på molnresurser.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man konvertera tabellen till HTML API med SDK:er?

### Konvertera tabell till HTML API Specifikation

 De[Konvertera tabell till HTML API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ConvertTableToHtml) beskriver ett offentligt tillgängligt programmeringsgränssnitt som låter dig utföra REST-interaktioner direkt från din webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan konvertera data från en kalkylbladstabell till en html-fil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToHtml.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToHtml.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToHtml.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToHtml.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToHtml.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToHtml.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToHtml.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToHtml.go" >}}
{{< /tab >}}
{{< /tabs >}}
