---
title: "Hämta sidantal från en Excel-fil"
second_title: "Dokument"
linktitle: "Sidor"
type: docs
url: /sv/get-page-count-from-an-excel-file/
aliases: [  /sv/workbook/page-count/ , /sv/workbook/get/page-count/ ]
keywords: "Aspose.Cells, moln-API, Excel-sidantal, arbetshandsboksformatering"
description: "Hämta det totala antalet utskrivbara sidor i en Excel-arbetshandsbok via Aspose.Cells Cloud REST API (v3.0). Innehåller begäranformat, nödvändiga parametrar, cURL-exempel, svarschema, felhantering och SDK-utdrag för flera språk."
weight: 10
version: "v3.0"
ArticleTitle: "Hämta sidantal från en Excel-fil med Aspose.Cells Cloud API"
---

Denna REST API returnerar **sidantalet** för en arbetshandsbok.

## Säkerhet och autentisering
Aspose.Cells Cloud-API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### Begäranparametrar

| Parameternamn | Typ   | Plats  | Nödvändig | Beskrivning                            |
| ------------- | ----- | ------ | --------- | -------------------------------------- |
| name          | string | path   | Ja        | Namnet på Excel-dokumentet.            |
| folder        | string | query  | Nej       | Mappen som innehåller dokumentet.      |
| storageName   | string | query  | Nej       | Namnet på den lagring som ska användas.|

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells REST API. Följande exempel visar hur du anropar slutpunkten med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/DinFil.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

*Ersätt `DinFil.xlsx` med det faktiska namnet på den arbetshandsbok du vill fråga.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Svarschema

| HTTP-status | Datatyp | Beskrivning                                              |
| ----------- | ------- | -------------------------------------------------------- |
| 200         | integer | Det totala antalet utskrivbara sidor i arbetshandsboken (t.ex. `13`). |
| 4xx‑5xx     | JSON    | Felobjekt (se avsnittet *Felhantering*).                 |

## Molnsdk-familj

Att använda en sdk är det bästa sättet att påskynda utvecklingen. En sdk hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud sdks.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika sdks:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Felhantering

| HTTP-status | Beskrivning                              | Exempel på JSON-kropp                                                                 |
| ----------- | ---------------------------------------- | ------------------------------------------------------------------------------------ |
| 401         | Ogiltig eller saknad JWT-token.          | `{ "Code": "InvalidAuthenticationToken", "Message": "Åtkomsttoken saknas eller är ogiltig." }` |
| 404         | Den angivna arbetshandsboken kunde inte hittas. | `{ "Code": "FileNotFound", "Message": "Den begärda filen finns inte." }`            |
| 400         | Felaktig begäran – nödvändiga parametrar saknas. | `{ "Code": "BadRequest", "Message": "Nödvändig parameter 'name' saknas." }`         |
| 500         | Internt serverfel.                       | `{ "Code": "InternalError", "Message": "Ett oväntat fel uppstod." }`                 |