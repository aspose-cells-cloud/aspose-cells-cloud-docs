---
title: "Ta bort horisontell sidbrytning"
ArticleTitle: "Aspose.Cells Cloud – Ta bort horisontell sidbrytning (REST API)"
second_title: "Dokument"
linktitle: "Ta bort horisontell sidbrytning"
type: docs
url: /page-breaks/delete-horizontal-page-break/
aliases: [/delete-horizontal-page-break-inside-worksheet/]
keywords: "Aspose.Cells Cloud, Ta bort horisontell sidbrytning, Excel-ark, REST API, SDK"
description: "Ta bort en horisontell sidbrytning från ett Excel-ark med Aspose.Cells Cloud REST API. SDK:er finns för C#, Java, PHP, Ruby, Node.js, Python, Perl och Go."
weight: 50
---

Denna REST API tar bort en **horisontell** sidbrytning.

**Förutsättningar**: För att anropa detta slutpunkt måste du ha en giltig Aspose Cloud JWT-åtkomsttoken. Skaffa den genom att följa [Autentisieringshandboken](https://docs.aspose.cloud/cells/authentication/).

## DeleteHorizontalPageBreak API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Alla API-anrop måste göras över **HTTPS**.*

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameternamn   | Typ     | Plats  | Beskrivning                                                |
| --------------- | ------- | ------ | ---------------------------------------------------------- |
| `name`          | string  | path   | Namnet på Excel-filen (arbetsboken).                       |
| `sheetName`     | string  | path   | Namnet på arket som innehåller sidbrytningen.              |
| `index`         | integer | path   | Nullbaserat index för den horisontella sidbrytning som ska tas bort. |
| `folder`        | string  | query  | Valfri mappväg i lagringen där filen finns.               |
| `storageName`   | string  | query  | Valfritt namn på lagringstjänsten.                         |

### Felsvar

| HTTP-kod | Beskrivning                                                              |
| -------- | ------------------------------------------------------------------------ |
| 401      | Inte auktoriserad – saknad eller ogiltig token.                         |
| 404      | Hittades inte – den angivna filen, arket eller sidbrytningsindexet finns inte. |
| 400      | Felaktig begäran – felaktig begäransyntax eller ogiltiga parametrar.    |
| 500      | Internt serverfel – ett oväntat tillstånd inträffade.                   |

**Se även:**  
- [Lägg till horisontell sidbrytning](/page-breaks/add-horizontal-page-break/)  
- [Hämta horisontella sidbrytningar](/page-breaks/get-horizontal-page-breaks/)  
- [Ta bort vertikal sidbrytning](/page-breaks/delete-vertical-page-break/)

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anropet med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**Responschema**

| Fält    | Typ     | Beskrivning                                     |
|---------|---------|-------------------------------------------------|
| Code    | integer | HTTP-statuskod (t.ex. 200).                     |
| Status  | string  | Textuell statusmeddelande (t.ex. "OK").         |
| Message | string  | Valfri ytterligare information vid fel.         |

{{< /tab >}}

{{< /tabs >}}

## Moln-SDK-familj

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d).*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f).*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152).*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca).*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0).*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1).*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca).*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Om exemplet inte laddas, visa det på [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185).*

{{< /tab >}}

{{< /tabs >}}