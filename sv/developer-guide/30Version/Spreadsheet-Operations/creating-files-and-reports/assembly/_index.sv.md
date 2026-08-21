---
title: "Sammanställning av data för skapande av en Excel-rapport"
second_title: "Dokument"
linktitle: "Sammanställningsdata"
type: docs
url: /sv/assembly-data-for-the-creation-of-an-excel-report/
aliases: [  /sv/assembly/ ]
keywords: "Aspose.Cells, Excel-rapport, dataassemblage, molntjänst-API, REST, SDK, cURL, PDF, ODS"
description: "Lär dig hur du använder Aspose.Cells Cloud:s Assembly API för att sammanfoga data till Excel-rapporter (XLSX, PDF, ODS). Innehåller slutpunkt, parametrar, cURL-exempel, SDK-kod, autentiseringsguide och felhantering."
weight: 40
---

Detta REST API sammanställer data **till** en Excel-fil.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärans parametrar


| Parameter namn | Typ    | Plats                     | Beskrivning                                                           |
| -------------- | ------ | ------------------------- | --------------------------------------------------------------------- |
| file           | fil    | formData (multipart body) | Kalkylarkfilen som ska laddas upp.                                    |
| DataSource     | sträng | frågesträng               | Identifierare för datakällan som tillhandahåller data för sammanställningen. |
| format         | sträng | frågesträng               | Önskat utdataformat (t.ex. `xlsx`, `pdf`).                            |

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[fil2 namn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                         |
|-----|-----------------------------|-----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token. |
| 413 | För stor nytolast           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder PostAssemble API med SDK:er

### PostAssemble API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "report1",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    },
    {
      "Filename": "report2",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att utveckla mot API:et. Ett SDK abstraher bort detaljer på lågnivånivå och låter dig fokusera på din affärslogik. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}