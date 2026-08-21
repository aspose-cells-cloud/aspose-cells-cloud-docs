---
title: "Autojustera en rad i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Rad"
type: docs
url: /sv/worksheets/autofit/row/
aliases: [  /sv/autofit-single-row-of-worksheet/ ]
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att autojustera en rad i ett Excel-arbetsblad. Inkluderar slutpunkt, parametrar, autentisering, felhantering, cURL-förfrågan och SDK-exempel."
keywords: "autojustera rad, Aspose.Cells Cloud, Excel API, REST, arbetsblad, SDK, kalkylark, moln-API"
weight: 30
ArticleTitle: "Autojustera rad i Excel-arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API **autojusterar en rad** i ett Excel-arbetsblad.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitrow
```

### **Förfrågningsparametrar**

| Parameternamn     | Typ     | Plats  | Beskrivning                                                                                                                                                                                                  |
| ----------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| name              | string  | path   | Namnet på Excel-filen.                                                                                                                                                                                       |
| sheetName         | string  | path   | Namnet på arbetsbladet.                                                                                                                                                                                      |
| rowIndex          | integer | query  | Nollbaserat index för raden som ska autojusteras.                                                                                                                                                            |
| firstColumn       | integer | query  | Index för den första kolumnen som inkluderas i åtgärden.                                                                                                                                                     |
| lastColumn        | integer | query  | Index för den sista kolumnen som inkluderas i åtgärden.                                                                                                                                                      |
| autoFitterOptions | object  | body   | Objekt som styr autojusteringsbeteendet (t.ex. om hopslagna celler, textrutning etc. ska beaktas). Se [AutoFitterOptions](/cells/auto-fitter-options){:rel="noopener" title="Styr autojusteringsbeteendet"}. |
| folder            | string  | query  | Mapp där filen lagras.                                                                                                                                                                                       |
| storageName       | string  | query  | Namn på lagringsutrymmet.                                                                                                                                                                                    |

**Exempel på `autoFitterOptions` JSON-body**

```json
{
  "IsMergedCells": true,
  "IsWrapped": false,
  "AutoFitMergedCells": true,
  "AutoFitWrappedCells": false
}
```

### Entitetsdefinitioner

| Entitet               | Beskrivning                                                                              |
| --------------------- | ---------------------------------------------------------------------------------------- |
| `rowIndex`            | Nollbaserat index för målraden.                                                          |
| `firstColumn`         | Startkolumn för autojusteringsåtgärden.                                                  |
| `lastColumn`          | Slutkolumn för autojusteringsåtgärden.                                                   |
| `autoFitterOptions`   | Valfria inställningar som påverkar hur raden autojusteras (hopslagna celler, textrutning etc.). |

[OpenAPI-specifikationen](/cells/#/Worksheets/PostAutofitWorksheetRow) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Exemplet nedan visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitrow?rowIndex=2&firstColumn=1&lastColumn=10" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

| Fält   | Beskrivning                                |
| ------ | ------------------------------------------ |
| Code   | `200` – förfrågan lyckades.                |
| Status | `"OK"` – raden autojusterades framgångsrikt. |

{{< /tab >}}

{{< /tabs >}}

## Felhantering

API:et returnerar standard-HTTP-statuskoder. Vanliga felsvare för denna slutpunkt är:

| HTTP-kod | Exempelpayload                                           | Betydelse                                                                          |
| -------- | -------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| 400      | `{ "Code": 400, "Message": "Row index out of range." }` | Den angivna `rowIndex` existerar inte i arbetsbladet.                              |
| 401      | `{ "Code": 401, "Message": "Invalid or expired token." }` | Autentisering misslyckades – kontrollera JWT-token och se till att förfrågan görs via HTTPS. |
| 404      | `{ "Code": 404, "Message": "File not found." }`         | Den angivna Excel-filen eller arbetsbladet kan inte hittas.                        |
| 500      | `{ "Code": 500, "Message": "Internal server error." }`  | Ett oväntat serverproblem uppstod.                                                 |

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorksheetRow.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorksheetRow.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorksheetRow.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorksheetRow.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2c4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorksheetRow.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorksheetRow.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorksheetRow.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorksheetRow.go" >}}
{{< /tab >}}

{{< /tabs >}}

**Se även:** [Autojustera kolumn](/worksheets/autofit/column/), [Autojustera rader](/worksheets/autofit/rows/), [AutoFitterOptions](/cells/auto-fitter-options).