---
title: Aspose.Cells Cloud Web API - Ta bort ett kalkylblad från kalkylarket
second_title: Documen
ArticleTitle: Delete a worksheet from the Spreadshee
linktitle: Ta bort kalkylblad från kalkylblad
type: docs
url: /sv/delete-worksheet-from-spreadsheet/
keywords: delete worksheet, spreadsheet management, Aspose.Cells Cloud Web API, REST API, workbook structure, remove worksheet
description: Denna slutpunkt API gör det möjligt för användare att ta bort ett angivet kalkylblad från en arbetsbok, vilket förenklar hanteringen av arbetsboksstrukturer genom att eliminera onödiga eller redundanta kalkylblad.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Hantera Excel Arbetsblad, Ta bort redundanta arbetsblad
---
Ta bort ett kalkylblad från ett kalkylblad.

## **Ta bort kalkylblad från kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/delete/worksheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:-               |:-     |:-                         |:-           |
| Kalkylblad|Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| arknamn| Sträng| Fråga| Anger namnet eller identifieraren för det kalkylblad som ska tas bort. Denna parameter är obligatorisk och måste matcha namnet på ett befintligt kalkylblad i arbetsboken.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
| outStorageName| Sträng| Fråga| Lagringsnamn för utdatafil.|
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

## Var ska vi använda kalkylbladet Ta bort från kalkylblad API?

När du behöver ta bort ett kalkylblad från kalkylblad kan du använda API.

## Varför ska du använda kalkylbladet Ta bort från kalkylblad API?

- Ta snabbt bort kalkylblad från kalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du kalkylbladet Ta bort från kalkylblad API med SDK:er

### Ta bort kalkylblad från kalkylblad API Specifikation

 De[Ta bort kalkylblad från kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/ManagementController/DeleteWorksheetFromSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan ta bort ett kalkylblad från kalkylbladet med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
