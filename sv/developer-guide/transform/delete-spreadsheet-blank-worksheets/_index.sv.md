---
title: Aspose.Cells Cloud Web API - Ta bort tomma kalkylblad i kalkylblad
second_title: Documen
ArticleTitle: Delete Blank Worksheets in a Spreadshee
linktitle: Ta bort tomt kalkylblad
type: docs
url: /sv/delete-spreadsheet-blank-worksheets/
keywords: Aspose.Cells Cloud Web API, Delete Blank Worksheets, Spreadsheet Managemen
description: Ta effektivt bort alla tomma kalkylblad från ett kalkylblad som inte innehåller några data eller objekt. Optimera din arbetsbok för bättre prestanda.
weight: 100
kwords: Excel, Office Moln, REST, Kalkylblad, PDF, CSV, JSON, Markdown
---
Ta bort alla tomma kalkylblad som inte innehåller några data eller andra objekt från ett Excel-kalkylblad.

## **Ta bort kalkylblad Tomt Arbetsblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/delete/blank-worksheets
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen som ska rensas.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Lagringsnamn för utdatafil.|
| område| Sträng| Fråga| Inställningen för kalkylbladets region.|
| lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen.|

## **Svar**

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

## Var ska vi använda Ta bort tomma kalkylblad API?

När du behöver transformera data kan du använda API.

## Varför ska du använda Ta bort tomma kalkylblad API?

- Ta snabbt bort alla tomma kalkylblad som inte innehåller data eller andra objekt från ett Excel-kalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Ta bort tomma kalkylblad API med SDK:er

### Ta bort tomma kalkylblad API Specifikation

 De[Ta bort tomma kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankWorksheets) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan ta bort tomma kalkylblad med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankWorksheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankWorksheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankWorksheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankWorksheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankWorksheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankWorksheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankWorksheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankWorksheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
