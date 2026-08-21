---
title: "Lägg till ett listobjekt (tabell) i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /sv/list-objects/add/
aliases: [  /sv/add-a-list-object-or-table-inside-the-worksheet/ , /sv/tables/add/ ]
keywords: "Aspose.Cells Cloud, Excel API, listobjekt, tabell, REST API, arbetsblad"
description: "Lär dig hur du lägger till ett listobjekt (Excel-tabell) i ett arbetsblad med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, parametrar, autentiseringsssteg, cURL-exempel och SDK-kodexempel."
weight: 10
ArticleTitle: "Lägg till ett listobjekt (tabell) i ett Excel-arbetsblad – Aspose.Cells Cloud-dokumentation"
---

Detta REST API lägger till ett **listobjekt (tabell)** i ett Excel-arbetsblad.

Innan du använder denna slutpunkt, se till att du har en giltig JWT-token, att arbetsboken lagras i ett stöddat molnlagringssystem och att arbetsbladet finns.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects
```

### Begärparametrar

| Parametername   | Typ     | Plats  | Beskrivning                                                           |
| --------------- | ------- | ------ | --------------------------------------------------------------------- |
| **name**        | string  | path   | Namn på arbetsboksfilen.                                              |
| **sheetName**   | string  | path   | Namn på arbetsbladet.                                                 |
| **startRow**    | integer | query  | Nollbaserat index för den första raden i tabellintervallet.           |
| **startColumn** | integer | query  | Nollbaserat index för den första kolumnen i tabellintervallet.        |
| **endRow**      | integer | query  | Nollbaserat index för den sista raden i tabellintervallet.            |
| **endColumn**   | integer | query  | Nollbaserat index för den sista kolumnen i tabellintervallet.         |
| **hasHeaders**  | boolean | query  | `true` om den första raden innehåller kolumnrubriker, annars `false`. |
| **listObject**  | object  | body   | Definitionen av listobjektet (se **Schemat för begärandetexten**).    |
| **folder**      | string  | query  | Mapp som innehåller arbetsboken.                                      |
| **storageName** | string  | query  | Lagringsnamn.                                                         |

### Schemat för begärandetexten

Objektet **listObject** beskriver tabellen som ska skapas. Endast de vanligaste egenskaperna visas; se OpenAPI-specifikationen för den fullständiga listan.

```json
{
  "displayName": "MinTabell",
  "showTotals": false,
  "style": "TableStyleMedium2"
}
```

### Exempel på begäran (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects?startRow=1&startColumn=1&endRow=10&endColumn=12&hasHeaders=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "displayName": "MinTabell",
        "showTotals": false,
        "style": "TableStyleMedium2"
      }'
```

### Exempel på svar

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Felkoder

| HTTP-status | Anledning         | Beskrivning                                      |
| ----------- | ----------------- | ------------------------------------------------ |
| **400**     | Felaktig begäran  | Ogiltiga intervalsparametrar eller felaktig JSON-begärandetext. |
| **401**     | Otillåten         | Saknad eller utgången JWT-token.                 |
| **404**     | Hittades inte     | Den angivna arbetsboken eller arbetsbladet finns inte. |
| **500**     | Internt serverfel | Oväntat serverfel på serversidan.                |

**Exempel på 400-svar**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Invalid range parameters."
}
```

**Exempel på 401-svar**

```json
{
  "Code": 401,
  "Status": "Unauthorized",
  "Message": "Authentication token is missing or expired."
}
```

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/ListObjects/PutWorksheetListObject) innehåller den fullständiga kontraktet för denna operation.

## Molnsdk-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetListObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetListObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetListObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetListObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetListObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetListObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetListObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetListObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---