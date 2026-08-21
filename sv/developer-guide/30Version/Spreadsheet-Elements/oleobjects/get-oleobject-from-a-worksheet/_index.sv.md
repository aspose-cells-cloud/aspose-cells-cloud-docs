---
title: "Hämta OLE-objekt från Excel-arbetsblad – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Hämta"
type: docs
url: /oleobjects/get/
aliases: [/get-oleobject-from-a-worksheet/]
keywords: "aspose, cells, ole-objekt, excel, arbetsblad, hämta ole-objekt, rest api"
description: "Hämta ett OLE-objekt (bild, diagram eller inbäddad fil) från ett arbetsblad med Aspose.Cells Cloud REST API. Innehåller HTTPS-slutpunkt, nödvändiga parametrar, exempel på cURL och SDK-kod i flera språk."
ArticleTitle: "Hämta OLE-objekt från Excel-arbetsblad – Aspose.Cells Cloud API"
weight: 10
---

Denna REST API hämtar ett **OLE-objekt** från ett Excel-arbetsblad.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## Rest API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{objectNumber}?format={format}
```

### Begäranparametrar

| Parameternamn   | Typ     | Plats  | Beskrivning                                                  |
| --------------- | ------- | ------ | ------------------------------------------------------------ |
| name            | string  | path   | Dokumentets namn.                                            |
| sheetName       | string  | path   | Arbetsbladets namn.                                          |
| objectNumber    | integer | path   | Objektnumret inom arbetsbladet.                              |
| format          | string  | query  | Önskat exportformat för objektet (t.ex. `png`, `jpeg`).     |
| folder          | string  | query  | Mapp där dokumentet finns.                                   |
| storageName     | string  | query  | Namn på det lagringsutrymme som ska användas.                |

### Lagringsalternativ

- **folder** – anger undermappen i standardlagringen där arbetsboken finns.
- **storageName** – åsidosätter standardlagringsnamnet om arbetsboken lagras någon annanstans.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/OleObjects/GetWorksheetOleObject) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells-webbtjänsten. Exemplet nedan visar hur du begär ett OLE-objekt som en PNG-bild.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects/0?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

### Binärbildssvar

När `format` är inställt på ett bildformat (t.ex. `png`) returnerar API:et de binära bilddata med headern:

```
Content-Type: image/png
```

_(Bildfilen strömmas direkt till klienten.)_

### JSON-metadata-svar

Om `format` utelämnas eller är inställt på `json` returnerar API:et ett JSON-svar som beskriver OLE-objektet:

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Name": "Object1",
    "Width": 200,
    "Height": 150,
    "Left": 10,
    "Top": 20,
    "IsLocked": false,
    "FileFormat": "png"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Felhantering

| HTTP-status | Felkod       | Beskrivning                                      |
| ----------- | ------------ | ------------------------------------------------ |
| 400         | BadRequest   | Saknade eller ogiltiga parametrar.              |
| 401         | Unauthorized | Ogiltig eller saknad JWT-token.                 |
| 404         | NotFound     | Arbetsbok, arbetsblad eller OLE-objekt hittades inte. |
| 500         | ServerError  | Oväntat serverfel.                               |

**Exempel på 404-svar**

```json
{
  "Code": 404,
  "Status": "NotFound",
  "Message": "Det begärda OLE-objektet med nummer 0 hittades inte i arbetsbladet 'Sheet1'."
}
```

## Molnsdk-familj

Att använda en SDK är det snabbaste sättet att integrera API:et. SDK:er hanterar detaljer på lågnivå så att du kan fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}