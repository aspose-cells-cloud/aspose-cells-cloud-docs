---
title: "Importera data utan att använda lagring – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Importera data utan lagring"
type: docs
url: /sv/import/without-using-storage/
aliases: [  /sv/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, molntjänst, importera data utan lagring, Excel-import-API, REST-import"
description: "Lär dig hur du importerar data till en Excel-arbetsbok utan att använda lagring med Aspose.Cells Cloud API. Inkluderar begärande format, parametrar, cURL-exempel, SDK-kod och felhantering."
weight: 10
ArticleTitle: "Importera data utan att använda lagring – Aspose.Cells Cloud API"
---

Excel-dataimport kan vara komplex eftersom många faktorer påverkar resultatet. Alla dessa faktorer bör beaktas under **import**-processen. Aspose.Cells Cloud gör det enkelt att importera olika format och datatyper till en Excel-fil med kvalitet på professionellt nivå.

Detta REST-API importerar **data** till en Excel-fil.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar:**

| Parameter_name | Typ           | Plats      | Beskrivning                                                                                                                                      |
| -------------- | ------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| file           | fil           | formData   | Den Excel-fil som ska laddas upp.                                                                                                                |
| ImportOption   | ImportOption  | JSON-body  | JSON-objekt som definierar vilken data som ska importeras, dess typ (t.ex. `IntArray`, `DoubleArray`, `StringArray`) och placering i kalkylbladet. |

**ImportOption**-parametrarna beskrivs i referensen för **ImportData-alternativ** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter).

**Förutsättningar:**  
En giltig JWT-token måste skapas på förhand, och filstorleken får inte överskrida tjänstens gräns (vanligtvis 100 MB). Stödda filformat inkluderar XLS, XLSX, CSV och ODS. Se till att lämpligt SDK är installerat om du föredrar programmatisk åtkomst.

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod  | Betydelse                   | Beskrivning                                                                 |
|------|-----------------------------|-----------------------------------------------------------------------------|
| 200  | OK                          | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).           |
| 401  | Auktorisering saknas        | Ogiltig eller saknad JWT-token.                                             |
| 413  | För stor nyttoinformation   | Den uppladdade filen överskrider storleksgränsen.                          |
| 500  | Internt serverfel           | Oväntat serverfel.                                                          |

**Anteckningar:**  
När du skickar begäran ställs `Content-Type: multipart/form-data` automatiskt in av `-F`-flaggan. För stora nyttolastar kan du överväga att komprimera data innan import och implementera återförsökslogik för tillfälliga fel.

## Hur man använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*`-F`-flaggan ställer automatiskt in `Content-Type: multipart/form-data`.*  

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektrapporter. Se i [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}