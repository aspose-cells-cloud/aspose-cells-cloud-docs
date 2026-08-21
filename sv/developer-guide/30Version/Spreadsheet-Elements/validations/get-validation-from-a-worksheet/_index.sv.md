---
title: "Hämta ett kalkylbladsvalidering med index från ett Excel-kalkylblad"
second_title: "Document"
linktype: "Hämta"
type: docs
url: /sv/validations/get/
aliases: [  /sv/get-validation-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, API för kalkylbladsvalidering, hämta validering med index, Excel REST API, Aspose.Cells SDK"
description: "Hämta ett kalkylbladsvalidering med sitt nollbaserade index från en Excel-arbetsbok med Aspose.Cells Cloud API (v3.0). Inkluderar cURL-exempel, svarsschema, felkoder och SDK-utdrag för C#, Java, Python och mer."
weight: 10
---

Denna REST API hämtar ett kalkylbladsvalidering med dess index från ett Excel-kalkylblad.  
Innan du anropar slutpunkten, skaffa ett JWT-token via slutpunkten `/connect/token` och inkludera det i `Authorization`-headern som `Bearer <jwt token>`.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/validations/{validationIndex}
```

### **Begärparametrar**

| Parameternamn   | Typ     | Plats  | Beskrivning                                           |
| --------------- | ------- | ------ | ----------------------------------------------------- |
| name            | string  | path   | Namnet på arbetsboksfilen.                            |
| sheetName       | string  | path   | Namnet på kalkylbladet.                               |
| validationIndex | integer | path   | Nollbaserat index för valideringen som ska hämtas.    |
| folder          | string  | query  | Mappen som innehåller arbetsboken.                    |
| storageName     | string  | query  | Namn på lagringstjänsten.                             |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/WorksheetValidations/GetWorksheetValidation) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/validations/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Validation": {
    "AlertStyle": "Stop",
    "AreaList": [
      {
        "EndColumn": 0,
        "EndRow": 0,
        "StartColumn": 0,
        "StartRow": 0
      },
      {
        "EndColumn": 27,
        "EndRow": 0,
        "StartColumn": 26,
        "StartRow": 0
      }
    ],
    "IgnoreBlank": false,
    "InCellDropDown": false,
    "Operator": "None",
    "ShowError": false,
    "ShowInput": false,
    "Type": "AnyValue",
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkBook.xlsx/worksheets/Sheet1/Validations/0",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Svarsschema**

| Fält           | Typ     | Beskrivning                                                              |
| -------------- | ------- | ------------------------------------------------------------------------ |
| AlertStyle     | string  | Stilen på den varning som visas till användaren (Stop, Warning, Information). |
| AreaList       | array   | Samling av cellintervall som valideringen gäller för.                   |
| IgnoreBlank    | boolean | Om `true`, ignoreras tomma celler vid validering.                        |
| InCellDropDown | boolean | Om `true`, visas en rullgardinslista i cellen.                          |
| Operator       | string  | Jämförelseoperator som används för valideringen (t.ex. `None`, `Between`). |
| ShowError      | boolean | Bestämmer om ett felmeddelande visas när valideringen misslyckas.       |
| ShowInput      | boolean | Bestämmer om ett inmatningsmeddelande visas när cellen väljs.           |
| Type           | string  | Typ av validering (t.ex. `AnyValue`, `WholeNumber`, `Decimal`, etc.).   |
| link.Href      | string  | Självreferens-URL till valideringsresursen.                              |
| link.Rel       | string  | Relations typ (alltid `self`).                                           |

**Möjliga felkoder**

| HTTP-status | Betydelse                                                              |
| ----------- | ---------------------------------------------------------------------- |
| 200         | Validering hämtades framgångsrikt.                                    |
| 400         | Felaktig begäran – saknade eller ogiltiga parametrar.                 |
| 401         | Otillåten åtkomst – ogiltigt eller saknat JWT-token.                  |
| 404         | Hittades inte – arbetsboken, kalkylbladet eller valideringsindexet finns inte. |
| 500         | Internt serverfel – oväntat tillstånd.                                 |

## Molnsdk-familj

Att använda en SDK är det snabbaste sättet att utveckla mot Aspose.Cells Cloud. En SDK abstraher bort detaljer på lägre nivå så att du kan fokusera på din affärslogik. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetValidation.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetValidation.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetValidation.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetValidation.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetValidation.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetValidation.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetValidation.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetValidation.go" >}}

{{< /tab >}}

{{< /tabs >}}