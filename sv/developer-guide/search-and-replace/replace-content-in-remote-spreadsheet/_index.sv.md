---
title: Aspose.Cells Molnwebb API - Ersätt innehåll i fjärrkalkylblad
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: Ersätt innehåll i fjärrkalkylblad
type: docs
url: /sv/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: Ersätt effektivt text i fjärrkalkylblad med hjälp av Excel API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Ersätt innehåll i Excel, Molnbaserad textersättning, Ändra text i fjärrkalkylblad
---
Ersätt effektivt specificerad text i en fjärransluten kalkylbladsfil.

## **Ersätt innehåll i fjärrkalkylblad API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| namn| Sträng| Väg| Namnet på den arbetsboksfil som ska ändras.|
| söktext| Sträng| Fråga| Texten att söka efter i kalkylbladet.|
| ersätt text| Sträng| Fråga| Texten som ska ersätta de funna förekomsterna.|
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

## Var ska vi använda Ersätt innehåll i fjärrkalkylblad API?

När du behöver ersätta innehåll i ett fjärrkalkylblad kan du använda API.

## Varför ska du använda Ersätt innehåll i fjärrkalkylblad API?

- Ersätt snabbt innehåll i fjärrkalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Ersätt innehåll i fjärrkalkylblad API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera ersättning av innehåll i kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:
