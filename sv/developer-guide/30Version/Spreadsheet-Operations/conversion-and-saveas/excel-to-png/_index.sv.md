---
title: "Excel till PNG"
second_title: "Dokument"
linktitle: "Excel till PNG"
type: docs
url: /sv/svconvert-excel-file-to-png-file/
keywords: "Excel till PNG, Aspose.Cells Cloud, REST API, kalkylbladskonvertering, PNG-format"
description: "Konvertera Excel-kalkylblad till PNG-bilder med Aspose.Cells Cloud REST API. Stöder flera SDK:er och tillhandahåller detaljerade exempel för olika programmeringsspråk."
weight: 90
---

Denna REST API konverterar ett kalkylbladsfil till PNG-format.

## REST API-specifikation

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Frågeparameter**

| Parametername         | Typ    | Beskrivning                                                                                   |
| --------------------- | ------ | --------------------------------------------------------------------------------------------- |
| password              | string | Lösenordet som krävs för att öppna Excel-filen.                                               |
| storageName           | string | Namnet på lagringsplatsen där filen finns.                                                    |
| checkExcelRestriction | bool   | Avgör om Excel-filbegränsningar ska kontrolleras vid ändring av celler eller relaterade objekt. |

### **Parameter för begärandetext**

| Parametername | Typ       | Beskrivning                                                            |
| ------------- | --------- | ---------------------------------------------------------------------- |
| datafile      | datafil   | Kalkylbladsfilen som ingår i första delen av multipart-begäran.       |

### **Svar**

API:et returnerar ett **FileInfo**-objekt som innehåller den genererade PNG-filen.

| Fält            | Typ    | Beskrivning                                   |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | Namn på PNG-filen (t.ex. `exempel.png`).      |
| **FileSize**    | int    | Filens storlek i byte.                        |
| **FileContent** | string | Base64-kodat innehåll i PNG-filen.            |

[FileInfo](/cells/file-info/)


**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                            |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller operationsdetaljer. |
| 400 | Ogiltig begäran             | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token.                        |
| 413 | För stor nyttolast          | Uppladdad fil överskrider storleksbegränsningen.      |
| 500 | Internt serverfel           | Oväntat serverfel.                                     |

## Hur man använder PostConvertWorkbookToPNG API med SDK:er

### PostConvertWorkbookToPNG API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "Filinnehåll: base64_kodad_sträng"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API:er som implementerar liknande funktioner

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Sparar en Excel-fil som CSV (eller andra format) med ytterligare inställningar och lagrar resultatet.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Konverterar en Excel-fil till CSV (eller andra format) med valfria parametrar och returnerar resultatet i svaret.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Hämtar en Excel-fil och kan konvertera den till CSV (eller andra format) på begäran.

---