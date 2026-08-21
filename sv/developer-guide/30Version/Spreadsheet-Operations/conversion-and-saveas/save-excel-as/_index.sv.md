---
title: "Spara Excel-arbetsbok – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Spara som"
type: docs
url: /sv/save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Spara som, PDF, CSV, JSON, Markdown, REST API"
description: "Spara Excel-arbetsböcker till PDF, CSV, JSON, Markdown och andra format med Aspose.Cells Cloud REST API."
weight: 30
---

Detta REST API gör det möjligt att **spara** en Excel-fil i olika format.  
Innan du anropar denna slutpunkt, se till att du har en giltig OAuth 2.0-åtkomsttoken och att källarbetsboken finns lagrad i din Aspose Cloud-lagring.

**Förutsättningar**  
1. Skaffa en JWT-åtkomsttoken och inkludera den i `Authorization: Bearer <token>`-headern för varje begäran.  
2. Ladda upp källarbetsboken till Aspose Cloud-lagring (eller bekräfta att den redan finns).  
3. Känna till lagringens namn och mappsökväg där arbetsboken finns.

## PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Sökvägsparameter**

| Parameternamn | Typ   | Beskrivning                  |
| ------------- | ----- | ---------------------------- |
| name          | string | Namnet på Excel-filen.       |

### **Frågeparameter**

| Parameternamn         | Typ    | Beskrivning                                                                                   |
| --------------------- | ------ | --------------------------------------------------------------------------------------------- |
| newfilename           | string | Nytt filnamn för det sparade dokumentet.                                                      |
| isAutoFitRows         | string | Om `true`, justeras alla rader automatiskt i arbetsboken. Standard är `false`.                |
| isAutoFitColumns      | string | Om `true`, justeras kolumnbredder automatiskt i arbetsboken. Standard är `false`.            |
| folder                | string | Mapp som innehåller den ursprungliga arbetsboken.                                             |
| storageName           | string | Namn på den lagring där källfilen finns.                                                      |
| outStorageName        | string | Namn på den lagring där utdatafilen kommer att sparas.                                        |
| checkExcelRestriction | bool   | Anger om Excel-begränsningar ska tillämpas vid ändring av celler eller relaterade objekt.    |
| region                | string | Regioninställningar som tillämpas på arbetsboken.                                             |
| pageWideFitOnPerSheet | bool   | Anpassa sidbredden till varje kalkylblad vid konvertering.                                   |
| pageTallFitOnPerSheet | bool   | Anpassa sidhöjden till varje kalkylblad vid konvertering.                                    |
| sheetName             | string | Namn på det kalkylblad som ska konverteras.                                                   |
| pageIndex             | string | Sidindex för den sida som ska konverteras inom det angivna kalkylbladet (kräver `sheetName`). |
| onePagePerSheet       | bool   | Skapa en sida per kalkylblad vid konvertering till PDF.                                       |

### **Parameter för begärandetext**

| Parameternamn | Typ   | Beskrivning                                                      |
| ------------- | ----- | ---------------------------------------------------------------- |
| SaveOptions   | Objekt | Sparningsalternativ som anges i den andra delen av multipart-begäran. |

**Exempel på begärandetext (JSON-del av multipart-begäran)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Svar

API:t returnerar ett `SaveResponse`-objekt.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                     |
|-----|-----------------------------|---------------------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer.        |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).               |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token.                                                 |
| 413 | För stor nyttelast          | Den uppladdade filen överskrider storleksgränsen.                              |
| 500 | Internt serverfel           | Oväntat serverfel.                                                              |

## Hur du använder PostWorkbookSaveAs API med SDK:er

### PostWorkbookSaveAs API-specificering

[OpenAPI-specificeringen](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. I exemplet nedan visas hur man anropar Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
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

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

För andra konverteringsscenario, se guiderna [Konvertera Excel till PDF](/convert-excel-to-pdf/) och [Exportera Excel till CSV](/export-excel-to-csv/).