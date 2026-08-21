---
title: "Excel till Docx"
second_title: "Dokument"
linktitle: "Excel till Docx"
type: docs
url: convert-excel-file-to-docx-file/
keywords: "konvertering av Excel till Docx, Aspose.Cells Cloud, REST API, konvertering av kalkylark, dokumentgenerering"
description: "Konvertera Excel-kalkylark till DOCX-dokument med Aspose.Cells Cloud REST API. Stöder flera SDK:er och programmeringsspråk för sömlös integration."
weight: 90
---

Detta REST API konverterar en kalkylarkfil till DOCX-format.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.



**Frågeparametrar**

| Parameter Name        | Typ    | Beskrivning                                                                                           |
| --------------------- | ------ | ----------------------------------------------------------------------------------------------------- |
| password              | sträng | Lösenordet som krävs för att öppna Excel-filen.                                                      |
| storageName           | sträng | Namnet på lagringen där filen finns.                                                                 |
| checkExcelRestriction | bool   | Anger om restriktioner för Excel-filen ska kontrolleras när användaren redigerar cellrelaterade objekt. |

**Parametrar för begärandetext**

| Parameter Name | Typ       | Beskrivning                                                     |
| -------------- | --------- | --------------------------------------------------------------- |
| datafile       | datafil   | Datafilen som sparas i den första delen av begärandetexten.     |

**Svar**

API:et returnerar ett **FileInfo**-objekt som innehåller den genererade Word-filen.

| Fält            | Typ    | Beskrivning                                    |
| --------------- | ------ | ---------------------------------------------- |
| **Filename**    | sträng | Namn på Word-filen (t.ex. `exempel.docx`).     |
| **FileSize**    | int    | Filens storlek i byte.                         |
| **FileContent** | sträng | Base64-kodat innehåll i Word-filen.            |


[FileInfo](/cells/file-info/)

**HTTP-statuskoder**

| Kod | Betyder                     | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

## Hur man använder PostConvertWorkbookToDocx API med SDK:er

### PostConvertWorkbookToDocx API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "exempel.docx",
  "FileSize": 12345,
  "FileContent": "Filinnehåll: base64_kodad_sträng"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API:er som implementerar denna funktion

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Sparar en Excel-fil som DOCX-fil med ytterligare inställningar och lagrar resultatet i den angivna lagringen.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konverterar en Excel-fil till DOCX-fil med valfria inställningar och returnerar resultatet i svaret.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Hämtar ett Excel-arbetsboksdokument och konverterar det till DOCX-fil med valfria parametrar.

---