---
title: "Importera 2D-strängmatris till Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Importera 2D-strängmatris"
type: docs
url: /sv/import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-string-array-into-excel-worksheet/",
    "/import-2dimension-string-array-into-worksheet/",
    "/import-data/-2dimension-string-array/",
    "/import-data/2dimension-string-array/",
    "/import/2dimension-string-array/",
  ]
keywords: "Aspose.Cells Cloud, importera 2D-strängmatris, Excel, REST API, SDK"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att importera en tvådimensionell strängmatris till ett Excel-arbetsblad. Innehåller begärandeformat, parameterbeskrivningar och SDK-kodexempel för C#, PHP och Ruby."
weight: 20
---

Denna REST API **importerar en tvådimensionell strängmatris** till ett Excel-arbetsblad.

Begäran är en HTTP-begäran med multipart-innehåll (se [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) eller [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Den första delen av multipart-innehållet innehåller `Import2DimensionStringArrayOption`-data och den andra delen innehåller datafilen.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

De viktiga parametrarna beskrivs i följande tabell:

### **Import2DimensionStringArrayOption**

| Parameter Name       | Typ                 | Beskrivning                                                                 |
| -------------------- | ------------------- | --------------------------------------------------------------------------- |
| FirstRow             | int                 | Nollbaserat radindex där importen börjar.                                   |
| FirstColumn          | int                 | Nollbaserat kolumnindex där importen börjar.                                |
| Data                 | String[,]           | Tvådimensionell matris som innehåller strängvärden att importera.           |
| DestinationWorksheet | string              | Namn på arbetsbladet som ska ta emot den importerade data.                  |
| IsInsert             | string (true/false) | Om **true**, infogas data och befintliga celler skjuts i följd.             |
| ImportDataType       | string              | Anger datatyp; använd `TwoDimensionStringArray` för denna operation.       |
| Source               | FileSource          | Anger datafilens plats när `BatchData`-parametern är null.                  |

### Exempel på begärandetext

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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

| Kod | Betydelse                   | Beskrivning                                                 |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller detaljerad åtgärdsinformation. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp stöds inte). |
| 401 | Obehörig                    | Ogiltig eller saknad JWT-token.                             |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.           |
| 500 | Internt serverfel           | Oväntat serverfel.                                          |

## Hur man använder PostImportData API med SDK:er

### PostImportData API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att integrera denna funktionalitet. En SDK abstraher bort detaljer på lägre nivå så att du kan fokusera på din affärslogik. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}