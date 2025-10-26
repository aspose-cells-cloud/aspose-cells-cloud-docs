---
title: Aspose.Cells Cloud Web API - Växla intervall i kalkylblad
second_title: Documen
ArticleTitle: Swap Range Data in a Spreadshee
linktitle: Byt rang
type: docs
url: /sv/swap-range/
keywords: Aspose.Cells Cloud Web API, Swap Ranges, Office Cloud, RES
description: Byt intervall för Excel API tillhandahåller ett kraftfullt verktyg för att byta ut två kolumner, rader, intervall eller enskilda celler i en Excel-fil. Denna API-fil låter användare effektivt ordna om sina tabeller, vilket säkerställer att den ursprungliga dataformateringen bevaras och att alla befintliga formler fortsätter att fungera korrekt. Genom att utnyttja denna API-fil kan användare effektivisera sina datahanteringsuppgifter och bibehålla integriteten i sina kalkylblad.
weight: 100
kwords: Excel, Office Moln, REST, PDF, CSV, Json, Markdown
---
Utbyta data mellan två valfria kolumner, rader, områden eller enskilda celler i en Excel-fil.

## **Växlingsintervall API**

```http
PUT http://api.aspose.cloud/v4.0/cells/swap/range
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen.|
|arbetsblad1|Sträng|Fråga|Ange det kalkylblad som är källan för utbytesdataområdet.|
|intervall1|Sträng|Fråga|Ange källan för utbytesdata.|
|arbetsblad2|Sträng|Fråga|Ange det kalkylblad som är målet för utbytesdataområdet.|
|intervall2|Sträng|Fråga|Ange målet för utbytesdata.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Lagringsnamn för utdatafil.|
|område|Sträng|Fråga|Inställningen för kalkylbladets region.|
|lösenord|Sträng|Fråga|Lösenordet för att öppna kalkylbladsfilen.|

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

## Var ska vi använda Swap Range API?

När du behöver byta intervalldata i ett kalkylblad kan du använda API.

## Varför ska du använda Swap Range API?

- Växla snabbt intervalldata i ett Excel-kalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du swap-intervallet API med SDK:er

### Specifikation för bytesområde API

 De[Specifikation för bytesområde API](https://reference.aspose.cloud/cells/#/TransformController/SwapRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan byta intervall med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{< /tab >}}
{{< /tabs >}}
