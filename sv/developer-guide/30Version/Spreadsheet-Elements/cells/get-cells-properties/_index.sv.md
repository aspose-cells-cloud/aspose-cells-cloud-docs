---
title: "Hämta cellernas egenskaper"
type: docs
url: /sv/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, kalkylblad, cellegenskaper, hämta cellernas egenskaper"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att hämta egenskaper för en specifik cell eller fördefinierade cellmetoder i ett Excel-kalkylblad."
---

Denna REST API visar hur man hämtar en specifik cell i en Excel-fil.

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Begärandeparametrar


| Parametername        | Typ    | Plats  | Beskrivning                                                                                                                                                                           |
| -------------------- | ------ | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**             | sträng | path   | Namnet på Excel-dokumentet.                                                                                                                                                       |
| **sheetName**        | sträng | path   | Namnet på kalkylbladet som innehåller cellen.                                                                                                                                        |
| **cellOrMethodName** | sträng | path   | Cellens namn eller namnet på en fördefinierad metod (t.ex. `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**           | sträng | query  | Mappen där dokumentet lagras.                                                                                                                                              |
| **storageName**      | sträng | query  | Namnet på lagringstjänsten.                                                                                                                                                      |

## **Svar**

Returnerar CellResponse.

- **Översikt över svarsfält**

| Fält            | Typ     | Beskrivning                                           |
| --------------- | ------- | ----------------------------------------------------- |
| `Name`          | sträng  | Cellens adress (t.ex. `F341`).                   |
| `Row`           | heltal  | Radindex med nollbaserad indexering.                                 |
| `Column`        | heltal  | Kolumnindex med nollbaserad indexering.                              |
| `Value`         | sträng  | Den värde som visas i cellen.                           |
| `Type`          | sträng  | Celldatatyp (t.ex. `IsString`).             |
| `Formula`       | sträng  | Formeltext om cellen innehåller en formel.          |
| `IsFormula`     | bool    | Indikerar om cellen innehåller en formel.        |
| `IsMerged`      | bool    | Indikerar om cellen är en del av ett sammanfogat område. |
| `IsArrayHeader` | bool    | Indikerar om cellen är en arrayhuvudrad.        |
| `IsInArray`     | bool    | Indikerar om cellen tillhör en array.       |
| `IsErrorValue`  | bool    | Indikerar om cellen innehåller ett felvärde.   |
| `IsInTable`     | bool    | Indikerar om cellen finns i en tabell.         |
| `IsStyleSet`    | bool    | Indikerar om en stil tillämpas på cellen.     |
| `HtmlString`    | sträng  | HTML-kodad representation av cellens värde.      |
| `Style.link`    | objekt  | Hyperlänk till stilresursen.                      |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                     | Beskrivning                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Obehörig                | Ogiltig eller saknad JWT-token. |
| 413  | För stor nyttolast           | Den uppladdade filen överskrider storleksgränsen. |
| 500  | Internt serverfel       | Oväntat serverfel. |
## Hur du använder GetWorksheetCell API med SDK:er

### GetWorksheetCell API-specifikation


[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.
{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det mest effektiva sättet att snabba upp utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Hur man hämtar en specifik cell

- [Hämta celldata från ett kalkylblad](/sv/cells/get-cell-data-from-a-worksheet/)
- [Hämta första cellen från Excel-kalkylblad](/sv/cells/get-first-cell-from-excel-worksheet/)
- [Hämta sista cellen i Excel-kalkylblad](/sv/cells/get-last-cell-of-excel-worksheet/)
- [Hämta MaxRow från Excel-kalkylblad](/sv/cells/get-maxrow-from-excel-worksheet/)
- [Hämta MaxDataRow från Excel-kalkylblad](/sv/cells/get-maxdatarow-from-excel-worksheet/)
- [Hämta MaxColumn från Excel-kalkylblad](/sv/cells/get-maxcolumn-from-excel-worksheet/)
- [Hämta MaxDataColumn från Excel-kalkylblad](/sv/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Hämta MinRow från Excel-kalkylblad](/sv/cells/get-minrow-from-excel-worksheet/)
- [Hämta MinDataRow från Excel-kalkylblad](/sv/cells/get-mindatarow-from-excel-worksheet/)
- [Hämta MinColumn från Excel-kalkylblad](/sv/cells/get-mincolumn-from-excel-worksheet/)
- [Hämta MinDataColumn från Excel-kalkylblad](/sv/cells/get-mindatacolumn-from-excel-worksheet/)