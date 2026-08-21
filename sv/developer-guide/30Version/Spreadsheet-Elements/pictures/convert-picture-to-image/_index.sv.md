---
title: "Aspose.Cells Cloud API – Hämta bild från kalkylblad"
second_title: "Dokument"
linktitle: "Hämta"
type: docs
url: /pictures/get/
aliases: [/convert-picture-to-image/]
keywords: "Aspose.Cells, Hämta bild, API, Excel, Moln, REST"
description: "Hämta en specifik bild från ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Inkluderar slutpunkt, parametrar, autentiseringssteg, svarsstatuskoder och kodexempel."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API – Hämta bild från kalkylblad"
---

Denna REST API hämtar en bild med hjälp av dess nollbaserade index från ett Excel-kalkylblad.

## REST API

För att anropa denna slutpunkt måste du inkludera ett giltigt JWT-åtkomsttoken i **Authorization**-headern. Tokens erhålls via Aspose.Cells Cloud-autentiseringsflödet och kräver lämpliga omfattningar för filåtkomst. För detaljer om hur du skaffar en token, se den globala guiden **Autentisering**.

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Begäranparametrar

| Parametername   | Typ     | Plats  | Beskrivning                                                                                                        |
| ---------------- | ------- | ------ | ------------------------------------------------------------------------------------------------------------------ |
| name             | string  | path   | Namn på Excel-dokumentet.                                                                                          |
| sheetName        | string  | path   | Namn på kalkylbladet.                                                                                              |
| pictureIndex     | integer | path   | Nollbaserat index för bilden.                                                                                      |
| format           | string  | query  | Önskat exportformat (t.ex. png, jpg, bmp, gif, tiff). Om utelämnas returneras bilden i sitt ursprungliga format. |
| folder           | string  | query  | Mapp som innehåller dokumentet.                                                                                    |
| storageName      | string  | query  | Namn på lagringsplatsen.                                                                                           |

### Felrespons

| HTTP-kod | Beskrivning                                                               |
| -------- | ------------------------------------------------------------------------- |
| 401      | Ej auktoriserad – token saknas eller är ogiltig.                         |
| 404      | Hittades inte – den angivna filen, kalkylbladet eller sidbrytningsindexet finns inte. |
| 400      | Felaktig begäran – felaktig syntaktisk struktur eller ogiltiga parametrar. |
| 500      | Internt serverfel – ett oväntat tillstånd uppstod.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Pictures/GetWorksheetPicture) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1?format=png" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
# Binära bilddata (PNG) returneras i svarsbrödtexten.
# Exempel: base64-kodat utdrag
iVBORw0KGgoAAAANSUhEUgAA...
```

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPictureWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPictureWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPictureWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "ExampleGetWorksheetPictureWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "ExampleGetWorksheetPictureWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ExampleGetWorksheetPictureWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "ExampleGetWorksheetPictureWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "ExampleGetWorksheetPictureWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}