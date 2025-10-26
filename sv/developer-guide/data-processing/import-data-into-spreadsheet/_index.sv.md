---
title: Aspose.Cells Cloud Web API - Importera CSV-, JSON- eller XML-data till en kalkylbladsfil
second_title: Documen
ArticleTitle: Import Csv, JSON, or XML Data into a Spreadsheet file
linktitle: Importera data till kalkylblad
type: docs
url: /sv/import-data-into-spreadsheet/
keywords: Import data, Aspose.Cells Cloud Web API, spreadsheet integration, CSV, JSON, XML, data handling, Aspose.Cell
description: Importera effektivt data till ett kalkylblad från format som stöds, som CSV, JSON och XML, med hjälp av Aspose.Cells Cloud Web API
weight: 100
kwords: Aspose.Cells Molnwebb API, Importera data, Office Moln, REST, Kalkylblad, CSV, JSON, XM
---
 Importera data till ett kalkylblad. Det format som stöds för den importerade datafilen är[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) eller[CSV-fil](https://docs.fileformat.com/spreadsheet/csv/).

## **Importera data till kalkylblad API**

```http
PUT http://api.aspose.cloud/v4.0/cells/import/data
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| datafil| Fil| FormulärData| Ladda upp datafilen som ska importeras.|
| Kalkylblad| Fil| FormulärData| Ladda upp målkalkylbladsfilen.|
| arbetsblad| Sträng| Fråga| Ange kalkylbladet för import av data.|
| startcell| Sträng| Fråga|Ange startpositionen för import av data.|
| infoga| Booleansk| Fråga| Anger om den angivna importdatan ska infogas eller skrivas över.|
| konverteraNumeriskData| Booleansk| Fråga| Ange om numeriska data ska konverteras under importen.|
| delare| Sträng| Fråga| Ange avgränsare för CSV-format.|
| utväg| Sträng| Fråga| (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.|
|outStorageName| Sträng| Fråga| Ange namnet på utdatafilens lagringsplats.|
| teckensnittPlats| Sträng| Fråga| Definiera anpassade teckensnitt som ska användas.|
| återgå| Sträng| Fråga| Ställ in konfigurationen för kalkylbladsregionen.|
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

## Var ska vi använda importdata till kalkylblad API?

- Importera stora mängder data till ett kalkylblad.
-  Det importerade datafilformatet är[XML](https://docs.fileformat.com/web/xml/), [JSON](https://docs.fileformat.com/web/json/) och[CSV-fil](https://docs.fileformat.com/spreadsheet/csv/).

## Varför ska du använda Importera data till kalkylblad API?

- Importera stora mängder data till kalkylblad.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur man använder importdata till kalkylblad API med SDK:er

### Importera data till kalkylblad API Specifikation

 De[Importera data till kalkylblad API Specifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/ImportDataIntoSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från din webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå, vilket gör att du kan importera data till ett kalkylblad med kort kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ImportDataIntoSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ImportDataIntoSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ImportDataIntoSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ImportDataIntoSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ImportDataIntoSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ImportDataIntoSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ImportDataIntoSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ImportDataIntoSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
