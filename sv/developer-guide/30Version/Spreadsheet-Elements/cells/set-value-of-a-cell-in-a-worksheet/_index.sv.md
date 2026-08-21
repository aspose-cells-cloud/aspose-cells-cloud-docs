---
title: "Ställ in cellvärde – Aspose.Cells Cloud API-referens (v3.0)"  
type: docs  
url: /sv/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "Aspose Cells API ställ in cellvärde, Excel-celluppdatering REST, Aspose.Cells Cloud cURL-exempel"  
description: "Lär dig hur du ställer in värdet för en specifik cell i ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Innehåller begäransyntax, parametrar, HTTPS-cURL-exempel och SDK-kodexempel."  
---  

Detta REST API ställer in **cellvärdet** i en Excel-fil.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Begärparametrar**

| Namn          | Typ    | Plats  | Beskrivning                                       |
|---------------|--------|--------|---------------------------------------------------|
| name          | string | path   | Namn på Excel-dokumentet (inklusive tillägg).    |
| sheetName     | string | path   | Namn på arbetsbladet (skiftlägeskänsligt).        |
| cellName      | string | path   | A1-stilad adress för målcellen (t.ex. `A1`).     |
| value         | string | query  | Värde som ska tilldelas cellen.                   |
| type          | string | query  | Datatyp för värdet (`int`, `string`, `float`, etc.). |
| formula       | string | query  | Formel som ska tillämpas på cellen (valfritt).    |
| folder        | string | query  | Mapp som innehåller dokumentet (valfritt).        |
| storageName   | string | query  | Namn på lagringsutrymmet där filen finns (valfritt). |

## **Svar**

Returnerar CellResponse.

- **Översikt över svarsfält**

| Fält            | Typ     | Beskrivning                                             |
| --------------- | ------- | ------------------------------------------------------- |
| `Name`          | string  | Cellens adress (t.ex. `F341`).                          |
| `Row`           | integer | Radindex (0-baserat).                                   |
| `Column`        | integer | Kolumnindex (0-baserat).                                |
| `Value`         | string  | Cellens visade värde.                                   |
| `Type`          | string  | Cellens datatyp (t.ex. `IsString`).                     |
| `Formula`       | string  | Formeltext om cellen innehåller en formel.             |
| `IsFormula`     | bool    | Indikerar om cellen innehåller en formel.              |
| `IsMerged`      | bool    | Indikerar om cellen är en del av ett sammanfogat område. |
| `IsArrayHeader` | bool    | Indikerar om cellen är en arrayhuvudrad.               |
| `IsInArray`     | bool    | Indikerar om cellen tillhör en array.                  |
| `IsErrorValue`  | bool    | Indikerar om cellen innehåller ett felvärde.           |
| `IsInTable`     | bool    | Indikerar om cellen finns i en tabell.                 |
| `IsStyleSet`    | bool    | Indikerar om en stil tillämpas på cellen.              |
| `HtmlString`    | string  | HTML-kodad representation av cellens värde.            |
| `Style.link`    | object  | Länk till stilresursen.                                 |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltig eller saknad JWT-token.                    |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.  |
| 500 | Internt serverfel           | Oväntat serverfel.                                 |

## Hur du använder PostWorksheetCellSetValue API med SDK:er

### PostWorksheetCellSetValue API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att utvecklare kan anropa REST-slutpunkter direkt från en webbläsare eller valfri HTTP-klient.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells webbtjänster. Exemplet nedan visar hur du ställer in ett cellvärde med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json

{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK accelererar utvecklingen genom att hantera detaljer på låg nivå så att du kan fokusera på ditt projekt. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}