---
title: "Lägg till hyperlänk till kalkylblad"
type: docs
url: /hyperlinks/add/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells, lägg till hyperlänk, Excel REST API, moln-SDK"
description: "Lär dig hur du lägger till en hyperlänk till ett Excel-kalkylblad med Aspose.Cells Cloud v3.0 REST API. Inkluderar slutpunkt, komplett parameterguide, cURL-exempel och SDK-fragment för C#, Java, Python och mer."
weight: 20
---

Denna REST API lägger till en hyperlänk till ett Excel-kalkylblad.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Begäranparametrar

| Parametername   | Typ    | Plats  | Beskrivning                                                                                   |
| --------------- | ------ | ------ | --------------------------------------------------------------------------------------------- |
| name            | string | path   | Dokumentets namn.                                                                             |
| sheetName       | string | path   | Kalkylbladets namn.                                                                           |
| firstRow        | integer | query | Nollbaserat index för den första raden i det intervall som hyperlänken ska tillämpas på.      |
| firstColumn     | integer | query | Nollbaserat index för den första kolumnen i det intervall som hyperlänken ska tillämpas på.   |
| totalRows       | integer | query | Antal rader som hyperlänkens intervall täcker.                                                |
| totalColumns    | integer | query | Antal kolumner som hyperlänkens intervall täcker.                                             |
| address         | string  | query | Mål-URL som hyperlänken pekar på (URL-kodad).                                                 |
| folder          | string  | query | Dokumentmappen.                                                                               |
| storageName     | string  | query | Lagringsnamn.                                                                                 |

Begäran kan också inkludera en JSON-kropp med samma fält (`Address`, `FirstRow`, `FirstColumn`, `TotalRows`, `TotalColumns`). Att ange en kropp är användbart när du föredrar en nyttolast framför frågesträngsparametrar.

### Felresponser

| HTTP-kod | Anledning                                              | Exempel på kropp                                                  |
| -------- | ------------------------------------------------------ | ----------------------------------------------------------------- |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }`          |
| **401**  | Auktorisering misslyckades – saknat eller ogiltigt JWT-token. | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Ej hittad – arbetsbok eller kalkylblad finns inte.    | `{ "Code":"404", "Message":"File not found." }`                   |
| **500**  | Internt serverfel – oväntat serverfel.                 | `{ "Code":"500", "Message":"An unexpected error occurred." }`     |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Hypelinks/PutWorksheetHyperlink) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks?firstRow=1&firstColumn=6&totalRows=1&totalColumns=1&address=https%3A%2F%2Fwww.msnbc.com%2F" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Om begäran misslyckas returnerar API:et standard-HTTP-felkoder (t.ex. 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Internal Server Error) tillsammans med en JSON-nyttolast som innehåller ett felmeddelande och kod.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetHyperlink.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetHyperlink.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetHyperlink.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetHyperlink.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetHyperlink.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetHyperlink.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetHyperlink.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetHyperlink.go" >}}

{{< /tab >}}

{{< /tabs >}}