---
title: "Uppdatera ett listobjekt i ett Excel-ark"
ArticleTitle: "Uppdatera ett listobjekt i ett Excel-ark – Aspose.Cells Cloud API-dokumentation"
second_title: "Dokument"
linktitle: "Uppdatera"
type: docs
url: /list-objects/update/
aliases:
  - /update-a-list-object-or-table-inside-the-worksheet/
  - /tables/update/
keywords: "Aspose.Cells, ListObject, Uppdatera tabell, Excel-API, REST, molntjänst, uppdatera listobjekt, Excel-ark, tabell"
description: "Lär dig hur du uppdaterar en Excel-tabell med Aspose.Cells Cloud API (v3.0). Innehåller slutpunkt, parametrar, exempel med cURL, felkoder och SDK-exempel."
weight: 20
---

Denna REST API uppdaterar egenskaperna för ett **listobjekt** (tabell) i ett Excel-ark.

## Säkerhet och autentisering

Aspose.Cells Cloud API:n är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Schema för begäran för begäran (Request Body Schema)

DTO:t `listObject` innehåller följande fält. Endast de fält som du vill ändra behöver inkluderas i begäran.

| Fält                                            | Typ                | Obligatoriskt | Beskrivning                                                                |
| ----------------------------------------------- | ------------------ | ------------- | -------------------------------------------------------------------------- |
| **DisplayName**                                 | sträng             | valfritt      | Namnet som visas för tabellen.                                             |
| **StartRow** / **StartColumn**                  | heltal             | valfritt      | Nollbaserat index för första raden/kolumnen i tabellen.                   |
| **EndRow** / **EndColumn**                      | heltal             | valfritt      | Nollbaserat index för sista raden/kolumnen i tabellen.                    |
| **Range**                                       | sträng             | valfritt      | A1-stilens adress som definierar tabellintervallet (t.ex. `A1:D10`).      |
| **ShowHeaderRow**                               | boolesk värde      | valfritt      | `true` för att visa rubrikraden.                                          |
| **ShowTotals**                                  | boolesk värde      | valfritt      | `true` för att visa raden för totalberäkningar.                          |
| **TableStyleName**                              | sträng             | valfritt      | Namn på den inbyggda tabellstilen som ska tillämpas.                      |
| **TableStyleType**                              | sträng             | valfritt      | Stiltyp (`TableStyleLight`, `TableStyleMedium`, etc.).                    |
| **ListColumns**                                 | array av objekt    | valfritt      | Samling med kolumndefinitioner (`Name`, `TotalsCalculation`).             |
| **Sorter**, **AutoFilter**, **ShowTableStyle…** | objekt             | valfritt      | Avancerade stil- och filteralternativ (se fullständig DTO i OpenAPI-specifikationen). |

### Minimal exempelnyttolast (payload)

```json
{
  "DisplayName": "SalesData",
  "Range": "A1:E20",
  "ShowHeaderRow": true,
  "ShowTotals": false
}
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}
```

### **Begärningsparametrar**

| Parameternamn       | Typ    | Plats | Beskrivning                          |
| ------------------- | ------ | ----- | ------------------------------------ |
| **name**            | sträng | path  | Dokumentets namn.                    |
| **sheetName**       | sträng | path  | Arkets namn.                         |
| **listObjectIndex** | heltal | path  | Index för listobjektet som ska uppdateras. |
| **listObject**      | objekt | body  | ListObject DTO i begärandetexten.    |
| **folder**          | sträng | query | Mapp som innehåller dokumentet.      |
| **storageName**     | sträng | query | Namn på lagringsutrymmet.            |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObject) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Begäran

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet7/listobjects/0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
    "DisplayName": "SalesData",
    "Range": "A1:E20",
    "ShowHeaderRow": true,
    "ShowTotals": false,
    "ListColumns": [
      { "Name": "Product", "TotalsCalculation": "None" },
      { "Name": "Quantity", "TotalsCalculation": "Sum" },
      { "Name": "Price", "TotalsCalculation": "Average" }
    ]
  }'
```

{{< /tab >}}

### Svar

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Ett lyckat svar innehåller följande fält:

| Fält                    | Typ    | Beskrivning                                           |
| ----------------------- | ------ | ----------------------------------------------------- |
| Code                    | heltal | HTTP-statuskod (200 för lyckad begäran).              |
| Status                  | sträng | Textuell beskrivning av statusen.                     |
| UpdatedObject *(valfritt)* | objekt | Den uppdaterade `ListObject`-representationen, inklusive egenskaperna som ändrats. |

{{< /tab >}}

{{< /tabs >}}

## Felaktiga svar (Error Responses)

| HTTP-kod | Beskrivning                                                             | Exempel på nyttoinnehåll (payload)                    |
| -------- | ----------------------------------------------------------------------- | ----------------------------------------------------- |
| **400**  | Felaktig begäran – obligatoriska fält saknas eller ogiltig JSON.        | `{ "Code": 400, "Message": "Invalid request body." }`  |
| **401**  | Auktorisering misslyckades – JWT-token saknas eller är ogiltig.         | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404**  | Resursen hittades inte – angivet arbetsbok, ark eller listobjekt saknas. | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500**  | Internt serverfel – oväntat tillstånd på serversidan.                   | `{ "Code": 500, "Message": "Server error." }`          |

## Vanliga frågor (FAQ)

<details>  
<summary>Hur uppdaterar jag ett listobjekt med Aspose.Cells Cloud API?</summary>

Använd slutpunkten `POST /cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}`. Inkludera en JSON-begäran med de egenskaper du vill ändra (t.ex. `DisplayName`, `ShowHeaderRow`). Autentisera med en JWT-token i `Authorization`-headern.

</details>

<details>  
<summary>Vilket svar får jag efter en lyckad uppdatering?</summary>

Ett JSON-objekt med `Code: 200` och `Status: "OK"` returneras. Vid ett fel returneras motsvarande HTTP-statuskod och ett `Error`-objekt som beskriver problemet.

</details>

<details>  
<summary>Kan jag uppdatera en delmängd av listobjektets egenskaper?</summary>

Ja. Inkludera bara de fält du vill ändra i begärandetexten; alla uteslutna fält förblir oförändrade.

</details>

## Relaterad dokumentation

- [Lägg till ett listobjekt](https://docs.aspose.cloud/cells/list-objects/add/)
- [Hämta listobjekt](https://docs.aspose.cloud/cells/list-objects/get/)
- [Ta bort listobjekt](https://docs.aspose.cloud/cells/list-objects/delete/)

## Molntjänstfamilj för SDK

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PostWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}