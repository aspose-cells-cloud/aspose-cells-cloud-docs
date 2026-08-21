---
title: "Excel till JSON"
second_title: "Dokument"
linktitle: "Excel till JSON"
type: docs
url: /sv/convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel till JSON, molntjänst, kalkylbladskonvertering, REST API"
description: "Lär dig hur du konverterar Excel-kalkylblad till JSON-filer med Aspose.Cells Cloud REST API. Innehåller cURL-exempel, SDK-snuttar (C#, Java, Python), nödvändiga parametrar, autentisering och svarsformat."
weight: 100
ArticleTitle: "Konvertera Excel till JSON med Aspose.Cells Cloud API – Snabbhandbok"
---


## REST API

Detta REST API konverterar en kalkylbladsfil till en JSON-formaterad fil.  


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Säkerhet och autentisering

Aspose.Cells Cloud API:n är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Begäran

**Frågeparametrar**

| Parameter namn          | Typ    | Beskrivning                                                          |
| ----------------------- | ------ | -------------------------------------------------------------------- |
| `password`              | sträng | Lösenord som krävs för att öppna Excel-filen (valfritt).             |
| `storageName`           | sträng | Namn på lagringen där filen finns (valfritt).                        |
| `checkExcelRestriction` | bool   | Tvingar Excel-specifika restriktioner vid redigering av celler (valfritt). |

**Begärans brödtextparameter**

| Parameter namn | Typ  | Beskrivning                                                                                   |
| -------------- | ---- | --------------------------------------------------------------------------------------------- |
| `datafile`     | fil  | Den Excel-fil som ska laddas upp. Måste skickas som första del i en `multipart/form-data`-begäran. |

#### Exempel på cURL-anrop

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Svar

Tjänsten returnerar ett **FileInfo**-objekt. De viktiga fälten beskrivs nedan:

| Fält          | Typ    | Beskrivning                                                                 |
| ------------- | ------ | --------------------------------------------------------------------------- |
| `Filename`    | sträng | Namn på den genererade JSON-filen (t.ex. `myWorkbook.json`).                |
| `FileSize`    | heltal | Storlek på den genererade filen i byte.                                     |
| `FileContent` | sträng | Base64-kodat innehåll i JSON-filen. Dekod för att hämta faktiskt JSON.     |

**Exempel på svar**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64-sträng) ..."
}
```

#### Felhantering

Om begäran misslyckas returnerar API:t ett felobjekt med följande struktur:

| Fält      | Typ   | Beskrivning                              |
| --------- | ----- | ---------------------------------------- |
| `Code`    | sträng | Maskinläsbar felidentifierare.           |
| `Message` | sträng | Mänsklig läsbar beskrivning av felet.    |

Vanliga HTTP-statuskoder:

- **400** – Dålig begäran (t.ex. saknad fil, ogiltiga parametrar).
- **401** – Ej auktoriserad (ogiltig eller saknad åtkomsttoken).
- **500** – Internt serverfel.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                             |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Dålig begäran               | Saknas eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad             | Ogiltig eller saknad JWT-token.                         |
| 413 | Payload för stor            | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel           | Oväntat serverfel.                                      |

## Hur du använder PostConvertWorkbookToJson API med SDK:er

### PostConvertWorkbookToJson API-specifikation

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI-specifikation – Konvertera arbetsbok till JSON">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64-sträng)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="Aspose.Cells Cloud SDK:er på GitHub">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API:er som implementerar liknande funktionalitet

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Sparar en Excel-fil som en HTML-fil med ytterligare inställningar och lagrar resultatet i den angivna lagringen.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konverterar en Excel-fil till en HTML-fil med ytterligare inställningar och returnerar resultatet i svaret.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Hämtar en Excel-fil; kan användas med frågeparametrar för att få filen i HTML-format.
---