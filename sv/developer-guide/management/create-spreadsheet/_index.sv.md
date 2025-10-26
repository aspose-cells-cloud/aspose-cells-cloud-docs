---
title: Aspose.Cells Cloud Web API - Skapa ett nytt kalkylblad med en kalkylbladsmall
second_title: Documen
ArticleTitle: Build a new Spreadsheet with a spreadsheet template - Timeline WorkPlan Table, Sales Data Comparison, etc
linktitle: Skapa kalkylblad
type: docs
url: /sv/create-spreadsheet/
keywords: Spreadsheet Creation, Excel API, REST API, Office Cloud, Template Support, Productivity Enhancemen
description: Excel API låter användare skapa ett nytt kalkylblad med ett angivet namn, stöder valfria mallar för fördefinierat innehåll eller formatering, vilket förbättrar användarproduktiviteten.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad, Skapa kalkylblad, Mallstöd, Produktivitetsförbättring
---
Skapa ett nytt kalkylblad, som kan vara antingen ett tomt kalkylblad eller ett användbart kalkylblad som skapats baserat på den angivna mallen.

## **Skapa kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|---------- ||----------------------- |----- |
|formatera| Sträng| Fråga| Anger namnet på det nya kalkylarket. Detta namn kommer att användas för att identifiera kalkylarket i systemet.|
| mall| Sträng| Fråga| Valfritt. Om det anges skapas det nya kalkylarket baserat på den angivna mallen. Detta kan vara användbart för att tillämpa fördefinierade layouter och stilar.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
| outStorageName| Sträng| Fråga| Lagringsnamn för utdatafil.|
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

## Var ska vi använda Skapa kalkylblad API?

När du behöver skapa ett nytt kalkylblad kan du använda API.

## Varför ska du använda Skapa kalkylblad API?

- Du kan inte bara skapa ett tomt kalkylblad, utan du kan också skapa ett specifikt kalkylblad baserat på en mall.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Skapa kalkylblad API med SDK:er

### Skapa kalkylblad API Specifikation

 De[Skapa kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan bygga kalkylarket med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
