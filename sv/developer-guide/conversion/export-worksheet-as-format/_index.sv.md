---
title: Aspose.Cells Cloud Web API - Exportera ett kalkylblad som en filformat
second_title: Documen
ArticleTitle: Export a Spreadsheet Worksheet as a Format fil
linktitle: Exportera arbetsblad
type: docs
url: /sv/export-worksheet-as-format/
keywords: Export worksheet, Cloud storage conversion, File format transformation, API for spreadsheet
description: Konverterar effektivt ett kalkylblad från molnlagring till olika format som PDF, CSV och bilder
weight: 100
kwords: Exportera kalkylblad, Molnkonvertering, PDF, Bildformat, Excel, REST API, CSV, JSON, Markdown, Hantera tomma celler i Excel
---
Exportera ett molnkalkylblad/Excel-kalkylblad till en fil i ett annat format med Aspose.Cells Cloud Web API.

## **Exportera kalkylblad som format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|namn|Sträng|Väg|(Obligatoriskt) Namnet på den arbetsboksfil som ska hämtas.|
|arbetsblad|Sträng|Väg|(Obligatoriskt) Det specifika kalkylbladet som ska konverteras.|
|formatera|Sträng|Fråga|(Obligatoriskt) Önskat utdataformat (t.ex. "png", "pdf", "svg").|
|mapp|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|lagringsnamn|Sträng|Fråga|(Valfritt) Namnet på den anpassade molnlagringen. Använd standardlagring om det utelämnas.|
|utväg|Sträng|Fråga|(Valfritt) Sökvägen till utdatamappen. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|(Valfritt) Lagringsnamn för utdatafil.|
|teckensnittPlats|Sträng|Fråga|(Valfritt) Ange anpassade teckensnitt om det behövs.|
|område|Sträng|Fråga|Inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet för att komma åt kalkylbladsfilen.|

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

## Varför ska du använda kalkylbladet Exportera kalkylblad som format API?

- Du kan konvertera molnfiler till olika format när som helst och var som helst.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man kalkylbladet Exportera kalkylblad som format API med SDK:er?

### Exportera kalkylblad som format API Specifikation

 De[Exportera kalkylblad som format API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ExportWorksheetAsFormat) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan exportera ett kalkylblad till en formatfil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
