---
title: Aspose.Cells Cloud Web API - Summa, antal, medelvärde etc. efter färg i kalkylblad/Exce
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /sv/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Aspose.Cells Cloud Web API (Excel Cloud API) kan utföra databeräkningar, summering och medelvärdesberäkning, och kan även hitta maximi- och minimivärdena i ett Excel kalkylblad baserat på cellernas fyllnings- eller teckenfärg.
weight: 100
kwords: Summa, Antal, Medelvärde, Maxvärde, Minvärde, Excel REST API, Kalkylbladsoperationer, Aspose.Cells, Excel Moln API
---
API kan utföra databeräkningar, summering och medelvärdesberäkning, och kan även hitta max- och minimivärden i ett Excel-kalkylblad baserat på cellernas fyllnings- eller teckenfärg.

| Beräkna operationen| Beskrivning|
|:- |:- |
| Räkna| Bestäm antalet celler med samma färg.|
| Belopp| Beräkna det totala värdet av celler med samma färg.|
| Maxvärde| Identifiera det högsta värdet bland celler med samma färg.|
| Minvärde| Hitta det lägsta värdet bland celler med samma färg.|
|Genomsnittligt värde| Beräkna medelvärdet för celler med samma färg.|

## **Aggregerar Cells efter färg API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp| Beskrivning|
|:- |:- |:- |:- |
| Kalkylblad| Fil| FormulärData| Ladda upp kalkylbladsfilen.|
| Arbetsblad| Sträng| Fråga| Anger kalkylbladet.|
| Räckvidd| Sträng| Fråga| Anger intervallet.|
| Drift| Sträng| Fråga| Ange beräkningsmetoder, inklusive Summa, Antal, Medelvärde, Min och Max.|
| FärgPosition| Sträng| Fråga| Anger innehållet som ska summeras och räknas baserat på bakgrundsfärg och/eller teckenfärg.|
| Område| Sträng| Fråga| Inställningen för kalkylbladets region.|
| Lösenord| Sträng| Fråga| Lösenordet för att öppna kalkylbladsfilen.|

### **Svar**

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Felkoder

- **400 Felaktig begäran**Ogiltig Apose.Cells Cloud API URI.
- **401 Obehörig**Ogiltig åtkomsttoken. Eller ogiltigt klient-ID och hemlighet.
- **404 Hittades inte**Kalkylbladsfilen är inte tillgänglig.
- **500 Serverfel**Kalkylbladet har stött på ett fel vid hämtning av beräkningsdata.

## Var ska vi använda aggregerat efter färg API?

I ett kalkylblad visas data från olika kategorier i olika färger, vilket möjliggör operationer som summering, räkning, beräkning av medelvärden och att hitta maximi- och minimivärden baserat på färg.

## Varför ska du använda Aggregate by Color API?

- Tillhandahåll metoder för analys av färgdata.
- Klassificera och beräkna data baserat på färg för att tillhandahålla grundläggande data för dataanalys.
- Utvecklingen kan snabbt slutföras via det befintliga SDK:t.

## Hur man använder aggregatet efter färg API med SDK:er

### Aggregera efter färg API Specifikation

 De[Aggregera efter färg API Specifikation](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:t är det snabbaste sättet att utveckla, eftersom det abstraherar detaljer på låg nivå, vilket gör att du kan aggregera beräkningar efter cellfärg med bara en kort kodsnutt.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
