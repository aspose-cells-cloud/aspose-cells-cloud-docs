---
title: "Importera strängarray till Excel-arbetsblad – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Importera strängarray"
type: docs
url: /sv/import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, importera strängarray, Excel REST API, multipart-uppladdning, import av arbetsbladsdata, moln-SDK"
description: "Lär dig hur du importerar en strängarray till ett Excel-arbetsblad med Aspose.Cells Cloud REST API (v3.0). Inkluderar begärandeformat, parametrar och SDK-exempel."
weight: 40
ArticleTitle: "Importera strängarray till Excel-arbetsblad – Aspose.Cells Cloud"
---

Att importera en strängarray till ett Excel-arbetsblad är en vanlig uppgift när du fyller i kalkylark med listbaserad data. Denna åtgärd är användbar i scener som att ladda konfigurationsvärden, överföra data från externa källor eller initiera arbetsblad med fördefinierade strängsamlingar.

**Förutsättningar:**  
- En giltig JWT-token som erhålls via Aspose.Cells Cloud:s autentiseringsflöde.  
- Ett befintligt kalkylark (eller möjlighet att skapa ett) i din Aspose Cloud-lagring.  
- Rätt SDK-version som stöder modellen `ImportStringArrayOption`.

Detta REST API importerar data i form av strängarray till ett Excel-arbetsblad.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärandeparametrar**

Begäran använder multipart HTTP-innehåll (se [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
Den första delen av multipart-kroppen innehåller en **ImportStringArrayOption**-nyttolast; den andra delen innehåller källdatafil.

Viktiga parametrar beskrivs i följande tabell:

<caption>ImportStringArrayOption-parametrar</caption>
### **ImportStringArrayOption**

| Parameternamn        | Typ        | Beskrivning                                                                                                                                                                         |
| -------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Startradindex (1-baserat) dit data ska placeras.                                                                                                                     |
| FirstColumn          | int        | Startkolumnindex (1-baserat) dit data ska placeras.                                                                                                                  |
| IsVertical           | boolean    | `true` för att infoga data vertikalt; `false` för att infoga horisontellt.                                                                                                                   |
| Data                 | String[]   | Den strängarray som ska importeras.                                                                                                                                                    |
| DestinationWorksheet | string     | Namnet på arbetsbladet som ska ta emot data.                                                                                                                               |
| IsInsert             | boolean    | `true` för att infoga rader/kolumner (skjuta befintliga celler); `false` för att skriva över befintliga celler.                                                                                       |
| ImportDataType       | string     | Typ av data som importeras (t.ex. `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Beskriver var datafil finns när **BatchData** är null (t.ex. `CloudFileSystem`, `LocalFile`). Krävs om `BatchData` inte tillhandahålls.                                   |

### Exempel

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Blad1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### Svar

En lyckad begäran returnerar **HTTP 200** med ett JSON-svar liknande:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Möjliga statuskoder:

| Kod | Betydelse                               |
| --- | --------------------------------------- |
| 200 | Importen lyckades                       |
| 400 | Felaktig begäran – saknad eller ogiltig data |
| 401 | Otillåten åtkomst – ogiltig eller saknad token |
| 500 | Internt serverfel                       |


## Hur man använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}