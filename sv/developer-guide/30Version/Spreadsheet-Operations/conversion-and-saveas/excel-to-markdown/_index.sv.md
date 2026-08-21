---
title: "Konvertera Excel till Markdown"
second_title: "Dokument"
linktitle: "Excel till Markdown"
type: docs
url: /sv/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, konvertering, Aspose.Cells Cloud, REST API, konvertering av Excel till Markdown, Aspose Cells Markdown API, export av Excel till Markdown"
description: "Konvertera Excel-ark till Markdown med Aspose.Cells Cloud REST API – inkluderar cURL-exempel, SDK-utdrag, obligatoriska parametrar och autentiseringsinformation."
weight: 100
ArticleTitle: "Konvertera Excel till Markdown – Aspose.Cells Cloud API-dokumentation"
---

Denna REST API konverterar en kalkylarksfil till en fil i Markdown-format.

## Säkerhet och autentisering
Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Frågeparametrar


| Parameternamn         | Typ    | Plats   | Beskrivning                                                                                      |
| --------------------- | ------ | ------- | ------------------------------------------------------------------------------------------------ |
| password              | string | query   | Lösenord som krävs för att öppna Excel-filen.                                                    |
| storageName           | string | query   | Namn på lagringsplatsen där filen finns.                                                         |
| checkExcelRestriction | bool   | query   | Anger om Excel-specifika restriktioner ska tillämpas vid ändring av celler eller relaterade objekt. |
| datafile              | file   | body    | Excel-filen som ska laddas upp som första del av innehållet i multipart-formatet.              |

### Respons

API:et returnerar ett JSON-objekt av typen **FileInfo**:

- **FileInfo** – objekt som innehåller namn, storlek och base64-kodat innehåll i den genererade Markdown-filen.

```json
{
  "Filename": "exempel.md",
  "FileSize": 12345,
  "FileContent": "base64_kodad_sträng"
}
```

### Felrespons

| HTTP-kod | Beskrivning                                                       | Exempel på JSON-kropp                        |
| -------- | ----------------------------------------------------------------- | -------------------------------------------- |
| 401      | Otillåten – saknat eller ogiltigt token.                         | `{"error":"Ogiltig åtkomsttoken."}`         |
| 400      | Felaktig begäran – saknade obligatoriska parametrar eller ogiltigt filformat. | `{"error":"Fältet 'datafile' krävs."}` |
| 500      | Internt serverfel – oväntat serverproblem.                        | `{"error":"Ett oväntat fel uppstod."}`       |



## Hur du använder PostConvertWorkbookToMarkdown API med SDK:er

### PostConvertWorkbookToMarkdown API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Exemplet nedan visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Respons" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@din_excel_fil.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exempel.md",
  "FileSize": 12345,
  "FileContent": "base64_kodad_sträng"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på lågnivå så att du kan fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API:er som implementerar denna funktion

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Sparar en Excel-fil som HTML med ytterligare inställningar och lagrar resultatet.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konverterar en Excel-fil till HTML med extra alternativ och returnerar resultatet i svaret.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Hämtar en Excel-fil och kan konvertera den till HTML med valfria inställningar.
---