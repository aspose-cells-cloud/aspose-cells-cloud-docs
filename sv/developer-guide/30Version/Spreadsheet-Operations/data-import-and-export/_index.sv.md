---
title: "Importera data till Excel-filer och exportera data från Excel-filer"
second_title: "Dokument"
linktitle: "Importera och exportera data"
type: docs
url: /data-import-and-export/
keywords: "Aspose.Cells Cloud, importera data, exportera Excel, API, CSV, JSON, bild, array"
description: "Lär dig hur du importerar data från CSV, JSON, arrayer och bilder till Excel-filer samt hur du exporterar arbetsböcker, diagram och former till PDF, PNG och mer med Aspose.Cells Cloud API (v3.0)."
weight: 25
---

Aspose.Cells Cloud API stöder import av data från olika källor och kan exportera Excel-arbetsböcker, diagram och andra objekt till olika format, inklusive **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** och mer. Detta gör datahantering och delning enkel och effektiv.

**API-version:** **v3.0** – Senast uppdaterad: **2024‑03‑15**

### Snabbstartsguide

1. **Förbered nyttolasten** – Skapa en JSON-body som beskriver import- eller exportalternativen (t.ex. `ImportCSVDataOption`, `ExportOptions`).
2. **Skicka begäran** – Använd `curl`, Postman eller ett SDK för att anropa lämplig slutpunkt (`POST /cells/import` eller `POST /cells/export`).
3. **Hantera svaret** – Vid lyckad import/export får du den bearbetade filen (binär eller Base64). Vid fel inspecterar du HTTP-statuskoden och felmeddelandet i JSON-body:en.

#### Förutsättningar

- Ett aktivt Aspose Cloud-konto och en giltig JWT-token.
- Målarbetsboken måste finnas på den angivna lagringsplatsen (för lagringsbaserade API:er).
- Rätt `Content-Type`-headers (`multipart/form-data` för filuppladdningar, `application/json` för JSON-body:ar).

## Hur man importerar data från olika datakällor

Att importera data till en Excel-fil innebär flera överväganden som måste tas i beaktande under processen. Möjligheten att importera många format och typer av data med professionell kvalitet är en av de främsta funktionerna i Aspose.Cells Cloud.

### Information om API:er för dataimport

Följande API:er tillhandahålls för att importera data till en eller flera Excel-filer:

| API                                                                                                | Beskrivning                                                  |
| :------------------------------------------------------------------------------------------------- | :----------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Importera data till Excel-filer utan att använda lagring.  |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Importera data till en Excel-fil som finns lagrad i molnet. |

### Begärparametrar

#### Utan användning av lagring

