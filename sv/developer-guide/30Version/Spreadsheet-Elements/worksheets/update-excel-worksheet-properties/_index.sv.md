---
title: "Uppdatera kalkylbladsegenskaper – Aspose.Cells Cloud API-referens (v3.0)"
second_title: "Dokument"
linktitle: "Uppdatera"
type: docs
url: /sv/worksheets/update-properties/
aliases: [  /sv/update-excel-worksheet-properties/ ]
weight: 20
keywords:
  [
    "Aspose.Cells",
    "Excel",
    "kalkylblad",
    "uppdatera egenskaper",
    "REST API",
    "moln",
    "v3.0",
  ]
description: "Lär dig hur du uppdaterar grundläggande egenskaper (t.ex. visning av nollor, linjalens synlighet) för ett Excel-kalkylblad med Aspose.Cells Cloud REST API v3.0. Innehåller cURL-begäran, SDK-exempel, parametrar och felhantering."
ArticleTitle: "Uppdatera kalkylbladsegenskaper – Aspose.Cells Cloud API-referens (v3.0)"
---

Denna REST API uppdaterar kalkylbladets grundläggande egenskaper.

## REST API

**Förutsättningar:** Du måste ha ett giltigt Aspose Cloud-konto, skaffa ett JWT-åtkomsttoken och säkerställa att målarboksposten finns lagrad på en stödd lagringsplats. Alla förfrågningar ska göras via **HTTPS**.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Begäranparametrar**

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                          |
| ------------- | ----- | --------------------------- | ---------------------------------------------------------------------------------------------------- |
| name          | string | path                        | Arbetsbokens filnamn (inklusive tillägg).                                                           |
| sheetName     | string | path                        | Namnet på det kalkylblad som ska uppdateras.                                                        |
| sheet         | object | body                        | JSON-objekt som innehåller nyckel/värde-par för kalkylbladsegenskaper (t.ex. `DisplayZeros`, `IsRulerVisible`). |
| folder        | string | query                       | Sökväg till mappen i lagringen där arbetsboken finns.                                               |
| storageName   | string | query                       | Namnet på den lagring som ska användas.                                                             |

Objektet **sheet** skickas i begärandetexten som JSON. Exempel på egenskaper som kan ändras är `DisplayZeros`, `IsRulerVisible`, `IsGridlinesVisible` och andra som definieras i API-specifikationen.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostUpdateWorksheetProperty) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL från kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1" \
-X POST \
-d '{"DisplayZeros":"true","IsRulerVisible":"true"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

Typiska svarskoder:

- **200** – Lyckades. Kalkylbladsegenskaperna uppdaterades.
- **400** – Ogiltig begäran (t.ex. felaktigt formaterad JSON eller saknad obligatorisk parameter).
- **401** – Otillåten åtkomst – saknad eller ogiltig JWT-token.
- **404** – Arbetsbok eller kalkylblad hittades inte.
- **500** – Internt serverfel.

| Kod | Betydelse |
|-----|-----------|
| 200 | Lyckades – kalkylbladsegenskaperna uppdaterades. |
| 400 | Felaktig begäran – felaktigt formaterad JSON eller saknad obligatorisk parameter. |
| 401 | Otillåten åtkomst – saknad eller ogiltig JWT-token. |
| 404 | Hittades inte – arbetsbok eller kalkylblad finns inte. |
| 500 | Internt serverfel. |

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostUpdateWorksheetProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostUpdateWorksheetProperty-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-update_worksheet_property-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-UpdateWorksheetProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-UpdateWorksheetProperties-update-worksheet-properties.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-UpdateWorksheetProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "ce38cb4feb118132fada7801c7f5cd43" >}}

{{< /tab >}}

{{< /tabs >}}