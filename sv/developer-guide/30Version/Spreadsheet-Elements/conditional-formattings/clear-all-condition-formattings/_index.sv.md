---
title: "Rensa villkorsformatering"
type: docs
url: /conditional-formattings/clear/
aliases: [/clear-all-condition-formattings/]
keywords: "Aspose.Cells Cloud, REST API, rensa villkorsformatering, Excel, kalkylblad, JWT, v3.2"
description: "Ta bort alla regler för villkorsformatering från ett kalkylblad med Aspose.Cells Cloud API (v3.2). Lär dig begärsyntaxen, nödvändiga parametrar, autentiseringssteg och se exempelkod i flera SDK:er."
weight: 80
---

Denna REST API rensar alla regler för villkorsformatering från ett kalkylblad.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.2/cells/{name}/worksheets/{sheetName}/conditionalFormattings
```

### Begärparametrar

| Parameternamn   | Typ    | Plats  | Beskrivning                                                           |
| --------------- | ------ | ------ | --------------------------------------------------------------------- |
| **name**        | string | path   | Namnet på arbetsboksfilen (t.ex. `Book1.xlsx`).                      |
| **sheetName**   | string | path   | Namnet på kalkylbladet från vilket villkorsformatering ska tas bort. |
| **folder**      | string | query  | _(Valfritt)_ Mappväg i lagringen där arbetsboken finns.              |
| **storageName** | string | query  | _(Valfritt)_ Namn på lagringstjänsten.                               |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormattings) definierar ett offentligt tillgängligt programmeringsgränssnitt, och **OpenAPI-specifikationen** gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.2/cells/Book1.xlsx/worksheets/sheet1/conditionalFormattings" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

### Fel-svar

| HTTP-kod | Anledning                                              | Exempel på responsbody                                         |
| -------- | ------------------------------------------------------ | ------------------------------------------------------------- |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Ogiltigt parametervärde." }`      |
| **401**  | Auktorisering misslyckades – saknat eller ogiltigt JWT-token. | `{ "Code":"401", "Message":"Åtkomsttoken saknas eller är ogiltig." }` |
| **404**  | Ej hittad – arbetsbok eller kalkylblad finns inte.    | `{ "Code":"404", "Message":"Filen hittades inte." }`          |
| **500**  | Internt serverfel – oväntat serverfel.                 | `{ "Code":"500", "Message":"Ett oväntat fel inträffade." }`   |

## SDK-exempel

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ConditionalFormatting-ClearConditionFormattings-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-clear-all-formatting.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-ConditionalFormatting-delete_worksheet_conditional_formattings-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-ConditionalFormatting-ClearConditionFormattings-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ConditionalFormatting-ClearConditionFormattings-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "63fda1be9e5149f83edca47ce58dac87" >}}

{{< /tab >}}

{{< /tabs >}}