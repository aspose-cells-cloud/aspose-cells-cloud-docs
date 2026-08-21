---
title: "Rensa hyperlänkar"
type: docs
url: /hyperlinks/clear/
aliases: [/add-hyperlinks-to-excel-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, rensa hyperlänkar, ta bort hyperlänkar, REST API, kalkylblad, SDK"
description: "Lär dig hur du tar bort alla hyperlänkar från ett Excel-kalkylblad med Aspose.Cells Cloud REST API eller någon av de SDK:er som stöds (C#, Java, Python, Node.js, Go, PHP, Ruby, Perl etc.)."
weight: 40
ArticleTitle: "Rensa hyperlänkar – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API tar bort **alla hyperlänkar** från ett Excel-kalkylblad.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks
```

### Begärparametrar

| Parameter namn | Typ    | Plats  | Beskrivning                            |
| -------------- | ------ | ------ | -------------------------------------- |
| name           | string | path   | Namnet på Excel-filen.                 |
| sheetName      | string | path   | Namnet på kalkylbladet.                |
| folder         | string | query  | Mappen som innehåller dokumentet.      |
| storageName    | string | query  | Namnet på lagringstjänsten.            |

### Felresponser

| HTTP-kod | Anledning                                             | Exempel på svarskropp                                             |
| -------- | ----------------------------------------------------- | ---------------------------------------------------------------- |
| **400**  | Felaktig begäran – saknade eller ogiltiga parametrar. | `{ "Code":"400", "Message":"Invalid parameter value." }`        |
| **401**  | Oauktoriserad – saknad eller ogiltig JWT-token.       | `{ "Code":"401", "Message":"Access token is missing or invalid." }` |
| **404**  | Inte hittad – arbetsbok eller kalkylblad finns inte. | `{ "Code":"404", "Message":"File not found." }`                  |
| **500**  | Internt serverfel – oväntat serverfel.                | `{ "Code":"500", "Message":"An unexpected error occurred." }`   |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlinks) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att anropa Aspose.Cells-webbtjänster. Exempel nedan visar hur du tar bort alla hyperlänkar från ett kalkylblad.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test1.xlsx/worksheets/Sheet1/hyperlinks" \
  -X DELETE \
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

## Moln-SDK-familj

Att använda en SDK påskyndar utvecklingen genom att hantera detaljer på låg nivå åt dig. För en fullständig lista över Aspose.Cells Cloud SDK:er, besök [GitHub-repositoriet](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur du tar bort hyperlänkar från kalkylblad med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetHyperlinks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetHyperlinks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetHyperlinks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetHyperlinks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetHyperlinks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetHyperlinks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetHyperlinks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetHyperlinks.go" >}}

{{< /tab >}}

{{< /tabs >}}