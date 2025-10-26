---
title: Aspose.Cells Cloud Web API - Sök efter kalkylbladsinnehåll i fjärrkalkylblad
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: Sök innehåll i fjärrarbetsblad
type: docs
url: /sv/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: Sök effektivt efter text i ett kalkylblad i ett fjärrkalkylblad som lagras i molnet
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad, Fjärrsökning i kalkylblad
---
Sök efter specifik text i ett kalkylblad i ett fjärrkalkylblad som lagras i molnlagring.

## **Gränssnittsdetaljer**

## **Sök innehåll i fjärrarbetsblad**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg|Namnet på arbetsboksfilen som ska sökas i.|
|arbetsblad|Sträng|Väg|Namnet på arbetsbladet.|
|söktext|Sträng|Fråga|Texten som ska sökas.|
|ignorerarFall|Booleansk|Fråga|Anger om gemener och versaler ska ignoreras under sökningen.|
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

## Var ska vi använda sökinnehållet i kalkylbladet i kalkylblad API?

När du behöver söka efter innehåll i kalkylbladet kan du använda API.

## Varför ska du använda sökfunktionen i kalkylbladet i kalkylblad API?

- Sök enkelt innehåll i ett fjärrkalkylblad med denna API.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du sökningen efter trasiga länkar i kalkylbladet i kalkylbladet API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera sökinnehåll i kalkylblad eller kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
