---
title: "Lägg till en form i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /sv/shapes/add/
aliases: [  /sv/add-a-shape-inside-the-worksheet/ ]
keywords: "Aspose.Cells, lägg till form, Excel, REST API, molntjänst, shapeDTO, ritningstyp"
description: "Lär dig hur du lägger till former (båge, linje, rektangel m.fl.) i ett Excel-arbetsblad med Aspose.Cells Cloud REST API v3.0. Innehåller begäronsyntax, nödvändiga parametrar, autentiseringssteg och exempel på SDK-kod."
weight: 30
ArticleTitle: "Lägg till en form i ett Excel-arbetsblad med Aspose.Cells Cloud API"
---

Denna REST API lägger till en form i ett Excel-arbetsblad.  
Slutpunkten tillhör **API-version v3.0**; se till att du använder ett JWT-åtkomsttoken som du får via Aspose Cloud OAuth2-flödet (client-id/client-secret) och inkludera den i `Authorization: Bearer <token>`-hoften.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## PutWorksheetShape API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes
```

### **Begäranparametrar**

| Parametername   | Typ     | Plats  | Beskrivning                                                                                           |
| ---------------- | ------- | ------ | ----------------------------------------------------------------------------------------------------- |
| name             | string  | path   | Dokumentets namn.                                                                                     |
| sheetName        | string  | path   | Arbetsbladets namn.                                                                                   |
| shapeDTO         | object  | body   | JSON-objekt som beskriver formen som ska läggas till (se OpenAPI-specifikationen för fullständigt schema). |
| drawingType      | string  | query  | Typ av formobjekt (t.ex. `arc`, `line`, `rectangle`).                                                 |
| upperLeftRow     | integer | query  | Övre vänstra radindex för formen.                                                                    |
| upperLeftColumn  | integer | query  | Övre vänstra kolumnindex för formen.                                                                 |
| top              | integer | query  | Vertikal förskjutning från formens övre kant, i bildpunkter.                                            |
| left             | integer | query  | Horisontell förskjutning från formens vänstra kant, i bildpunkter.                                         |
| width            | integer | query  | Formens bredd, i bildpunkter.                                                                        |
| height           | integer | query  | Formens höjd, i bildpunkter.                                                                        |
| folder           | string  | query  | Mappen som innehåller dokumentet.                                                                    |
| storageName      | string  | query  | Namn på lagringsutrymmet.                                                                                  |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Shapes/PutWorksheetShape) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör ett anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/shapes?DrawingType=arc&upperLeftRow=1&upperLeftColumn=1&top=1&left=1&width=100&height=100" \
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
  "Status": "OK",
  "ShapeId": 5
}
```

_Ett lyckat svar returnerar HTTP-statuskoden, en textuell status och identifieraren för den nyligen skapade formen (`ShapeId`)._

{{< /tab >}}

{{< /tabs >}}

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

Typiska felaktiga svar inkluderar:

- **400 Felaktig begäran** – saknade eller ogiltiga parametrar.  
- **401 Oauktoriserad** – ogiltig eller saknad JWT-token.  
- **404 Ej hittad** – det angivna arbetsbladet eller dokumentet finns inte.

Varje fel returneras som ett JSON-objekt med fälten `Code` och `Message`.

## Molntjänstfamilj för SDK

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}