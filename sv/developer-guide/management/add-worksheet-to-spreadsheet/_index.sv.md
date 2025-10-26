---
title: Aspose.Cells Cloud Webb API - Lägg till ett kalkylblad i ett kalkylblad
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: Lägg till kalkylblad i kalkylblad
type: docs
url: /sv/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: Med Cloud Web API kan utvecklare effektivt lägga till nya kalkylblad i en arbetsbok, vilket ger kontroll över kalkylbladets typ, position och namn. Denna funktion förbättrar hanteringen och flexibiliteten i arbetsböcker.
weight: 100
kwords: Excel, Office Moln, REST, Kalkylblad, PDF, CSV, JSON, Markdown, Hantera Excel Arbetsblad, Skapande av dynamiska kalkylblad
---
Lägga till ett kalkylblad i kalkylbladet och ange typ och plats för kalkylbladet.

|**Arbetsbladstyp** | Beskrivning|
|:- |:- |
|**VB** | Visual Basic-modulen|
|**Arbetsblad** | Arbetsblad|
|**Diagram** | Diagramblad|
|**BIFF4Makro** | BIFF4 Makroark|
|**InternationellMakro** | Internationellt makroark|
|**Andra** | Internationellt makroark|
|**Dialog** | Dialogarbetsblad|

## **Lägg till arbetsblad i kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen.|
|arktyp|Sträng|Fråga|Anger namnet på det nya kalkylbladet. Om inget namn anges kommer ett standardnamn att tilldelas.|
|placera|Heltal|Fråga|Anger positionen där det nya kalkylbladet ska infogas. Om inget anges läggs kalkylbladet till i slutet av arbetsboken.|
|arknamn|Sträng|Fråga|Anger vilken typ av kalkylblad som ska läggas till. Om inget anges används en standardkalkylbladstyp.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Namn på utdatafilens lagringsplats.|
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

## Var ska vi använda Lägg till kalkylblad till kalkylblad API?

När du behöver lägga till ett kalkylblad för ett kalkylblad kan du använda API.

## Varför ska du använda Lägg till kalkylblad i kalkylblad API?

- Lägg till ett kalkylblad i kalkylbladet och ange kalkylbladets typ och plats.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Lägg till kalkylblad i kalkylblad API med SDK:er

### Lägg till kalkylblad i kalkylblad API Specifikation

 De[Lägg till kalkylblad i kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan lägga till ett kalkylblad i ett kalkylblad med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör API-anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
