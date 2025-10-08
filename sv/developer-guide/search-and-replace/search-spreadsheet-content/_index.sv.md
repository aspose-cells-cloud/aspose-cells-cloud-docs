---
title: Aspose.Cells Cloud Web API - Sök kalkylbladsinnehåll
second_title: Documen
ArticleTitle: Search Spreadsheet Conten
linktitle: Sök i kalkylbladsinnehåll
type: docs
url: /sv/search-spreadsheet-content/
keywords: Excel, Office Cloud, REST API, Spreadsheet Search, PDF Export, CSV Handling, JSON Formatting, Markdown Integration, Match Empty Cells in Exce
description: Sök effektivt efter text i lokala kalkylbladsfiler med hjälp av vår API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylbladssökning, PDF Export, CSV-hantering, JSON-formatering, Markdown-integration, Matcha tomma Cells i Excel
---
Sök efter text i lokala kalkylbladsfiler med hjälp av vår API.

## **Sök kalkylbladsinnehåll API**

```
PUT http://api.aspose.cloud/v4.0/cells/search/content
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen för att söka.|
|söktext|Sträng|Fråga|Texten att söka efter i kalkylbladet.|
|ignorerarFall|Booleansk|Fråga|Ange om gemener och versaler ska ignoreras i sökningen.|
|arbetsblad|Sträng|Fråga|Ange vilket kalkylblad du vill söka i.|
|cellArea|Sträng|Fråga|Ange området för cellerna som ska sökas.|
|område|Sträng|Fråga|Regionsinställningen för kalkylbladet.|
|lösenord|Sträng|Fråga|Lösenordet som krävs för att öppna kalkylbladsfilen.|

### **Svar**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Var ska vi använda sökinnehållet i kalkylbladet API?

När du behöver söka efter innehåll i kalkylarket kan du använda API.

## Varför ska du använda sökinnehållet i kalkylbladet API?

- Sök enkelt efter innehåll i ett kalkylblad med denna API.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du sökningen efter trasiga länkar i kalkylbladet API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera sökinnehåll i kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
