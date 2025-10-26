---
title: Aspose.Cells Cloud Web API - Flytta ett kalkylblad till en ny position i kalkylarket
second_title: Documen
ArticleTitle: Move worksheet to new position in Spreadshee
linktitle: Flytta kalkylblad i kalkylblad
type: docs
url: /sv/move-worksheet-in-spreadsheet/
keywords: Move Worksheet, Aspose.Cells Cloud Web API, Spreadsheet Management, Worksheet Positioning, Workbook Organization, Excel AP
description: MoveWorksheet API gör det möjligt för användare att effektivt flytta ett angivet kalkylblad i en arbetsbok, vilket förbättrar organisationen och tillgängligheten av kalkylbladsdata.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, Flytta arbetsblad, Arbetsboksorganisation, PDF, CSV, JSON, Markdown
---
Flytta ett kalkylblad till en ny position i ett kalkylblad.

## **Flytta kalkylblad från kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/move/worksheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen.|
|arbetsblad|Sträng|Fråga|Det aktuella namnet på kalkylbladet som ska flyttas.|
|placera|Heltal|Fråga|Den nya positionen för arbetsbladet.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namn på utdatafilens lagringsplats.|
|område|Sträng|Fråga|Inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet för att öppna kalkylbladsfilen.|

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

## Var ska vi använda flyttbladet i kalkylblad API?

När du behöver flytta ett kalkylblad till en ny position i kalkylblad kan du använda API.

## Varför ska du använda flyttbladet i kalkylblad API?

- Flytta snabbt kalkylblad från kalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du flyttningsarket i kalkylblad API med SDK:er

### Flytta kalkylblad i kalkylblad API Specifikation

 De[Flytta kalkylblad i kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/ManagementController/MoveWorksheetInSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att underlätta direkta REST-interaktioner från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan flytta kalkylblad i kalkylbladet med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.
Följande kodexempel visar hur man anropar webbtjänsterna Aspose.Cells med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
