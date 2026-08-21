---
title: "Ta bort bakgrund på ett Excel-ark"
second_title: "Dokument"
linktitle: "Ta bort"
type: docs
url: /worksheets/background/delete/
aliases: [/delete-background-or-watermark-of-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Ta bort bakgrund på arket, Excel, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Använd Aspose.Cells Cloud REST API för att ta bort bakgrundsbilden från ett Excel-ark. SDK:er finns tillgängliga för C#, Java, PHP, Ruby, Node.js, Python, Perl och Go."
weight: 210
ArticleTitle: "Ta bort bakgrund på ett Excel-ark med Aspose.Cells Cloud API"
---

Denna REST API tar bort bakgrundsbilden från ett ark.

**Förutsättningar:** Du måste ha arbetshandboken lagrad i Aspose Cloud-lagring och ha ett giltigt JWT-åtkomsttoken för autentisering.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/background
```

### **Begärparametrar**

| Parameternamn | Typ   | Plats  | Beskrivning                                         |
| ------------- | ----- | ------ | --------------------------------------------------- |
| name          | string | path   | Namnet på Excel-filen.                              |
| sheetName     | string | path   | Namnet på arket vars bakgrund ska tas bort.        |
| folder        | string | query  | Mappen i lagring där filen finns.                   |
| storageName   | string | query  | Namnet på lagringen (om det inte är standardlagring). |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheetBackground) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du enkelt kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Alla begärningar kräver en giltig JWT-token. Hämta token via OAuth2-tokenändpunkten enligt beskrivningen i autentiseringsguiden.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/WorkSheetBackground_Sample_Test_Book.xls/worksheets/Sheet1/background" \
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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                              |
|-----|-----------------------------|----------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                          |
| 413 | Payload för stor            | Den uppladdade filen överskrider storleksgränsen.        |
| 500 | Internt serverfel           | Oväntat serverfel.                                       |

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}