---
title: "Ta bort en specifik dokumentegenskap"
second_title: "Dokument"
linktitle: "Ta bort"
type: docs
url: /document-properties/delete/
aliases: [/remove-a-particular-document-property/]
keywords: "Aspose.Cells, ta bort dokumentegenskap, Excel-metadata-API, REST, moln-SDK, cURL-exempel"
description: "Ta bort en specifik dokumentegenskap från en Excel-arbetsbok med Aspose.Cells Cloud REST API v3.0. Innehåller cURL- och SDK-exempel för C#, Java, Python och mer."
weight: 50
---

Denna REST API tar bort en dokumentegenskap från en arbetsbok.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/documentproperties/{propertyName}
```

### Begäran parametrar

| Parameternamn   | Typ    | Plats  | Obligatorisk | Beskrivning                                      |
| --------------- | ------ | ------ | ------------ | ------------------------------------------------ |
| name            | string | path   | Ja           | Namnet på Excel-arbetsboken.                     |
| propertyName    | string | path   | Ja           | Namnet på den dokumentegenskap som ska tas bort. |
| folder          | string | query  | Nej          | Sökvägen till mappen där arbetsboken lagras.     |
| storageName     | string | query  | Nej          | Namnet på lagringstjänsten.                      |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Properties/DeleteDocumentProperty) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties/author" \
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

### Felaktiga svar

| HTTP-status | Beskrivning                                                       | Exempel på JSON                                              |
| ----------- | ----------------------------------------------------------------- | ------------------------------------------------------------ |
| 400         | Felaktig begäran – saknar obligatoriska parametrar eller ogiltiga värden. | `{"Code":400,"Message":"Missing required parameter 'name'."}` |
| 401         | Auktoriseringsfel – ogiltig eller saknad JWT-token.              | `{"Code":401,"Message":"Invalid access token."}`             |
| 404         | Hittades inte – arbetsboken eller den angivna egenskapen finns inte. | `{"Code":404,"Message":"Document property not found."}`      |
| 500         | Internt serverfel – ett oväntat tillstånd uppstod på servern.    | `{"Code":500,"Message":"An unexpected error has occurred."}` |

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektsuppgifter. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentProperty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentProperty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentProperty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentProperty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentProperty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentProperty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentProperty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentProperty.go" >}}

{{< /tab >}}

{{< /tabs >}}