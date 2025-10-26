---
title: Aspose.Cells Cloud WEb API - Dela upp kalkylarket i separata filer
second_title: Documen
ArticleTitle: Split the Spreadsheet into separate files
linktitle: Dela kalkylblad
type: docs
url: /sv/split-spreadsheet/
keywords: Excel API, Split Spreadsheet, Spreadsheet Management, Cloud Processing, File Formats, REST API, XLSX, CSV, PDF, JSON, Markdow
description: Dela upp ett lokalt kalkylblad i flera filer i olika format utan att kräva molnlagring
weight: 100
kwords: Excel API, Office Moln, REST API, Kalkylblad, PDF, CSV, JSON, Markdown, Dela lokalt kalkylblad, Molnbehandling, Filhantering, Felhantering
---
Dela upp det lokala kalkylbladet i separata filer med 30 utdatafilformat utan att kräva molnlagring.

## **Dela kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen som ska delas.|
| från| Heltal| Fråga| Ange det inledande kalkylbladets index.|
| till| Heltal| Fråga| Ange det avslutande kalkylbladets index.|
| utformat| Sträng| Fråga| Definiera utdatafilformatet.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen för att lagra utdataarbetsboken. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Definiera namnet på utdatafilens lagringsplats.|
| teckensnittPlats| Sträng| Fråga| Ange anpassade teckensnitt om det behövs.|
| återgå| Sträng| Fråga| Ange kalkylbladsregionen.|
| lösenord| Sträng| Fråga| Ange lösenordet för att komma åt kalkylbladsfilen.|

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

## Var ska vi använda det delade kalkylarket API?

När du behöver dela upp ett kalkylblad till fler filer kan du använda API.

## Varför ska du använda Split Spreadsheet API?

- Inget behov av molnlagringsutrymme, bara dela direkt.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Så här använder du det delade kalkylarket API med SDK:er

### Specifikation för delat kalkylblad API

 De[Specifikation för delat kalkylblad API](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan dela upp kalkylblad i separata filer med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
