---
title: Aspose.Cells Cloud Web API - Sök efter trasiga länkar i fjärrkalkylblad
second_title: Documen
ArticleTitle: Search for Broken Links in Remote Spreadsheet
linktitle: Sök i fjärrkalkylblad Trasig länk
type: docs
url: /sv/search-broken-links-in-remote-spreadsheet/
keywords: broken links, remote spreadsheet, Excel API, cloud storage, hyperlink checker, dead URL detection, REST AP
description: Sök effektivt efter trasiga länkar i fjärrkalkylblad som lagras i molnmiljöer
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, trasiga länkar, hyperlänkvalidering, molnlagring
---
Sök efter trasiga länkar i fjärrkalkylblad som lagras i molnmiljöer.

## **Sök efter trasiga länkar i fjärrkalkylblad API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg|Namnet på den arbetsboksfil som ska sökas i.|
|arbetsblad|Sträng|Fråga|Ange kalkylbladet för sökningen.|
|cellArea|Sträng|Fråga|Ange cellområdet för sökningen.|
|mapp|Sträng|Fråga|Mappsökvägen där arbetsboken lagras.|
|lagringsnamn|Sträng|Fråga|(Valfritt) Namnet på lagringsplatsen om anpassad molnlagring används. Standardlagring används om den utelämnas.|
|område|Sträng|Fråga|Inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet för att öppna kalkylbladsfilen.|

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

## Var ska vi använda Sök efter trasiga länkar i kalkylbladet API?

När du behöver söka efter trasiga länkar i kalkylarket kan du använda API.

## Varför ska du använda Sök efter trasiga länkar i kalkylbladet API?

- Sök effektivt efter trasiga länkar i fjärrkalkylblad som lagras i molnmiljöer.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du sökningen efter trasiga länkar i kalkylbladet API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/SearchController/SearchBrokenLinksInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera sökningar som är trasiga i kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
