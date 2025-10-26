---
title: Aspose.Cells Cloud Web API - Ersätt kalkylbladsinnehåll
second_title: Documen
ArticleTitle: Replace Spreadsheet Conten
linktitle: Ersätt kalkylbladsinnehåll
type: docs
url: /sv/replace-spreadsheet-content/
keywords: Excel API, Spreadsheet manipulation, Replace text, Office Cloud integration, REST AP
description: Ersätt effektivt text i lokala kalkylbladsfiler med hjälp av Aspose.Cells API
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Ersätt text i Excel, Matcha tomma celler i Excel-arbetsbladet
---
Ersätt effektivt specificerad text i lokala kalkylarksfiler.

## **Ersätt kalkylbladsinnehåll API**

```
PUT http://api.aspose.cloud/v4.0/cells/replace/content
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| söktext| Sträng| Fråga|Texten att söka efter.|
| ersätt text| Sträng| Fråga| Texten som ska ersättas med.|
| arbetsblad| Sträng| Fråga| Ange kalkylbladet för ersättningen.|
| cellArea| Sträng| Fråga| Ange cellarean för ersättningen.|
| område| Sträng| Fråga| Inställningen för kalkylbladets region.|
| lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen.|

### **Svar**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Var ska vi använda Ersätt innehåll i kalkylblad API?

När du behöver ersätta innehåll i ett kalkylblad med ett lösenord kan du använda API.

## Varför ska du använda Ersätt innehåll i kalkylblad API?

- Ersätt snabbt innehåll i kalkylblad med lösenord.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Ersätt innehåll i kalkylblad API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceSpreadsheetContent) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera ersättning av innehåll i kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
