---
title: "Tillämpa formatering med rik text på en cell"
type: docs
url: /sv/apply-rich-text-formatting-to-a-cell/
weight: 40
keywords: "Aspose.Cells, Excel, rik text, cellformatering, REST API, Aspose.Cells Cloud"
description: "Lär dig hur du tillämpar formatering med rik text på en specifik Excel-cell med Aspose.Cells Cloud REST API. Innehåller begärsyntax, parameterinformation, cURL-exempel och SDK-utdrag."
ArticleTitle: "Tillämpa formatering med rik text på en cell med Aspose.Cells Cloud API"
---

Denna REST API tillämpar **formatering med rik text** på en cell i en Excel-fil.

**Förutsättningar:** Du måste ha en giltig JWT-token, och mål-Excel-filen måste redan finnas i den angivna lagringsmappen innan du utför denna åtgärd.

**Bakgrund:** Formatering med rik text möjliggör att tillämpa flera teckensnittsstilar inom en enda cell, vilket gör det möjligt att presentera data mer uttrycksfullt i Excel-arbetsblad.

## PostCellCharacters API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/characters
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| ParameterNamn  | Typ    | Plats                        | Beskrivning                                                                 |
|----------------|--------|------------------------------|-----------------------------------------------------------------------------|
| name           | string | path                         | Namnet på Excel-filen (t.ex. `Book1.xlsx`).                               |
| sheetName      | string | path                         | Arbetsbladet som innehåller målcellen.                                     |
| cellName       | string | path                         | Adressen till cellen som ska formateras (t.ex. `A1`).                      |
| options        | object | body                         | JSON-objekt som definierar inställningarna för formatering med rik text för cellen. |
| folder         | string | query                        | Mappen i lagringen där Excel-filen finns.                                 |
| storageName    | string | query                        | Namnet på lagringstjänsten (om en anpassad lagring används).              |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Formatering tillämpades framgångsrikt; svaret innehåller åtgärdsinformation. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                        |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.      |
| 500 | Internal Server Error       | Oväntat serverfel.                                     |

## Hur du använder PostCellCharacters API med SDK:er

### PostCellCharacters API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PostCellCharacters) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/characters" \
-X POST \
-d "{ \"FontSetting\": [ { \"Font\": { \"IsBold\": \"true\", \"Size\": \"24\" }, \"Length\": \"5\", \"StartIndex\": \"0\" }, { \"Font\": { \"IsItalic\": \"true\", \"Size\": \"15\" }, \"Length\": \"4\", \"StartIndex\": \"5\" } ] }" \
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
*C#-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCharacters.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
*Java-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCharacters.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
*PHP-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCharacters.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
*Ruby-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCharacters.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
*Node.js-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCharacters.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
*Python-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCharacters.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
*Perl-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCharacters.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
*Go-SDK-exempel*  

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCharacters.go" >}}
{{< /tab >}}

{{< /tabs >}}
---