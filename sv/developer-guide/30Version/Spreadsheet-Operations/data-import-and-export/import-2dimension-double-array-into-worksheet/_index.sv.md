---
title: "Importera 2‑dimensionellt dubbelarray till Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Importera 2‑dimensionellt dubbelarray"
type: docs
url: /import-a-2D-double-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-double-array-into-excel-worksheet/,
    /import-2dimension-double-array-into-worksheet/,
    /import-data/2dimension-double-array/,
    /import/2dimension-double-array/,
  ]
keywords: "Importera 2‑dimensionellt dubbelarray, Excel, Aspose Cells Cloud, REST API, Kalkylark, Dataimport"
description: "Lär dig hur du importerar ett tvådimensionellt dubbelarray till ett Excel-arbetsblad med Aspose.Cells Cloud REST API. Inkluderar begärandeformat, parametrar och SDK-kodexempel."
weight: 20
---

Denna REST API **importerar ett tvådimensionellt dubbelarray** till ett Excel-arbetsblad.

Begäran är en HTTP `POST` med multipart-innehåll (se [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av multipart-brödtexten innehåller data för **Import2DimensionDoubleArrayOption**, och den andra delen innehåller källfilen med data.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

De viktiga parametrarna beskrivs i följande tabell:

### Import2DimensionDoubleArrayOption

| Parameter Name           | Typ          | Beskrivning                                                                                                              |
| ------------------------ | ------------ | ------------------------------------------------------------------------------------------------------------------------ |
| **FirstRow**             | `int`        | Radindex (1‑baserat) där importen börjar.                                                                                |
| **FirstColumn**          | `int`        | Kolumnindex (1‑baserat) där importen börjar.                                                                             |
| **Data**                 | `Double[,]`  | Tvådimensionellt fält med dubbelvärden som ska importeras.                                                               |
| **DestinationWorksheet** | `string`     | Namn på arbetsbladet som ska ta emot data.                                                                                |
| **IsInsert**             | `string`     | `"true"` för att infoga rader, `"false"` för att skriva över befintliga celler.                                          |
| **ImportDataType**       | `string`     | Typ av data som importeras (t.ex. `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, etc.). |
| **Source**               | `FileSource` | Anger platsen för datafilen när parametern `BatchData` är null.                                                          |

**Exempel**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### Respons

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdsdetaljer.      |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).           |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                                            |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.                          |
| 500 | Internal Server Error       | Oväntat serverfel.                                                         |

## Hur man använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att integrera denna funktionalitet. SDK:er hanterar detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}