| Parameter Name | Type          | Location | Description                |
| :------------- | :------------ | :------- | :------------------------- |
| file           | file          | formData | Fil som ska laddas upp     |
| ImportOption   | ImportOptions | body     | Anger importformatet (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### Med användning av lagring

| Parameter Name | Type          | Location | Description                |
| :------------- | :------------ | :------- | :------------------------- |
| name           | string        | path     | Namn på Excel-filen        |
| folder         | string        | query    | Mappväg i lagringen        |
| storageName    | string        | query    | Lagringsnamn               |
| importData     | ImportOptions | body     | Nyttolast för dataimport   |

#### Parametrar för importalternativ

**De viktigaste parametrarna beskrivs i följande tabeller:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>Massdata att importera</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Om numerisk data ska konverteras (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Kolumnseparator</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Anpassade parserkonfigurationer</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Om bilden ska placeras vertikalt (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Bilddata (Base64-strängar)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>Tvådimensionell heltalsarray</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>Tvådimensionell dubbelarray</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>Tvådimensionell strängarray</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Om arrayen är vertikal (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Endimensionell heltalsarray</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>Index för första raden</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>Index för första kolumnen</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Om arrayen är vertikal (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Endimensionell dubbelarray</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Övre vänstra radindex</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Övre vänstra kolumnindex</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td>Nedre högra radindex</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Nedre högra kolumnindex</td></tr>
    <tr><td>Filename</td><td>string</td><td>Namn på källfilen</td></tr>
    <tr><td>Data</td><td>string</td><td>Strängdata att importera</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Namn på målarbetsbladet</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Om data ska infogas (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>Dataplats när BatchData är null</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Radindex för cellen</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Kolumnindex för cellen</td></tr>
    <tr><td>type</td><td>string</td><td>Data typ för cellvärdet</td></tr>
    <tr><td>value</td><td>string</td><td>Cellvärde</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>Definition av cellstil</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Parameter</th><th>Type</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem eller RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Sökväg till källfilen</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Hur man exporterar Excel-objekt till olika filformat

Om du ursprungligen skapade en Excel-fil i ett format såsom **XLS**, **XLSX**, **XLSB** eller **CSV**, kan du vilja konvertera den till ett annat format för att utnyttja specifika funktioner. Att exportera till **PDF** skyddar till exempel innehållet från obehöriga ändringar samtidigt som det blir lättare att läsa och dela.

Att exportera Excel-objekt innebär flera överväganden. Aspose.Cells Cloud tillhandahåller högkvalitativ export av arbetsböcker, diagram, former och bilder till ett brett utbud av format:

_Endast export-format_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
_För import och export_: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

Begäran använder multipart-innehåll enligt definitionen i [RFC 2046] och [RFC 1341]. Den första delen innehåller datafilen; den andra delen innehåller sparalternativen.

### Information om export-API

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### Begärparametrar

| Parameter Name | Type   | Location | Description                                                                                   |
| :------------- | :----- | :------- | :-------------------------------------------------------------------------------------------- |
| file           | file   | formData | Fil som ska laddas upp                                                                        |
| objectType     | string | query    | Objekttyp (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format         | string | query    | Önskat utdatafilformat (se [Stödda filformat](/cells/supported-file-formats/))               |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definierar ett offentligt tillgängligt programmeringsgränssnitt som låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att anropa API:et. Exemplet nedan visar en begäran och dess JSON-svar.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Vanliga HTTP-statuskoder

| Status | Betydelse                                                    | Rekommenderad åtgärd                              |
| ------ | ------------------------------------------------------------ | ------------------------------------------------- |
| 200    | Lyckades – filen exporterades                                | Bearbeta den returnerade filen/n                    |
| 400    | Felaktig begäran – saknade eller ogiltiga parametrar         | Verifiera begärans nyttolast och frågesträngar   |
| 401    | Obehörig – ogiltig eller utgången JWT-token                  | Uppdatera token och försök igen                  |
| 404    | Inte hittad – den angivna arbetsboken eller arbetsbladet finns inte | Kontrollera filnamn och lagringsväg             |
| 500    | Internt serverfel – oväntat tillstånd på servern              | Kontakta Aspose-support med begärans-ID           |

## Hur man anropar import- och export-API:er

Följande artiklar förklarar varje API i detalj och innehåller cURL- och SDK-exempel:

- [Hur man importerar data till Excel-filer utan att använda lagring.](/cells/import/without-using-storage)
- [Hur man importerar data till Excel-filer med hjälp av lagring.](/cells/import/with-using-storage)
- [Hur man importerar massdata till Excel-arbetsblad](/cells/import-batch-data-into-excel-worksheet/)
- [Hur man importerar CSV-data till Excel-arbetsblad](/cells/import-CSV-data-into-excel-worksheet/)
- [Hur man importerar bild till Excel-arbetsblad](/cells/import-picture-into-excel-worksheet/)
- [Hur man importerar heltalsarray till Excel-arbetsblad](/cells/import-integer-array-into-excel-worksheet/)
- [Hur man importerar dubbelarray till Excel-arbetsblad](/cells/import-double-array-into-excel-worksheet/)
- [Hur man importerar strängarray till Excel-arbetsblad](/cells/import-string-array-into-excel-worksheet/)
- [Hur man importerar 2D-heltalsarray till Excel-arbetsblad](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [Hur man importerar 2D-dubbelarray till Excel-arbetsblad](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [Hur man importerar 2D-strängarray till Excel-arbetsblad](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Hur man exporterar Excel-diagram till olika filformat](/cells/export-excel-chart-to-different-formats/)
- [Hur man exporterar Excel-listobjekt till olika filformat](/cells/export-excel-listobject-to-different-formats/)
- [Hur man exporterar Excel-ole-objekt till olika filformat](/cells/export-excel-ole-object/)
- [Hur man exporterar Excel-bild till olika filformat](/cells/export-excel-picture-to-different-formats/)
- [Hur man exporterar Excel-form till olika filformat](/cells/export-excel-shape-to-different-formats/)
- [Hur man exporterar Excel-arbetsbok till olika filformat](/cells/export-excel-to-different-formats/)
- [Hur man exporterar Excel-arbetsblad till olika filformat](/cells/export-excel-worksheet-to-different-formats/)

---