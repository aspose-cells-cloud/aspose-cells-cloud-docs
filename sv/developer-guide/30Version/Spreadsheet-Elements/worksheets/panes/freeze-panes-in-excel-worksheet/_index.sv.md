---
title: "Frys rutor i ett Excel-ark"
second_title: "Dokument"
linktype: "Frys"
type: docs
url: /worksheets/panes/freeze/
aliases: [/frys-rutor-i-excel-ark/, /worksheets/freeze-panes/]
keywords: "Aspose.Cells Cloud, Frys rutor, Excel, REST API, Ark"
description: "Lär dig hur du fryser rader och kolumner i ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar slutpunktsyntax, nödvändiga parametrar, ett cURL-exempel, autentisieringsvägledning, detaljerad felhantering samt SDK-kodexempel för flera programmeringsspråk."
weight: 190
---

Denna REST API **ställer in** frysning av rutor i ett Excel-ark.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/freezepanes
```

Följande begärparametrar används:

| Parameter_name | Typ     | Plats  | Beskrivning                                           |
| -------------- | ------- | ------ | ----------------------------------------------------- |
| name           | string  | path   | Namnet på arbetsboksfilen.                            |
| sheetName      | string  | path   | Namnet på arket där rutor ska fryses.                 |
| row            | integer | query  | Nollbaserat index för den första **icke-frysna** raden. |
| column         | integer | query  | Nollbaserat index för den första **icke-frysna** kolumnen. |
| frozenRows     | integer | query  | Antal rader att frysa från toppen.                    |
| frozenColumns  | integer | query  | Antal kolumner att frysa från vänster.                |
| folder         | string  | query  | Mappväg i lagringen där arbetsboken finns.            |
| storageName    | string  | query  | Namn på lagringstjänsten.                             |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PutWorksheetFreezePanes) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/freezepanes?row=1&column=1&frozenRows=1&frozenColumns=1" \
-X PUT \
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

### Felrespons

| HTTP-status               | Kod | Meddelande                       | Exempel                                                   |
| ------------------------- | --- | -------------------------------- | --------------------------------------------------------- |
| 400 Bad Request           | 400 | Ogiltiga parametrar              | `{ "Code": 400, "Message": "Ogiltigt värde för frozenRows" }` |
| 401 Unauthorized          | 401 | Saknas eller ogiltig JWT-token   | `{ "Code": 401, "Message": "Ogiltig åtkomsttoken" }`      |
| 404 Not Found             | 404 | Arbetsbok eller ark hittades inte | `{ "Code": 404, "Message": "Filen hittades inte" }`       |
| 500 Internal Server Error | 500 | Oväntat serverfel                | `{ "Code": 500, "Message": "Internt serverfel" }`         |

## SDK-familj för molnet

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:n:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Objective C" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPutWorksheetFreezePanes.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutWorksheetFreezePanes-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-set_freeze_panes-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-FreezePanes-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-FreezePanes-freeze-panes.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-FreezePanes-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "099a22da7db4d5602c0da3b90bc1dc30" >}}

{{< /tab >}}

{{< /tabs >}}

---