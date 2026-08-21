---
title: "Importera tvådimensionellt heltalsfält till Excel-ark"
second_title: "Dokument"
linktype: "Importera tvådimensionellt heltalsfält"
type: docs
url: /import-a-2d-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, importera 2D-heltalsfält, Excel-ark, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "Aspose.Cells Cloud REST API möjliggör import av tvådimensionella heltalsfält till Excel-ark. SDK:er finns tillgängliga för Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift."
weight: 20
---

Denna REST API **importerar ett tvådimensionellt heltalsfält** till ett Excel-ark.

Förfrågan är en HTTP-förfrågan med multipart-innehåll (se [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av multipart-innehållet innehåller `Import2DimensionIntegerArrayOption`-data och den andra delen innehåller datafilen.

De viktiga parametrarna beskrivs i följande tabell:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Import2DimensionIntegerArrayOption**

| Parameter Name       | Typ        | Beskrivning                                                                                                                                                                                  |
| -------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | 1-baserat index för den första raden dit data placeras.                                                                                                                                      |
| FirstColumn          | int        | 1-baserat index för den första kolumnen dit data placeras.                                                                                                                                   |
| Data                 | Integer[,] | Tvådimensionellt heltalsfält som innehåller värdena som ska importeras.                                                                                                                      |
| DestinationWorksheet | string     | Namn på målarket.                                                                                                                                                                             |
| IsInsert             | string     | `"true"` för att infoga data (skjuta befintliga celler), `"false"` för att skriva över befintliga celler.                                                                                   |
| ImportDataType       | string     | Anger dataformatet. Stödda värden: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`.        |
| Source               | FileSource | Anger datafilens plats när `BatchData`-parametern är `null`.                                                                                                                                 |

### **Exempel**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
}
```

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|-----------------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400 | Felaktig förfrågan          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).           |
| 401 | Autentisering krävs         | Ogiltig eller saknad JWT-token.                                             |
| 413 | För stor nyttolast          | Uppladdad fil överskrider storleksgränsen.                                  |
| 500 | Internt serverfel           | Oväntat serverfel.                                                          |

## Hur man använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt som låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Besök [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}