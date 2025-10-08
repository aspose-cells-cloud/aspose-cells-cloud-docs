---
title: Aspose.Cells Cloud Web API - Addera, minus, multiplicera, dividera och procent i ett kalkylblad/Excel-intervall
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Matematikberäkning
type: docs
url: /sv/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: Omfattande guide för att använda Math Calculate API för att utföra beräkningar i Excel-kalkylblad
weight: 100
kwords: Matematisk beräkning, Cloud REST API, Addera, Minus, Multiplicera, Dividera, Procent, Office Cloud, Aspose.Cells
---
Utvecklare kan använda denna API för att utföra addition, subtraktion, multiplikation, division och procentuell beräkning på angivna områden av kalkylblad/Excel.

|**Beräkna operationen** | Beskrivning|
|:- |:- |
|**Tillägga** |+ |
|**Minus** |-  |
|**Multiplicera** |*  |
|**Dela** |/ |
|**Procentsats** |% |

## **Matematik Beräkna API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen för bearbetning.|
| drift| Sträng| Fråga| Den matematiska operationen som ska utföras (addera, minus, multiplicera, dividera och procent).|
| värde| Sträng| Fråga| Ett värde som ska användas i beräkningen, om tillämpligt.|
| arbetsblad| Sträng| Fråga| Namnet på kalkylbladet som ska bearbetas.|
| räckvidd| Sträng| Fråga| Cellintervallet som ska inkluderas i beräkningen.|
| område| Sträng| Fråga|Definierar den specifika regionen i kalkylarket.|
| lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen, om den är skyddad.|

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

## Var ska vi använda matematikfunktionen Beräkna API?

Matematisk beräkning API är lämplig för batchberäkningar i kalkylblad.

## Varför ska du använda matematikberäkningen API?

- Utför batchmatteberäkningar.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur man använder matematiken Beräkna API med SDK:er

### Matematik Beräkna API Specifikation

 De[Matematik Beräkna Specifikation](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör det möjligt för utvecklare att interagera med API direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan göra matematiska beräkningar cell för cell med bara en kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
