---
title: "Ta bort en bild från ett Excel-ark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, moln-API, ta bort bild, Excel-ark, REST"
description: "Ta bort en bild från ett Excel-ark med Aspose.Cells Cloud REST API. Lär dig DELETE-slutpunkten, nödvändiga parametrar, autentisering, felkoder och exempelkod."
weight: 50
ArticleTitle: "Ta bort en bild från ett Excel-ark – Aspose.Cells Cloud API"
---

Detta REST API tar bort en bild från ett Excel-ark.

### **Säkerhet och autentisering**

Aspose.Cells moln-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### Begäran parametrar

| Parameternamn   | Typ     | Plats  | Obligatorisk | Beskrivning                                          |
| --------------- | ------- | ------ | ------------ | ---------------------------------------------------- |
| name            | string  | path   | Ja           | Namnet på arbetsboksfilen.                          |
| sheetName       | string  | path   | Ja           | Namnet på arket som innehåller bilden.              |
| pictureIndex    | integer | path   | Ja           | Den nollbaserade indexpositionen för bilden som ska tas bort. |
| folder          | string  | query  | Nej          | Mappen där arbetsboken lagras.                      |
| storageName     | string  | query  | Nej          | Namnet på lagringstjänsten (valfritt).              |

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anropet med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
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

**Exempel på svarshuvuden**

| Huvud                | Värde                         |
|----------------------|------------------------------|
| Content-Type         | application/json             |
| Content-Length       | (varierar)                   |
| Date                 | (serverdatum)                |

{{< /tab >}}

{{< /tabs >}}

### Felhantering

| HTTP-kod | Betydelse                                                       | Exempel på feldata                                              |
| -------- | --------------------------------------------------------------- | -------------------------------------------------------------- |
| 200      | Bilden har tagits bort utan problem.                            | `{ "Code": 200, "Status": "OK" }`                              |
| 400      | Felaktig begäran – ogiltiga parametrar.                         | `{ "Code": 400, "Message": "Ogiltig pictureIndex." }`         |
| 401      | Oauktorisering – saknas/ogiltig token.                          | `{ "Code": 401, "Message": "Åtkomsttoken saknas eller är ogiltig." }` |
| 404      | Ej hittad – arbetsbok, ark eller bild finns inte.              | `{ "Code": 404, "Message": "Resursen hittades inte." }`        |
| 500      | Internt serverfel.                                              | `{ "Code": 500, "Message": "Oväntat serverfel." }`             |

## Moln SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på ditt projekt. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}