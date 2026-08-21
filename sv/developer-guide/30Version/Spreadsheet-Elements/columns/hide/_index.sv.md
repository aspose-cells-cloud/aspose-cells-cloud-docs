---
title: "Dölj kolumner i ett Excel-arbetsark"
second_title: "Dokument"
linktitle: "Dölj"
type: docs
url: /sv/columns/hide/
aliases:
  - /hide-columns-in-excel-worksheet/
  - /hide-columns-in-an-excel-worksheet/
keywords: "Aspose.Cells Cloud, API för att dölja kolumner, Excel-kolumndöljning, REST API för att dölja kolumner, Aspose.Cells SDK, kalkylarkautomation"
description: "Lär dig hur du döljer en eller flera kolumner i ett Excel-arbetsark med Aspose.Cells Cloud REST API (v3.0). Innehåller slutpunkt, parametrar, cURL-exempel, SDK-kodexempel och felhantering."
weight: 40
---

Denna REST API döljer kolumner i ett arbetsark.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/hide
```

### Begäranparametrar

| Parametername | Typ     | Plats  | Beskrivning                                                                 |
| ------------- | ------- | ------ | --------------------------------------------------------------------------- |
| name          | string  | path   | Namnet på arbetsboksfilen.                                                  |
| sheetName     | string  | path   | Namnet på arbetsarket där kolumner kommer att döljas.                      |
| startColumn   | integer | query  | Nollbaserat index för den första kolumnen som ska döljas.                  |
| totalColumns  | integer | query  | Antal på varandra följande kolumner som ska döljas, börjande från **startColumn**. |
| folder        | string  | query  | Sökvägen till mappen som innehåller arbetsboken.                           |
| storageName   | string  | query  | Namnet på lagringstjänsten där filen finns.                                |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetColumns) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att anropa Aspose.Cells-webbtjänster. Exempel nedan visar hur man döljer en kolumn med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/hide?startColumn=1&totalColumns=1" \
     -H "accept: application/json" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Möjliga svarskoder**

| HTTP-kod | Betydelse                              | Exempel JSON (fel)                                    |
| -------- | -------------------------------------- | ----------------------------------------------------- |
| 200      | Lyckades                               | `{ "Code": 200, "Status": "OK" }`                     |
| 400      | Felaktig begäran (t.ex. ogiltiga parametrar) | `{ "Code": 400, "Message": "Ogiltigt kolumnområde." }` |
| 401      | Otillåten (saknas/ogiltigt token)      | `{ "Code": 401, "Message": "Ogiltig åtkomsttoken." }` |
| 404      | Hittades inte (arbetsbok eller arbetsark) | `{ "Code": 404, "Message": "Filen hittades inte." }`   |
| 500      | Internt serverfel                      | `{ "Code": 500, "Message": "Oväntat fel." }`          |

{{< /tab >}}

{{< /tabs >}}

## familj av moln-SDK:er

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostHideWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostHideWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostHideWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostHideWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostHideWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostHideWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostHideWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostHideWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}