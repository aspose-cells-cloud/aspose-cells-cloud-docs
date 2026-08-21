---
title: "Hämta en form efter index på ett Excel-arbetsark"
second_title: "Dokument"
linktitle: "Hämta"
type: docs
url: /sv/shapes/get/
aliases: [/sv/get-a-shape-by-index-inside-the-worksheet/]
keywords: "Aspose.Cells Cloud, Excel-form-API, hämta form efter index, arbetsarkform, REST-API, formhämtning, Aspose.Cells SDK"
description: "Hämta en form efter dess index från ett Excel-arbetsark med Aspose.Cells Cloud REST API. Innehåller begäranSyntax, parametrar, svarsinformation och SDK-exempel."
weight: 20
ArticleTitle: "Hämta en form efter index på ett Excel-arbetsark – Aspose.Cells Cloud-dokumentation"
---

Denna REST API hämtar en form (inklusive dess bilddata eller metadata) från ett Excel-arbetsark.

## GetWorksheetShape API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/shapes/{shapeindex}
```

**Förutsättningar**  
- En giltig Aspose Cloud-åtkomsttoken (Bearer JWT).  
- Arbetsboken måste lagras i din Aspose Cloud-lagring eller en angiven mapp.  

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameternamn  | Typ     | Plats   | Beskrivning                                         |
| -------------- | ------- | ------- | --------------------------------------------------- |
| name           | string  | path    | Namn på Excel-dokumentet.                           |
| sheetName      | string  | path    | Namn på arbetsarket som innehåller formen.          |
| shapeindex     | integer | path    | Nollbaserat index för formen inom arbetsarket.      |
| folder         | string  | query   | Mappväg där dokumentet lagras.                      |
| storageName    | string  | query   | Namn på lagringstjänsten.                           |

**Obs:** `shapeindex` är nollbaserat; den första formen har index 0. Se till att arbetsboken är lagrad i den angivna `folder` och `storageName` om du inte använder standardlagringen.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Shapes/GetWorksheetShape) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Korrekt endpoint och sökväg
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet4/shapes/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "Shape": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "Name": "string",
    "MsoDrawingType": "string",
    "AutoShapeType": "string",
    "Placement": "string",
    "UpperLeftRow": 0,
    "Top": 0,
    "UpperLeftColumn": 0,
    "Left": 0,
    "LowerRightRow": 0,
    "Bottom": 0,
    "LowerRightColumn": 0,
    "Right": 0,
    "Width": 0,
    "Height": 0,
    "X": 0,
    "Y": 0,
    "RotationAngle": 0,
    "HtmlText": "string",
    "Text": "string",
    "AlternativeText": "string",
    "TextHorizontalAlignment": "string",
    "TextHorizontalOverflow": "string",
    "TextOrientationType": "string",
    "TextVerticalAlignment": "string",
    "TextVerticalOverflow": "string",
    "IsGroup": true,
    "IsHidden": true,
    "IsLockAspectRatio": true,
    "IsLocked": true,
    "IsPrintable": true,
    "IsTextWrapped": true,
    "IsWordArt": true,
    "LinkedCell": "string",
    "ZOrderPosition": 0
  }
}
```

{{< /tab >}}

{{< /tabs >}}

**Möjliga HTTP-statuskoder**

| Kod  | Beskrivning |
|------|-------------|
| **200 OK** | Formen hämtades framgångsrikt. |
| **400 Bad Request** | Begäran är felaktigt formaterad eller saknar nödvändiga parametrar. |
| **401 Unauthorized** | Autentisering misslyckades eller token saknas/är ogiltig. |
| **404 Not Found** | Den angivna arbetsboken, arbetsarket eller formindexet finns inte. |
| **500 Internal Server Error** | Ett oväntat serverfel uppstod. |

**Vanliga felkällor:** Användning av felaktig rotdomän (`api.aspose.com`) eller den föråldrade `/autoshapes/`-sökvägen leder till ett 404-fel. Använd alltid `/shapes/`-sökvägen med domänen `api.aspose.cloud`.

## Cloud SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projekttal. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetShape.go" >}}

{{< /tab >}}

{{< /tabs >}}

För relaterade åtgärder, se dokumentationen för **[Lägga till en form](/sv/shapes/add/)** och **[Uppdatera en form](/sv/shapes/update/)**.