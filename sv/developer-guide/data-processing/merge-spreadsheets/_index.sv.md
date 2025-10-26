---
title: Aspose.Cells Cloud Web API - Sammanfoga flera kalkylblad till ett enda kalkylblad
second_title: Documen
ArticleTitle: Merge multiple Spreadsheets into a single spreadsheet
linktitle: Sammanfoga kalkylblad
type: docs
url: /sv/merge-spreadsheets/
keywords: Merge spreadsheets, data merging, file format conversion, REST, XLSX, CSV, PD
description: Sammanfoga enkelt lokala kalkylbladsfiler till olika format (XLSX, CSV, PDF) med hjälp av Excel API
weight: 100
kwords: Excel API, Sammanfoga kalkylblad, Office Moln, REST API, Sammanfoga kalkylblad, CSV-format, JSON, Markdow
---
Sammanfoga flera lokala kalkylbladsfiler till en enda fil, samtidigt som du stöder utdata i över 30 filformat.

## **Sammanfoga kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/spreadsheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| utformat| Sträng| Fråga| Ange utdatafilformatet.|
| sammanfogaIEttSheet| Booleansk| Fråga| Ange om all data ska kombineras till ett enda kalkylblad.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen för utdataarbetsboken. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Ange namnet på utdatafilens lagringsplats.|
| teckensnittPlats| Sträng| Fråga| Definiera anpassade teckensnitt som ska användas.|
| område| Sträng| Fråga| Ange kalkylbladsregionen.|
| lösenord| Sträng| Fråga| Ange lösenordet för att öppna kalkylbladsfilen.|

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

## Var ska vi använda det sammanfogade lokala kalkylbladet API?

När du behöver sammanfoga flera datafiler kan du använda API.

## Varför ska du använda kalkylbladet Sammanfoga lokalt API?

- Inget behov av molnlagringsutrymme, bara sammanfoga direkt.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du kalkylarket "Merge Local" API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheets)tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som gör det möjligt för användare att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan sammanfoga flera kalkylblad till ett kalkylblad med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheets.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheets.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheets.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheets.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheets.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheets.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheets.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheets.go" >}}
{{< /tab >}}
{{< /tabs >}}
