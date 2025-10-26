---
title: Aspose.Cells Molnwebb API - Komprimera kalkylarkets storlek
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Komprimera kalkylblad
type: docs
url: /sv/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: Komprimera kalkylblad API låter användare effektivt minska filstorleken på kalkylblad genom att tillämpa angivna komprimeringsnivåer, optimera lagring och förbättra prestanda.
weight: 100
kwords: Excel, Office Moln, REST, Kalkylbladskomprimering, Filstorleksoptimering, PDF, CSV, Json, Markdow
---
Komprimera kalkylbladets storlek.

## **Komprimera kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen som ska komprimeras.|
|nivå|Heltal|Fråga|Anger den komprimeringsnivå som ska tillämpas, från 0 (ingen komprimering) till 9 (maximal komprimering).|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där den komprimerade arbetsboken ska lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namn på utdatafilens lagringsplats.|
|område|Sträng|Fråga|Inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet som krävs för att öppna kalkylbladsfilen.|

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

## Var ska vi använda det komprimerade kalkylbladet API?

När du behöver minska storleken på kalkylblad kan du använda API.

## Varför ska du använda det komprimerade kalkylbladet API?

- Kalkylarket är för stort och filstorleken behöver minskas.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du komprimeringsarket API med SDK:er

### Komprimera kalkylblad API Specifikation

 De[Komprimera kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) tillhandahåller ett offentligt tillgängligt gränssnitt för REST-interaktioner, vilket möjliggör direkta API-samtal från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan komprimera kalkylbladets storlek med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
