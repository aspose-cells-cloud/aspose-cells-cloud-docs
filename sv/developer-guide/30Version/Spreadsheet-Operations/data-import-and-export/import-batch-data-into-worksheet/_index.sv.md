---
title: "Importera batchdata till Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Importera batchdata"
type: docs
url: /import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, moln-API, importera batchdata, Excel, CSV, JSON, XML, arrayer"
description: "Lär dig hur du importerar batchdata (CSV, JSON, XML, arrayer) till ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Inkluderar autentisering, exempel på begäran/svar, SDK-utdrag och felhantering."
weight: 19
ArticleTitle: "Importera batchdata till Excel-arbetsblad – Aspose.Cells Cloud-dokumentation"
---

Detta REST-API **importerar batchdata** till ett Excel-arbetsblad. Det tar emot en multipart-begäran där den första delen innehåller objektet **ImportBatchDataOption** och den andra delen innehåller den faktiska datafilen (CSV, JSON, XML, etc.).

Operationen använder en HTTP-begäran med multipart-innehåll (se [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### ImportBatchDataOption

| Parameter namn           | Typ               | Beskrivning                                                                                                                                                                                  |
| ------------------------ | ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | Samling av cellvärden som ska skrivas direkt.                                                                                                                                                |
| **DestinationWorksheet** | `string`          | Namn på arbetsbladet dit data ska importeras.                                                                                                                                                |
| **IsInsert**             | `bool`            | När `true` infogas data och befintliga celler skjuts åt sidan; när `false` skriver data över befintliga celler.                                                                              |
| **ImportDataType**       | `string`          | Format på den data som ska importeras. Tillåtna värden: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | `FileSource`      | Anger platsen för datafilen när **BatchData** är `null`.                                                                                                                                     |

### CellValue

| Parameter namn  | Typ      | Beskrivning                                              |
| --------------- | -------- | -------------------------------------------------------- |
| **rowIndex**    | `int`    | Nollbaserat radindex för målcellen.                      |
| **columnIndex** | `int`    | Nollbaserat kolumnindex för målcellen.                   |
| **type**        | `string` | Datatyp för värdet (t.ex. `int`, `double`, `string`).    |
| **value**       | `string` | Det faktiska värdet som ska skrivas i cellen.            |
| **style**       | `Style`  | Valfri stilinformation för cellen.                       |

### FileSource

| Parameter namn     | Typ      | Beskrivning                                                          |
| ------------------ | -------- | -------------------------------------------------------------------- |
| **FileSourceType** | `string` | Källa för filen: `InMemoryFiles`, `CloudFileSystem` eller `RequestFiles`. |
| **FilePath**       | `string` | Sökväg eller identifierare för filen inom den valda källan.         |

### Exempel (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Ark1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                   |
|-----|-----------------------------|---------------------------------------------------------------|
| 200 | OK                          | Filter har tillämpats framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token.                               |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.             |
| 500 | Internt serverfel           | Oväntat serverfel.                                            |

## Hur du använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att integrera den här funktionen. SDK:er hanterar detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}