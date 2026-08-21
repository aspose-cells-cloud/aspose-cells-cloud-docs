---
title: "Sortera data i ett intervall på ett Excel-ark"
second_title: "Dokument"
linktitle: "Sortera"
type: docs
url: /sv/worksheets/sort-data/
aliases: [  /sv/sort-worksheet-data/ ]
keywords: "Aspose.Cells Cloud, Excel-sorterings-API, sortering av arkintervall, REST-API, dataSorter"
description: "Sortera ett specifikt intervall i ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, nödvändiga parametrar, autentiseringssteg, felhantering och SDK-exempel."
weight: 20
---

REST-API:et sortera data inom ett angivet intervall i ett Excel-ark.

## REST API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### Begärparametrar

| Parameternamn | Typ   | Plats  | Nödvändig | Beskrivning                                                       |
| ------------- | ----- | ------ | --------- | ----------------------------------------------------------------- |
| name          | string | path   | Ja        | Arbetsbokens namn.                                                |
| sheetName     | string | path   | Ja        | Arkets namn.                                                      |
| cellArea      | string | query  | Ja        | Det intervall som ska sorteras (t.ex. `A5:A10`).                 |
| dataSorter    | object | body   | Ja        | JSON-objekt som definierar sorteringsinställningarna (se schema nedan). |
| folder        | string | query  | Nej       | Mappen som innehåller arbetsboken.                               |
| storageName   | string | query  | Nej       | Namnet på den lagring där arbetsboken finns.                     |

**`dataSorter`-objektschema** – Brödtexten måste innehålla ett JSON-objekt med följande egenskaper:

- `CaseSensitive` _(boolean, nödvändig)_ – Bestämmer om sorteringen är skiftlägeskänslig.
- `HasHeaders` _(boolean, nödvändig)_ – Anger om intervallet innehåller en rubrikrad.
- `KeyList` _(array, nödvändig)_ – En samling sorteringsnycklar. Varje nyckelobjekt innehåller:
  - `Key` _(integer)_ – Nollbaserat kolumnindex.
  - `SortOrder` _(string)_ – `"ascending"` eller `"descending"`.
- `SortLeftToRight` _(boolean, nödvändig)_ – Om `true` sker sorteringen från vänster till höger; annars från topp till botten.
- _(Valfritt)_ `CaseOrder`, `SortLeftToRight`, etc. kan också anges enligt OpenAPI-specifikationen.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
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

**Felhantering** – API:et kan returnera standard-HTTP-felkoder. Vanliga svar inkluderar:

| HTTP-status | Kod | Meddelande                                        |
| ----------- | --- | ------------------------------------------------- |
| 400         | 400 | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401         | 401 | Obehörig – ogiltigt eller saknat JWT-token.        |
| 404         | 404 | Hittades inte – arbetsboken eller arket finns inte. |
| 500         | 500 | Internt serverfel.                               |

Svarsbrödtexten följer mönstret `{ "Code": <status>, "Message": "<description>", "Status": "Error" }` i felfall.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}