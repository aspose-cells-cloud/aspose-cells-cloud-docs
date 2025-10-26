---
title: Aspose.Cells Cloud Web API - Ersätt kalkylbladsinnehåll i fjärrkalkylblad
second_title: Documen
ArticleTitle: Replace Worksheet Content in Remote a Spreadshee
linktitle: Ersätt innehållet i fjärrarbetsbladet
type: docs
url: /sv/replace-content-in-remote-worksheet/
keywords: Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integratio
description: Ersätt effektivt text i kalkylbladet i ett fjärrkalkylblad med hjälp av Aspose.Cells API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad, ReplaceContentInRemoteWorksheet
---
Ersätt effektivt specificerad text i ett kalkylblad i en fjärrkalkylbladsfil.

## **Ersätt innehåll i fjärrarbetsblad API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| namn| Sträng| Väg| Namnet på den arbetsboksfil som ska ändras.|
| arbetsblad| Sträng| Väg| Ange kalkylbladet för ersättningen.|
| söktext| Sträng| Fråga| Texten att söka efter i kalkylbladet.|
| ersätt text| Sträng| Fråga| Texten som den sökta texten ska ersättas med.|
| mapp| Sträng| Fråga| Mappsökvägen där arbetsboken lagras.|
| lagringsnamn| Sträng| Fråga|(Valfritt) Namnet på lagringsutrymmet om anpassad molnlagring används. Använd standardlagring om det utelämnas.|
| område| Sträng| Fråga| Inställningen för kalkylbladets region.|
| lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen.|

### **Svar**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
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

## Var ska vi använda Ersätt innehållet i kalkylbladet i fjärrkalkylbladet API?

När du behöver ersätta innehållet i ett kalkylblad i ett fjärrkalkylblad kan du använda API.

## Varför ska du använda Ersätt innehållet i kalkylbladet i fjärrkalkylbladet API?

- Ersätt snabbt innehållet i kalkylblad i fjärrkalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Ersätt innehållet i kalkylbladet i fjärrkalkylbladet API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera ersättning av innehåll i kalkylblad i kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:
