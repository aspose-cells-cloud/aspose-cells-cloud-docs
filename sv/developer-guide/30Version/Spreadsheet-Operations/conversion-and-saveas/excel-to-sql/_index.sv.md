---
title: "Excel till SQL"
second_title: "Dokument"
linktitle: "Excel till SQL"
type: docs
url: /convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel till SQL, moln-API, kalkylbladkonvertering, REST"
description: "Använd Aspose.Cells Cloud REST API för att konvertera Excel-kalkylblad till SQL-filer. Stöder flera SDK:er och programmeringsspråk för en sömlös integration i dina program."
weight: 100
ArticleTitle: "Konvertera Excel till SQL – Aspose.Cells Cloud API"
---

Detta REST API konverterar en kalkylbladsfil till ett SQL-format.

**Förutsättningar**  
För att använda detta slutställe måste du ha ett giltigt JWT-token genererat enligt beskrivningen i <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>-guide. API:et stöder Excel-filer upp till storleksgränserna som definieras i service dokumentationen och kan hantera lösenordsskyddade arbetsböcker när `password`-frågeparametern tillhandahålls.

## PostConvertWorkbookToSQL API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Frågeparameter**

| Parameternamn         | Typ    | Beskrivning                                                                 |
| --------------------- | ------ | --------------------------------------------------------------------------- |
| password              | string | Lösenord som krävs för att öppna Excel-filen.                               |
| storageName           | string | Namn på lagringsplatsen där filen är lagrad.                                 |
| checkExcelRestriction | bool   | Anger om Excel-filrestriktioner ska kontrolleras vid ändring av cellrelaterade objekt. |

### **Parametrar i begärandetexten**

| Parameternamn | Typ       | Beskrivning                                                           |
| ------------- | --------- | --------------------------------------------------------------------- |
| datafile      | datafil   | Kalkylbladsfilen som ska konverteras, inkluderad som den första delen av begäran. |

### Svar

API:et returnerar ett **FileInfo**-objekt som innehåller den genererade SQL-filen.

| Fält            | Typ    | Beskrivning                                |
| --------------- | ------ | ------------------------------------------ |
| **Filename**    | string | Namn på SQL-filen (t.ex. `example.sql`).  |
| **FileSize**    | int    | Filens storlek i byte.                     |
| **FileContent** | string | Base64-kodat innehåll i SQL-filen.        |

[FileInfo](/cells/file-info/)

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                   |
|-----|-----------------------------|---------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig                    | Ogiltigt eller saknat JWT-token.                             |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.            |
| 500 | Internt serverfel           | Oväntat serverfel.                                           |

## Hur du använder PostConvertWorkbookToSQL API med SDK:er

### PostConvertWorkbookToSQL API-specifikation

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_kodad_sträng"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API som implementerar denna funktion

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Sparar en arbetsbok i ett annat format och lagrar resultatet i den angivna lagringsplatsen.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konverterar en arbetsbok till ett annat format med valfria inställningar och returnerar resultatet i svaret.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Hämtar en arbetsbok med valfria konverteringsinställningar.

**Anteckningar**  
- När du konverterar lösenordsskyddade Excel-filer, se till att `password`-frågeparametern tillhandahålls; annars kommer konverteringen att misslyckas med ett 400-fel.  
- Tjänsten returnerar SQL-filens innehåll som Base64; avkoda det innan du sparar till en `.sql`-fil.  

**Exempelfiler**  
Ladda ner en exempelarbetsbok i Excel-format [här](https://example.com/sample.xlsx) och ett förgenererat SQL-resultat [här](https://example.com/sample.sql) för snabbt att testa API:et.  
---