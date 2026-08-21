---
title: "Sammanfoga celler i ett Excel-arbetsblad"
type: docs
url: /sv/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, Sammanfoga celler, REST API, molntjänst SDK"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att sammanfoga celler i ett Excel-arbetsblad, med exempel på begäranden, svarsformat och SDK-kodexempel för flera programmeringsspråk."
ArticleTitle: "Sammanfoga celler i ett Excel-arbetsblad"
---

Denna REST API sammanfogar celler i en Excel-fil.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


**Begärandeparametrar**

| Parameternamn   | Typ     | Plats  | Beskrivning                                              |
|-----------------|---------|--------|----------------------------------------------------------|
| name            | string  | path   | Namn på arbetsbokens fil.                                |
| sheetName       | string  | path   | Namn på arbetsbladet.                                    |
| startRow        | integer | query  | Nollbaserat index för första raden som ska sammanfogas.  |
| startColumn     | integer | query  | Nollbaserat index för första kolumnen som ska sammanfogas. |
| totalRows       | integer | query  | Antal rader som ingår i sammanfogningsåtgärden.         |
| totalColumns    | integer | query  | Antal kolumner som ingår i sammanfogningsåtgärden.      |
| folder          | string  | query  | Mappväg där arbetsboken lagras.                          |
| storageName     | string  | query  | Namn på lagringstjänsten.                                |

## **Svar**

Returnerar CellCloudResponse.

- **Översikt över svarsfält**

| Fält            | Typ     | Beskrivning                                          |
| --------------- | ------- | ---------------------------------------------------- |
| `Status`        | string  |                                                      |
| `Code`          | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder PostWorksheetUnmerge API med SDK:er

### PostWorksheetUnmerge API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}
---