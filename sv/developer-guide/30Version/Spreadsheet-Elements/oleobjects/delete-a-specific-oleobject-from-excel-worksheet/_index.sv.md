---
title: "Ta bort ett OLE-objekt i ett Excel-arbetsark"
second_title: "Dokument"
linktitle: "Ta bort"
type: docs
url: /oleobjects/delete/
aliases: [/delete-a-specific-oleobject-from-excel-worksheet/]
keywords: "Aspose.Cells, Moln, Ta bort, OLE, Objekt, Excel, arbetsark, REST, API, SDK"
description: "Lär dig hur du tar bort ett OLE-objekt från ett Excel-arbetsark med Aspose.Cells Cloud REST API (v4.0). Inkluderar HTTPS-slutpunkt, autentiseringssteg, cURL-exempel, SDK-utdrag, felhanteringsanvisningar och länkar till nästa steg."
weight: 50
ArticleTitle: "Ta bort OLE-objekt från Excel-arbetsark med Aspose.Cells Cloud API"
---

Den här sidan förklarar hur du tar bort ett specifikt OLE-objekt från ett ark i en Excel-arbetsbok med **Aspose.Cells Cloud**. Ett OLE-objekt kan vara en länkad bild, ett diagram eller något annat inbäddat objekt som Excel lagrar som en egen entitet.

## Säkerhet och autentisering
Aspose.Cells Cloud-API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

### Begärningsparametrar

| Parameternamn    | Typ     | Plats  | Beskrivning                                        |
| ---------------- | ------- | ------ | -------------------------------------------------- |
| name             | string  | path   | Arbetsbokens namn.                                 |
| sheetName        | string  | path   | Arkets namn.                                       |
| oleObjectIndex   | integer | path   | Index för det OLE-objekt som ska tas bort.         |
| folder           | string  | query  | Mappen som innehåller arbetsboken. (valfritt)      |
| storageName      | string  | query  | Namnet på lagringstjänsten. (valfritt)             |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/OleObjects/DeleteWorksheetOleObject) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anropet med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v4.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0" \
  -X DELETE \
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

### Svardetaljer

| HTTP-status          | Beskrivning                                                           | Exempel-JSON                                                       |
| -------------------- | --------------------------------------------------------------------- | ----------------------------------------------------------------- |
| **200 OK**           | OLE-objektet togs framgångsrikt bort.                                | `{ "Code": 200, "Status": "OK" }`                                 |
| **401 Unauthorized** | JWT-token saknas eller är ogiltig.                                   | `{ "Code": 401, "Message": "Access token is missing or invalid." }` |
| **404 Not Found**    | Den angivna arbetsboken, arbetsarket eller OLE-objektindexet finns inte. | `{ "Code": 404, "Message": "OLE object index out of range." }`    |
| **400 Bad Request**  | Nödvändiga parametrar saknas eller är felaktigt formaterade.         | `{ "Code": 400, "Message": "Invalid request parameters." }`      |

Hantera dessa svar i din applikation genom att kontrollera statuskoden och visa tillhörande meddelande.

## Moln SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}