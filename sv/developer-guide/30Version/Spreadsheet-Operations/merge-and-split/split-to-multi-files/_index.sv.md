---
title: "Dela en Excel-fil i flera filer"
second_title: "Dokument"
linktitle: "Dela flera Excel-filer"
type: docs
url: /split-an-excel-file-to-multi-files/
aliases: [/split-excel-workbooks/,/workbook/split/]
keywords: "Aspose.Cells, moln, Excel, Dela, API, PDF, CSV, JSON"
description: "Använd Aspose.Cells Cloud REST API för att dela flersidiga Excel-arbetsböcker i separata filer. Stöder utdataformat som PDF, CSV och JSON, och är tillgängligt via SDK:er för Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift."
weight: 32
ArticleTitle: "Dela en Excel-fil i flera filer - Aspose.Cells Cloud-dokumentation"
---

Aspose.Cells Cloud REST API delar flersidiga Excel-arbetsböcker i separata filer.

**Förutsättningar**  
Innan du anropar API:et måste du skaffa en giltig JWT-token och inkludera den i `Authorization`-headern i varje begäran. Se [autentiseringshandboken](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) för detaljer.

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameternamn | Typ   | Plats     | Beskrivning                                                    |
|---------------|-------|-----------|----------------------------------------------------------------|
| file          | fil   | formData  | Den Excel-arbetsbok som ska laddas upp.                        |
| format        | sträng| query     | Önskat utdataformat (t.ex. `pdf`, `csv`, `json`).              |
| password      | sträng| query     | Lösenord för en krypterad arbetsbok (valfritt).                |
| from          | heltal| query     | Index för första ark som ska inkluderas (1-baserat).           |
| to            | heltal| query     | Index för sista ark som ska inkluderas (inklusive).           |

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
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

| Kod | Betydelse                   | Beskrivning                                                   |
|-----|-----------------------------|---------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                               |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.             |
| 500 | Internt serverfel           | Oväntat serverfel inträffade.                                  |

## Hur du använder PostSplit API med SDK:er

### PostSplit API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

**HTTP-statuskoder**

| Kod | Betydelse                     | Beskrivning                                                    |
|-----|-------------------------------|----------------------------------------------------------------|
| 200 | OK                            | Arbetsboken delades framgångsrikt och svaret innehåller fillistan. |
| 400 | Felaktig begäran              | Saknade eller ogiltiga parametrar (t.ex. format som inte stöds). |
| 401 | Obehörig                      | Ogiltig eller saknad JWT-token.                                |
| 500 | Internt serverfel             | Ett oväntat fel inträffade på serversidan.                     |

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# Ersätt xxxxx1.xlsx och xxxxx2.xlsx med sökvägarna till dina Excel-filer
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64-sträng--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64-sträng--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}