---
title: "Lägg till formatvillkor"
type: docs
url: /sv/conditional-formattings/add-format-condition/
aliases: [  /sv/add-a-format-condition/ ]
keywords: "Aspose.Cells Cloud, API för villkorlig formatering, Lägg till formatvillkor, Excel REST API, Cells API"
description: "Lär dig hur du lägger till ett formatvillkor i ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Innehåller begärsyntax, parametrar, säkert cURL-exempel och SDK-utdrag."
ArticleTitle: "Lägg till formatvillkor – Aspose.Cells Cloud API-dokumentation"
weight: 50
---

Denna REST API lägger till ett formatvillkor i ett kalkylark.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Begärparametrar

| Parameternamn | Typ    | Plats | Beskrivning                                                                 |
| ------------- | ------ | ----- | --------------------------------------------------------------------------- |
| name          | string | path  | Namnet på Excel-arbetsboken.                                                |
| sheetName     | string | path  | Namnet på kalkylarket som innehåller det intervall som ska formateras.     |
| index         | integer | path | Det nollbaserade indexet för det formatvillkor som ska läggas till eller ersättas. |
| cellArea      | string | query | Cellintervallet (t.ex. `A1:C3`) till vilket villkoret gäller.              |
| type          | string | query | Typen av villkor (t.ex. `Expression`, `CellValue`).                        |
| operatorType  | string | query | Operatorn för villkoret (t.ex. `Between`, `Equal`).                        |
| formula1      | string | query | Den första formeln eller värdet som används av villkoret.                  |
| formula2      | string | query | Den andra formeln eller värdet (krävs för vissa operatorer som `Between`). |
| folder        | string | query | Mappen i lagringen där arbetsboken finns.                                  |
| storageName   | string | query | Namnet på lagringstjänsten (t.ex. `Default`).                              |

### Felresponser

| HTTP-kod | Anledning                                           | Exempel på responsbody                                         |
| -------- | --------------------------------------------------- | ------------------------------------------------------------ |
| **400**  | Bad Request – saknade eller ogiltiga parametrar.   | `{ "Code":"400", "Message":"Invalid parameter value." }`     |
| **401**  | Unauthorized – saknad eller ogiltig JWT-token.     | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Not Found – arbetsboken eller kalkylarket finns inte. | `{ "Code":"404", "Message":"File not found." }`             |
| **500**  | Internal Server Error – oväntat serverfel.         | `{ "Code":"500", "Message":"An unexpected error occurred." }` |

### Lyckad respons

| HTTP-kod | Anledning                                     | Exempel på responsbody                  |
| -------- | --------------------------------------------- | ---------------------------------------- |
| **200**  | OK – villkoret har lagts till eller uppdaterats. | `{ "Code": "200", "Status": "OK" }`    |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/PutWorksheetFormatCondition) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda **cURL** för att anropa Aspose.Cells API:et. Exemplet nedan visar en komplett begäran, inklusive en tom JSON-kropp.

### cURL-exempel

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings/0?cellArea=A1:C3&type=Expression&operatorType=Between&formula1=v1&formula2=v2" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Moln SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-förvaret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-AddFormatCondition-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-add-cells-area-for-format-condition.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-put_worksheet_format_condition-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-AddFormatCondition-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-AddFormatCondition-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "caa13d019b3c7c3b5c14110ccd217e99" >}}

{{< /tab >}}

{{< /tabs >}}
---