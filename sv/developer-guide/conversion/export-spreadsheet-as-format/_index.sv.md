---
title: Aspose.Cells Cloud Web API - Exportera ett kalkylblad som en formatfil
second_title: Documen
ArticleTitle: Export a Spreadsheet as a Format fil
linktitle: Exportera kalkylblad som format
type: docs
url: /sv/export-spreadsheet-as-format/
keywords: Export spreadsheet, Aspose.Cells Cloud Web API, Convert spreadsheet, Spreadsheet formats, XLSX, PDF, CSV, JSON, Markdow
description: Konverterar effektivt kalkylblad lagrade i molnlagring till olika format som XLSX, PDF och CSV
weight: 100
kwords: Excel, Office Moln, REST, Kalkylbladskonvertering, PDF, CSV, JSON, Markdow
---
Exportera ett molnkalkylblad/Excel till en annan filformat.

## **Exportera kalkylblad som format API**

```http
GET http://api.aspose.cloud/v4.0/cells/{name}
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
| namn| Sträng| Väg| (Obligatoriskt) Namnet på den arbetsboksfil som ska hämtas.|
| formatera| Sträng| Fråga| (Obligatoriskt) Önskat utdataformat (t.ex. "Xlsx", "Pdf", "Csv").|
| mapp| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
| lagringsnamn| Sträng| Fråga|(Valfritt) Namnet på lagringsutrymmet om anpassad molnlagring används. Använd standardlagring om det utelämnas.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken ska lagras. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Lagringsnamn för utdatafil.|
| teckensnittPlats| Sträng| Fråga| Använd anpassade teckensnitt.|
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

## Varför ska du använda exportkalkylarket som format API?

- Du kan konvertera molnfiler till olika format när som helst och var som helst.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man exportkalkylarket som format API med SDK:er?

### Exportera kalkylblad som format API Specifikation

 De[Exportera kalkylblad som format API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/ExportSpreadsheetAsFormat) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner sömlöst.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan exportera ett kalkylblad till en formaterad fil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med olika SDK:er för Aspose.Cells webbtjänster via:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{< /tab >}}
{{< /tabs >}}
