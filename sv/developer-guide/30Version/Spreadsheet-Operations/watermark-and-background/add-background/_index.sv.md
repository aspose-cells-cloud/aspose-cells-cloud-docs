---
title: "Lägg till bakgrundsbild i arbetsbok"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, lägg till bakgrundsbild, Excel-API, REST, molntjänst, cURL, arbetsboksbakgrund"
description: "Lär dig hur du lägger till en bakgrundsbild i en Excel-arbetsbok med Aspose.Cells Cloud REST API. Inkluderar nödvändiga parametrar, autentiseringsuppgifter, ett komplett cURL-exempel och information om felhantering."
weight: 160
---

## REST API

Detta REST API lägger till en **bakgrundsbild** till en Excel-arbetsbok.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Frågeparametrar

| Parameternamn  | Typ   | Beskrivning                                              |
| -------------- | ----- | -------------------------------------------------------- |
| `picPath`      | string | Sökväg till den bildfil som ska användas som bakgrund.  |
| `folder`       | string | Mappen som innehåller den ursprungliga arbetsboken.     |
| `storageName`  | string | Namnet på lagringsutrymmet där filen finns.             |

### Parametrar i begärandetexten

| Parameternamn | Typ | Beskrivning                                               |
| ------------- | --- | --------------------------------------------------------- |
| `datafile`    | file | Arbetsboksfilen till vilken bakgrunden ska appliceras.   |

**Sökvägsparameter** – `{name}` i URL:en representerar **arbetsbokens filnamn** (t.ex. `Book1.xlsx`).


### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                 | Beskrivning                                             |
|-----|---------------------------|---------------------------------------------------------|
| 200 | OK                        | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Ogiltig begäran           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad             | Ogiltig eller saknad JWT-token.                         |
| 413 | Payload för stor          | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel         | Oväntat serverfel.                                      |
## Hur du använder PutWorkbookBackground API med SDK:er

### PutWorkbookBackground API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar en komplett begäran, inklusive flaggan för multipart-filuppladdning och den nödvändiga autentiseringshuvudet.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}


### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK abstraher bort detaljer på lågnivå så att du kan koncentrera dig på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}