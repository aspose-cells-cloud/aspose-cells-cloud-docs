---
title: "Konvertera Excel till PDF – Aspose.Cells Cloud API"
ArticleTitle: "Konvertera Excel till PDF – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Konvertera Excel till PDF"
type: docs
url: /sv/convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, konvertering, molntjänst-API"
description: "Lär dig hur du konverterar Excel-arbetsböcker till PDF med Aspose.Cells Cloud REST API. Innehåller cURL- och SDK-exempel (C#, Java, Python) samt en guidad översikt över autentisering."
weight: 80
---

Detta REST-API konverterar en kalkylarkfil till en PDF-fil. **Förutsättningar:** Du behöver en giltig JWT-åtkomsttoken, käll-Excel-filen måste finnas lagrad i ett stöddat lagringsutrymme, och du måste ha rätt behörigheter för att anropa konverteringsändpunkten.

## API för PostConvertWorkbookToPDF

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Frågeparameter**

| Parameter namn        | Typ    | Beskrivning                                                                 |
| :-------------------- | :----- | :--------------------------------------------------------------------------- |
| password              | string | Lösenord för att öppna Excel-filen.                                          |
| storageName           | string | Namnet på det lagringsutrymme där filen finns.                               |
| checkExcelRestriction | bool   | Huruvida Excel-filens begränsningar ska tillämpas vid ändring av cellobjekt. |

`checkExcelRestriction` är standardvärdet `false` om parametern utelämnas.

### **Parameter för begärandetext**

| Parameter namn | Typ  | Beskrivning                                                       |
| :------------- | :--- | :---------------------------------------------------------------- |
| datafile       | fil  | Datafilen som sparas som första del av innehållet i multipart-formatet. |

### **Svar**

[FileInfo](/sv/cells/file-info/)

Svaret returnerar ett JSON-objekt med filmetadata. PDF-filen själv kan laddas ner via den angivna `FileContent` (base64-kodad sträng) eller via länken i `FileInfo`. API:t returnerar ett JSON-objekt av typen **FileInfo**:

- **FileInfo** – objekt som innehåller namn, storlek och base64-kodat innehåll för den genererade **PDF**-filen.

```json
{
  "Filename": "exempel.pdf",
  "FileSize": 12345,
  "FileContent": "base64_kodad_sträng"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad             | Ogiltig eller saknad JWT-token.                            |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.          |
| 500 | Internt serverfel           | Oväntat serverfel.                                         |

## Hur du använder API:t PostConvertWorkbookToPDF med SDK:n

### API-specifikation för PostConvertWorkbookToPDF

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

**Begärandehuvuden**

| Huvud            | Typ    | Beskrivning                                                |
| :--------------- | :----- | :--------------------------------------------------------- |
| Authorization    | string | Bearer-token som erhållits via JWT-autentisering.          |
| Content-Type     | string | Måste vara `multipart/form-data` för filuppladdning.      |
| Accept           | string | `application/json` för att ta emot svarsmetadata.         |

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Inkludera en åtkomsttoken i `Authorization`-huvudet och kör sedan följande begäran.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_kodad_sträng"
}
```

{{< /tab >}}

{{< /tabs >}}


### Använd Aspose.Cells Cloud SDK:n

Att använda ett SDK kan förenkla utvecklingen genom att hantera detaljer på låg nivå. Ta en titt på [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Andra API som implementerar denna funktion

| **API**        | **Typ** | **Beskrivning**                                                 | **Swagger-länk**                                                                            |
| :------------- | :------ | :-------------------------------------------------------------- | :------------------------------------------------------------------------------------------ |
| /cells/convert | PUT     | Konverterar en arbetsbok från begärandetexten till ett angivet format. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API låter dig spara en MS Excel-fil som PDF med ytterligare inställningar och lagra resultatet i lagringen.

Detta REST API konverterar en Excel-fil till PDF.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API låter dig konvertera en MS Excel-fil till PDF med ytterligare inställningar och returnera resultatet i svaret.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API låter dig konvertera en MS Excel-fil till PDF med ytterligare inställningar och returnera resultatet i svaret.

Dessa API:n [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) och [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

För ytterligare konverteringsalternativ, se sidan [Save Options](/sv/save-options/).