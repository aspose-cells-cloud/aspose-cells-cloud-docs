---
title: "Exportera OLE-objekt – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "OLE-objekt"
type: docs
url: /sv/export-excel-ole-object/
aliases: [  /sv/export/excel-ole-object/ ]
keywords: "Aspose.Cells, OLE-objekt, export, Excel, moln-API, PDF, PNG, DOCX, PPTX"
description: "Exportera OLE-objekt från en Excel-arbetsbok med Aspose.Cells Cloud API. Lär dig begäranformat, parametrar, exempel på cURL och felhantering."
weight: 20
ArticleTitle: "Exportera OLE-objekt – Aspose.Cells Cloud API"
---

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begärandeparametrar

| Parameter       | Plats      | Typ   | Obligatorisk | Beskrivning                                                                    |
| --------------- | ---------- | ----- | ------------ | ------------------------------------------------------------------------------ |
| `file`          | Form‑data  | fil   | Ja           | Excel-arbetsboken (`.xlsx`, `.xls`, etc.) som innehåller OLE-objekten.         |
| `outputFormat`  | Frågesträng | sträng | Ja           | Målformat för de exporterade objekten (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Frågesträng | sträng | Ja           | Fast värde `oleobject`.                                                       |


### Svar

En lyckad begäran returnerar ett JSON-objekt som listar de exporterade filerna:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token. |
| 413 | Begärandetext för stor      | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder PostExport API med SDK:er

### PostExport API-specifikation


[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör en anrop till moln-API:et med cURL.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### Vad är ett OLE-objekt?

Ett **OLE-objekt** (Object Linking and Embedding) bäddar in externt innehåll—t.ex. Word-dokument, PowerPoint-bildspel, bilder eller andra filer—inuti en Excel-arbetsbok. Vid export extraheras det inbäddade innehållet och sparas i det begärda utdataformatet.

### Översikt över slutpunkten

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – Måste ställas in till `oleobject`.
- `format` – Önskat utdataformat (t.ex. `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---