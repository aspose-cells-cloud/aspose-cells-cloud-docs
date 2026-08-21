---
title: "Ta bort flera Excel-ark"
second_title: "Dokument"
linktitle: "Flera ark"
type: docs
url: /sv/worksheets/delete-multiple/
aliases: [/sv/delete-excel-worksheets/]
keywords: "Aspose.Cells Cloud, ta bort flera Excel-ark, Excel-API, REST-API, v3.0, ta bort ark"
description: "Lär dig hur du tar bort flera ark från en Excel-arbetsbok med Aspose.Cells Cloud REST API (v3.0). Innehåller en säker HTTPS-slutpunkt, nödvändiga parametrar, ett korrigert cURL-exempel och SDK-utdrag för flera programmeringsspråk."
weight: 20
ArticleTitle: "Ta bort flera Excel-ark med Aspose.Cells Cloud REST API"
---

Denna REST API tar bort flera ark från en arbetsbok.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets
```

### **Begärparametrar**

| Parameternamn   | Typ    | Plats  | Beskrivning                                                                 |
| --------------- | ------ | ------ | --------------------------------------------------------------------------- |
| name            | string | path   | Namnet på Excel-filen.                                                      |
| matchCondition  | object | body   | Ett `MatchConditionRequest`-objekt som anger vilka ark som ska tas bort.   |
| folder          | string | query  | Mappväg i lagringen där filen finns.                                        |
| storageName     | string | query  | Namnet på lagringstjänsten.                                                 |

**MatchConditionRequest-egenskaper**

| Namn                | Typ       | Beskrivning                                 | Noteringar    |
| ------------------- | --------- | ------------------------------------------- | ------------- |
| RegexPattern        | string    | Reguljärt uttryck för att matcha arknamn.  | valfritt      |
| FullMatchConditions | string[]  | Exakta arknamn som ska tas bort.            | valfritt      |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheets) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL. **Ett giltigt JWT-token krävs i `Authorization`-headern.**

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets?folder=Temp" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>" \
  -d '{"FullMatchConditions":["Sheet1","Sheet2","Sheet3"]}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Begäran kan också returnera vanliga felresponser, till exempel:

| HTTP-status | Betydelse                                    | Exempel på nyttolast                                      |
| ----------- | -------------------------------------------- | --------------------------------------------------------- |
| 400         | Felaktig begäran – ogiltig JSON eller parametrar | `{"Code":400,"Message":"Invalid request payload."}`      |
| 401         | Auktorisationsfel – saknad eller ogiltig JWT-token | `{"Code":401,"Message":"Authentication failed."}`        |
| 403         | Åtkomst nekad – otillräckliga rättigheter    | `{"Code":403,"Message":"Access denied."}`                |
| 404         | Inte hittad – fil eller ark finns inte       | `{"Code":404,"Message":"Resource not found."}`           |
| 500         | Internt serverfel                            | `{"Code":500,"Message":"An unexpected error occurred."}` |

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheets.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheets.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheets.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheets.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheets.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheets.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheets.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Se även:**  
- [Ta bort ett enskilt ark](https://docs.aspose.cloud/cells/sv/worksheets/delete/)  
- [Kopiera ark](https://docs.aspose.cloud/cells/sv/worksheets/copy/)  
- [Flytta ark](https://docs.aspose.cloud/cells/sv/worksheets/move/)  
---