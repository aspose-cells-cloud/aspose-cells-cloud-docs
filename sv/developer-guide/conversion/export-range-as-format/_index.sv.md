---
title: Aspose.Cells Cloud Web API - Exportera kalkylbladsdata som en formatfil
second_title: Documen
ArticleTitle: Export a Spreadsheet Range data as a Format file
linktitle: Exportera intervall som format
type: docs
url: /sv/export-range-as-format/
keywords: Aspose.Cells Cloud Web API, Export range, Spreadsheet conversion, REST API, PDF, CSV, JSON, Markdown, Excel workshee
description: Konvertera ett angivet område i ett kalkylblad i molnlagring till olika format som PDF, CSV eller bildformat utan att ladda ner filen.
weight: 100
kwords: Kalkylbladskonvertering, REST API, PDF, CSV, JSON, Markdown, Excel-kalkylblad
---
Exportera ett molnbaserat kalkylbladsintervall/Excel till en formatfil. Formatfilen kan sparas i molnet eller exporteras till lokal lagring.

## **Exportera intervall som format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg|(Obligatoriskt) Namnet på den arbetsboksfil som ska hämtas.|
|arbetsblad|Sträng|Väg|Arbetsbladets namn för Spreadsheet/Excel|
|räckvidd|Sträng|Väg|Intervallet som ska konverteras (t.ex. A1:C12).|
|formatera|Sträng|Fråga|(Obligatoriskt) Önskat utdataformat (t.ex. "png", "pdf", "svg").|
|mapp|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|lagringsnamn|Sträng|Fråga|(Valfritt) Namnet på lagringsplatsen om anpassad molnlagring används. Standardlagring används om den utelämnas.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen för utdatafilen. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namnet på utdatafilens lagringsplats.|
|teckensnittPlats|Sträng|Fråga|Placering av anpassade teckensnitt.|
|område|Sträng|Fråga|Kalkylbladets regionsinställning.|
|lösenord|Sträng|Fråga|Lösenordet som krävs för att öppna kalkylbladsfilen.|

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

## Varför ska du använda Exportera kalkylbladsintervallet som format API?

- Du kan konvertera molnfiler till olika format när som helst och var som helst.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man exportkalkylbladsintervallet som format API med SDK:er?

### Exportera intervall som format API Specifikation

 De[Exportera intervall som format API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ExportRangeAsFormat) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan exportera ett kalkylbladsintervalldata till en formatfil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
