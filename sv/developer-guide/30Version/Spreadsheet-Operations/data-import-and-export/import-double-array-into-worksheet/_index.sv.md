---
title: "Importera dubbelarray till Excel-arket"
second_title: "Dokument"
linktitle: "Importera dubbelarray"
type: docs
url: /import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, importera dubbelarray, Excel-API, moln-SDK"
description: "Lär dig hur du importerar en dubbelarray till ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller autentisering, begäranformat, parametrar, exempel på XML/JSON och detaljerad svarsinformation."
weight: 20
ArticleTitle: "Importera dubbelarray till Excel-ark – Aspose.Cells Cloud-guide"
---

Denna REST API **importerar dubbelarraydata** till ett Excel-ark.

> **Förutsättningar:** Du måste ha ett giltigt JWT-token innan du anropar detta API. Se autentiseringsguiden för mer information.

Du skickar en HTTP-begäran med **multipart**-innehåll (se [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Den första delen av multipart-kroppen innehåller **ImportDoubleArrayOption**-data och den andra delen innehåller datafilen.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

#### **ImportDoubleArrayOption**

| Parameter Name       | Typ        | Beskrivning                                                                                               |
| -------------------- | ---------- | --------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Nullbaserat index för den första raden där data ska placeras.                                            |
| FirstColumn          | int        | Nullbaserat index för den första kolumnen där data ska placeras.                                         |
| IsVertical           | boolean    | `true` / `false` – anger om arrayen infogas vertikalt (`true`) eller horisontellt (`false`).             |
| Data                 | Double[]   | Array med dubbelvärden som ska importeras.                                                               |
| DestinationWorksheet | string     | Namn på målarket.                                                                                         |
| IsInsert             | boolean    | `true` / `false` – om `true`, infogas data; om `false`, skrivs befintliga celler över.                   |
| ImportDataType       | string     | Typ av data som importeras (t.ex. `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`).     |
| Source               | FileSource | Anger datafilens plats när parametern `BatchData` är null.                                                |

#### Exempel (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Blad1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Exempel (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Blad1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
```

### Svar

En lyckad begäran returnerar **HTTP 200** med ett JSON-svar på följande form:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Möjliga statuskoder:

| Kod | Betydelse                                    |
| --- | -------------------------------------------- |
| 200 | Importen lyckades                            |
| 400 | Felaktig begäran – saknad eller ogiltig data |
| 401 | Autentisering misslyckades – ogiltigt eller saknat token |
| 500 | Internt serverfel                            |

### Felhantering

När ett fel uppstår returnerar API:t ett JSON-objekt som innehåller felkod och en beskrivande meddelandetext. Exempel för en oauktoriserad begäran:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

För mer information om relaterade importåtgärder, se dokumentationssidorna för “Importera 2-dimensionell dubbelarray” och “Importera heltalsarray”.

## Hur du använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Ta en titt på [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}