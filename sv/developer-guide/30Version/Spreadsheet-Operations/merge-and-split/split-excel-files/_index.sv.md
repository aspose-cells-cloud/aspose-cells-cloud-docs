---
title: "Dela en Excel-arbetsbok i flera filer"
ArticleTitle: "Hur man delar en Excel-arbetsbok i flera filer med Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Dela en Excel-fil"
type: docs
url: /sv/split-multi-excel-files/
aliases: [  /sv/split/multi-files/ ]
keywords: "Excel, Aspose.Cells Cloud, REST API, dela arbetsbok, flera filer, JPEG, PNG, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API möjliggör delning av en Excel-arbetsbok i flera filer i olika format. Denna dokumentation tillhandahåller begärparametrar, ett cURL-exempel och SDK-kodexempel för språk som C#, Java, PHP, Ruby, Node.js, Python, Perl och Go."
weight: 130
---

Denna REST API delar en Excel-**arbetsbok** i flera filer i olika format.

> **Förutsättningar** – För att använda denna API måste du erhålla en giltig JWT-token, säkerställa att du använder en SDK-version som stöds och verifiera att din arbetsbok lagras på en lagringsplats som stöds. API:t tillämpar även filstorleksbegränsningar som dokumenteras i plattformens riktlinjer.

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameter namn       | Typ     | Plats     | Beskrivning                                                                                     | Obligatoriskt |
| -------------------- | ------- | --------- | ----------------------------------------------------------------------------------------------- | ------------- |
| files[]              | fil     | formData  | En eller flera Excel-arbetsböcker som ska **delas**. Använd `file1`, `file2`, … i begäran.     | Ja            |
| format               | sträng  | Query     | Önskat utdataformat för de delade filerna.                                                     | Nej           |
| from                 | heltal  | Query     | Startindex för kalkylblad.                                                                     | Nej           |
| to                   | heltal  | Query     | Slutindex för kalkylblad.                                                                      | Nej           |
| horizontalResolution | heltal  | Query     | Horisontell bildupplösning.                                                                     | Nej           |
| verticalResolution   | heltal  | Query     | Vertikal bildupplösning.                                                                        | Nej           |
| outFolder            | sträng  | Query     | Utdatamapp för de delade filerna.                                                               | Nej           |
| splitNameRule        | sträng  | Query     | Namngivningsregel som tillämpas på delade filer.                                               | Nej           |
| folder               | sträng  | Query     | Mapp som innehåller den ursprungliga arbetsboken.                                               | Nej           |
| storageName          | sträng  | Query     | Namn på den lagring som ska användas.                                                           | Nej           |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[fil1 namn]",
        "Filesize" : [filstorlek],
        "FileContent" : "[Base64-sträng]"
      },
      {
        "Filename" : "[fil2 namn]",
        "Filesize" : [filstorlek],
        "FileContent" : "[Base64-sträng]"
      },
      {
        "Filename" : "[fil3 namn]",
        "Filesize" : [filstorlek],
        "FileContent" : "[Base64-sträng]"
      }
    ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad               | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksbegränsningen. |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

## Hur man använder PostWorkbookSplit API med SDK:er

### PostWorkbookSplit API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---