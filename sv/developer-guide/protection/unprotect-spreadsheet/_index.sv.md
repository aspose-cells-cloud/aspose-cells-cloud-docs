---
title: Aspose.Cells Cloud Web API - Avskydda kalkylblad med lösenord
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: Avaktivera kalkylblad
type: docs
url: /sv/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Tar effektivt bort lösenordsskydd med dubbla lager från Excel-kalkylblad, och stöder både öppning och ändring av lösenord med avancerade krypteringstekniker.
weight: 100
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Matcha alla tomma celler i ett Excel-kalkylblad
---
Tillämpar avskydda Excel kalkylblad med lösenord, stöder både öppning och ändring av lösenord.

## **Avskydda kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
|Kalkylblad|Fil|FormulärData|Ladda upp kalkylbladsfilen så att den inte skyddas.|
|lösenord|Sträng|Fråga|Krypteringslösenordet för kalkylbladsfilen.|
|ändra lösenord|Sträng|Fråga|Lösenordet som krävs för att ändra den skyddade filen.|
|utväg|Sträng|Fråga|(Valfritt) Mappsökvägen där den oskyddade arbetsboken ska lagras. Standardvärdet är null.|
|outStorageName|Sträng|Fråga|Anger namnet på utdatafilens lagringsplats.|
|område|Sträng|Fråga|Definierar inställningarna för kalkylbladets region.|

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

## Var ska vi använda alternativet Ta bort tomma kolumner i kalkylblad API?

När du behöver transformera data kan du använda API.

## Varför ska du använda Ta bort tomma kolumner i kalkylblad API?

- Ta snabbt bort alla tomma kolumner som inte innehåller data eller andra objekt från ett Excel-kalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du Ta bort tomma kolumner i kalkylblad API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera borttagning av tomma kolumner i kalkylblad för celler med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
