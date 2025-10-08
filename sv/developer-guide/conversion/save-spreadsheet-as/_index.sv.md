---
title: Aspose.Cells Cloud Web API - Spara kalkylblad som en filformat
second_title: Documen
ArticleTitle: Save Spreadsheet as a Format fil
linktitle: Spara kalkylblad
type: docs
url: /sv/save-spreadsheet-as/
keywords: spreadsheet conversion, Save as, Excel to PDF, Excel to CSV, RES
description: Konvertera enkelt kalkylblad som lagras i molnet till olika format, inklusive XLSX, PDF och CSV, med hjälp av vår robusta API
weight: 100
kwords: Excel API, Office Moln, REST, Kalkylblad, PDF, CSV, JSON, Markdown, konvertera Excel filer, spara kalkylblad som, Aspose.Cells Cloud Web AP
---
Spara en molnbaserad kalkylbladsfil/Excel som en formatfil till molnlagring.

## **Spara kalkylblad som API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
| namn| Sträng| Väg| (Obligatoriskt) Namnet på arbetsboksfilen som ska konverteras.|
| formatera| Sträng| Fråga| (Obligatoriskt) Önskat utdataformat (t.ex. "Xlsx", "Pdf", "Csv").|
| sparaAlternativData| Klass| Kropp| (Valfritt) Spara alternativdata. Standardvärdet är null.|
| mapp| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
| lagringsnamn| Sträng| Fråga|(Valfritt) Namnet på lagringsutrymmet om anpassad molnlagring används. Använd standardlagring om det utelämnas.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Lagringsnamn för utdatafil.|
| teckensnittPlats| Sträng| Fråga| Använd anpassade teckensnitt.|
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

## Varför ska du använda Spara Spread API?

- Du kan konvertera molnfiler till olika format när som helst och var som helst.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur använder man konverteringstabellen till JSON API med SDK:er?

### Spara kalkylblad som API Specifikation

 De[Spara kalkylblad som API Specifikation](https://reference.aspose.cloud/cells/#/ConversionController/SaveSpreadsheetAs) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan spara ett kalkylblad som en formatfil med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{< /tab >}}
{{< /tabs >}}
