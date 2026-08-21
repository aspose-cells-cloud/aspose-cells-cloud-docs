---
title: "Lägg till en vertikal sidbrytning"
second_title: "Document"
linktitle: "Lägg till en vertikal sidbrytning"
type: docs
url: /sv/page-breaks/add-vertical-page-break/
aliases: [  /sv/insert-vertical-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, vertikal sidbrytning, REST API, Excel, SDK, cURL"
description: "Lär dig hur du infogar en vertikal sidbrytning i ett Excel-ark med Aspose.Cells Cloud REST API (v3.0). Innehåller begärsyntax, cURL-exempel, SDK-exempel, autentiseringshandbok och detaljerad felhantering."
weight: 40
ArticleTitle: "Lägg till en vertikal sidbrytning – Aspose.Cells Cloud API"
---

Denna REST API infogar en vertikal sidbrytning i ett kalkylblad.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/verticalpagebreaks
```

### Begärparametrar

| Parameter Name | Typ     | Plats  | Beskrivning                                                                 |
| -------------- | ------- | ------ | --------------------------------------------------------------------------- |
| name           | string  | path   | Namnet på Excel-arbetsboken.                                                |
| sheetName      | string  | path   | Namnet på kalkylbladet där sidbrytningen ska läggas till.                  |
| cellname       | string  | query  | Cellreferensen (t.ex. **A1**) som definierar sidbrytningsplatsen.           |
| column         | integer | query  | Det nollbaserade indexet för den kolumn där sidbrytningen börjar.          |
| row            | integer | query  | Det nollbaserade indexet för den rad där sidbrytningen börjar.             |
| startRow       | integer | query  | Den första raden i sidbrytningsintervallet.                                |
| endRow         | integer | query  | Den sista raden i sidbrytningsintervallet.                                 |
| folder         | string  | query  | Mappsökvägen i lagringen där arbetsboken finns.                            |
| storageName    | string  | query  | Namnet på lagringstjänsten.                                                 |

**Obligatoriska parametrar** – Antingen `cellname` **eller** `column` måste anges. När `column` används kan du även ange `row`, `startRow` och `endRow` för att definiera ett intervall. Alla andra fält är valfria.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PageBreaks/PutVerticalPageBreak) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### cURL-exempel

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/SampleBreaks.xlsx/worksheets/Sheet1/verticalpagebreaks?column=9" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Svar

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                     |
|-----|-----------------------------|-----------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request (Felaktig begäran) | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized (Ej auktoriserad) | Ogiltig eller saknad JWT-token.                               |
| 413 | Payload Too Large (För stor payload) | Den uppladdade filen överskrider storleksgränsen.            |
| 500 | Internal Server Error (Internt serverfel) | Oväntat serverfel.                                          |

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutVerticalPageBreak.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutVerticalPageBreak.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutVerticalPageBreak.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutVerticalPageBreak.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutVerticalPageBreak.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutVerticalPageBreak.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutVerticalPageBreak.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutVerticalPageBreak.go" >}}

{{< /tab >}}

{{< /tabs >}}
---