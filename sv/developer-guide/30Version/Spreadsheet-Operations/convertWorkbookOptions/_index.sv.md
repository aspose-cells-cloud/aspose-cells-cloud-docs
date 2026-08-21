---
title: "Konvertera arbetsboksalternativ"
second_title: "Dokument"
linktitle: "Konvertera arbetsboksalternativ"
type: docs
url: /sv/convert-workbook-options/
keywords: "Aspose.Cells, ConvertWorkbookOptions, Excel-konvertering, PDF, CSV, API"
description: "Konvertera arbetsboksalternativ – konfigurera Excel-arbetsbokskonvertering till PDF, CSV, HTML och mer med Aspose.Cells Cloud API."
weight: 79
ArticleTitle: "Konvertera arbetsboksalternativ – Aspose.Cells Cloud API"
---

# Egenskaper för ConvertWorkbookOptions

**API-version:** 23.12 (2024‑03)

`ConvertWorkbookOptions` är modellen för begäran som används av Aspose.Cells Cloud-konverterings-API:et för att ange hur en Excel-arbetsbok ska omvandlas till ett annat format (PDF, CSV, HTML etc.). Den sammanfattar information om källfilen, målformatet, inställningar för sidlayout och formatspecifika sparalternativ.

| Namn                                | Typ        | Beskrivning                                                                                                   | Anteckningar |
| ----------------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------- | ----- |
| **DataSource**                      | **Object**  | Källa för datafil: `CloudFileSystem`, `RequestFiles` eller `HttpUri`.                                            |       |
| **[FileInfo](/sv/cells/file-info/)**   | **Object**  | Beskriver filnamn, storlek och base64-kodat innehåll.                                                   |       |
| **[PageSetup](/sv/cells/page-setup/)** | **Object**  | Egenskaper för sidlayout såsom marginaler, orientering och skalning.                                              |       |
| **SaveOptions**                     | **Object**  | Behållare för formatspecifika alternativobjekt för spara (t.ex. `PdfSaveOptions`, `HtmlSaveOptions`).                |       |
| **ConvertFormat**                   | **string**  | Målfilformat (t.ex. **PDF**, **CSV**, **HTML**, **XLSX**, **TIFF**, etc.).                              |       |
| **CheckExcelRestriction**           | **boolean** | Får eller sätter om Excel-specifika begränsningar (maximalt antal rader, kolumner, arknamnslängd etc.) ska tillämpas. |       |

**Förutsättningar**

- Skaffa en giltig OAuth 2.0-åtkomsttoken för Aspose.Cells Cloud.  
- Se till att källfilen är tillgänglig via en av de stödda `DataSource`-typerna.

**Snabbexempel**

```json
{
  "DataSource": {
    "FileInfo": {
      "FileName": "Sample.xlsx",
      "FileContent": "<base64-kodat-innehåll>"
    }
  },
  "ConvertFormat": "pdf",
  "SaveOptions": {
    "PdfSaveOptions": {
      "CompressImages": true,
      "ImageQuality": 90
    }
  }
}
```

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d @request.json \
     -o Sample.pdf
```

**Detaljer för API-begäran**

Konverteringsåtgärden utförs med en **POST**-begäran till slutpunkten:

```
https://api.aspose.cloud/v3.0/cells/convert
```

Obligatoriska headrar:

| Header                | Värde                              |
|-----------------------|------------------------------------|
| `Authorization`       | `Bearer {access_token}`            |
| `Content-Type`        | `application/json`                |

Begärandetexten måste vara en JSON-representation av `ConvertWorkbookOptions` (se ovanstående exempel). Alla egenskaper är valfria om de inte krävs av det valda `ConvertFormat`.

**API-svar**

En lyckad konvertering returnerar **HTTP 200 OK** (eller **202 Accepted** vid asynkron bearbetning) med den konverterade filen strömmas i svaret. När svaret är en strömning innehåller headern `Content-Disposition` det föreslagna filnamnet.

Exempel på ett JSON-svar för en asynkron begäran:

```json
{
  "JobId": "a1b2c3d4e5",
  "Status": "InProgress",
  "ResultUrl": "https://api.aspose.cloud/v3.0/cells/jobs/a1b2c3d4e5/result"
}
```

**Statuskoder**

| Kod | Betydelse                                 |
|------|------------------------------------------|
| 200  | Konvertering slutförd; fil returnerad.     |
| 202  | Konvertering accepterad; resultatet finns tillgängligt senare. |
| 400  | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401  | Auktorisering saknas – ogiltig eller saknad token. |
| 403  | Förbjudet – otillräckliga rättigheter.   |
| 500  | Internt serverfel.                   |

**Anteckningar / begränsningar**

- Flaggan `CheckExcelRestriction` tillämpar Excel-begränsningar som maximalt antal rader (1 048 576) och kolumner (16 384).  
- Inte alla målformat stöder alla `SaveOptions`-egenskaper; icke-stödda alternativ ignoreras.  
- När `HttpUri` används som datakälla måste URL:en vara offentligt nåbar utan auktorisering.  
- API-metod- och slutpunktsinformation har lagts till för att förbättra utvecklarklarhet och minska integreringsfel.  

## Egenskaper för FileSource

| Egenskapsnamn  | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                                               |
| -------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------------------- |
| FileSourceType | String        | true     | false    |               | Anger källtypen (`CloudFileSystem`, `RequestFiles`, `HttpUri`). |
| FilePath       | String        | true     | false    |               | Sökväg till filen.                                                       |

## Egenskaper för DbfSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ExportAsString            | Boolean       | true     | false    |               | När **true** exporteras numeriska värden som strängar.  |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för DBF-filer.               |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.            |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.         |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.            |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.               |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.   |

## Egenskaper för DifSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för DIF-filer.               |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.            |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.         |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.            |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.               |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.   |

## Egenskaper för DocxSaveOptions

| Egenskapsnamn                     | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | Teckensnitt som används när ett källteckensnitt inte är tillgängligt.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Kontrollerar om arbetsbokens standardteckensnitt tillämpas.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Validerar teckensnittskompatibilitet för målformatet.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Styr tecken-nivå-teckensnittssubstitution.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Tvingar varje ark till en egen sida.               |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Fyller alla kolumner i ett ark på en sida.            |
| IgnoreError                       | Boolean       | true     | false    |               | Ignorerar icke-kritiska fel under konvertering.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | Genererar en tom sida om det inte finns något att rendera. |
| PageIndex                         | Integer       | true     | false    |               | Index för den första sidan att exportera.                    |
| PageCount                         | Integer       | true     | false    |               | Antal sidor att exportera.                            |
| PrintingPageType                  | String        | true     | false    |               | Anger sidtyp för utskrift.                 |
| GridlineType                      | String        | true     | false    |               | Bestämmer hur rutnätslinjer renderas.                |
| TextCrossType                     | String        | true     | false    |               | Definierar krysstyp för textrendering.            |
| DefaultEditLanguage               | String        | true     | false    |               | Standard språk för textredigering.                    |
| EmfRenderSetting                  | String        | true     | false    |               | Inställningar för EMF-rendering.                           |
| MergeAreas                        | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.       |
| SaveFormat                        | String        | true     | false    |               | Formatidentifierare för DOCX-filer.                 |
| CachedFileFolder                  | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.               |
| ClearData                         | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.           |
| RefreshChartCache                 | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.           |
| SortNames                         | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                   |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.              |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.    |
| EncryptDocumentProperties          | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.      |

## Egenskaper för HtmlSaveOptions

| Egenskapsnamn                   | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                          |
| ------------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportPageHeaders               | Boolean       | true     | false    |               | Inkluderar sidhuvuden i HTML-utdata.            |
| ExportPageFooters               | Boolean       | true     | false    |               | Inkluderar sidfötter i HTML-utdata.            |
| ExportRowColumnHeadings         | Boolean       | true     | false    |               | Exporterar rad- och kolumnrubriker.                     |
| ShowAllSheets                   | Boolean       | true     | false    |               | Visar alla kalkylblad i en enda HTML-fil.          |
| ImageOptions                    | Class         | true     | false    |               | Inställningar som styr bildrendering.               |
| SaveAsSingleFile                | Boolean       | true     | false    |               | Sparar hela arbetsboken som en HTML-fil.          |
| ExportHiddenWorksheet           | Boolean       | true     | false    |               | Inkluderar dolda kalkylblad i exporten.            |
| ExportGridLines                 | Boolean       | true     | false    |               | Renderar rutnätslinjer i HTML-utdata.               |
| PresentationPreference          | Boolean       | true     | false    |               | Optimerar HTML för presentationsläge.                |
| CellCssPrefix                   | String        | true     | false    |               | Prefix som läggs till i genererade CSS-klassnamn för celler. |
| TableCssId                      | String        | true     | false    |               | ID-attribut för den genererade HTML-tabellen.           |
| IsFullPathLink                  | Boolean       | true     | false    |               | Genererar fullständiga sökvägshyperlänkar för resurser.        |
| ExportWorksheetCSSSeparately    | Boolean       | true     | false    |               | Placera varje kalkylblads CSS i en separat fil.      |
| ExportSimilarBorderStyle        | Boolean       | true     | false    |               | Slår samman liknande kantstilsstilar för att minska CSS-storlek.     |
| MergeEmptyTdForcely             | Boolean       | true     | false    |               | Tvingar sammanfogning av tomma `<td>`-element.             |
| ExportCellCoordinate            | Boolean       | true     | false    |               | Inkluderar cellkoordinater (t.ex. A1) i HTML.    |
| ExportExtraHeadings             | Boolean       | true     | false    |               | Lägg till extra rubrikrader/kolumner vid behov.       |
| ExportHeadings                  | Boolean       | true     | false    |               | Exporterar rad- och kolumnrubriker.                     |
| ExportFormula                   | Boolean       | true     | false    |               | Visa formler istället för beräknade värden.         |
| AddTooltipText                  | Boolean       | true     | false    |               | Lägg till verktygstips med cellkommentarer.                   |
| ExportBogusRowData              | Boolean       | true     | false    |               | Inkludera platshållarrader för tomma data.            |
| ExcludeUnusedStyles             | Boolean       | true     | false    |               | Ta bort CSS-stilar som inte används.                |
| ExportDocumentProperties        | Boolean       | true     | false    |               | Skriver dokumentnivåegenskaper till HTML-meta-taggar.  |
| ExportWorksheetProperties       | Boolean       | true     | false    |               | Skriver kalkylbladsnivåegenskaper till HTML.           |
| ExportWorkbookProperties        | Boolean       | true     | false    |               | Skriver arbetsbokens nivåegenskaper till HTML.            |
| ExportFrameScriptsAndProperties | Boolean       | true     | false    |               | Inkludera skript och egenskaper för ramar.          |
| AttachedFilesDirectory          | String        | true     | false    |               | Katalogsökväg för bifogade filer.                   |
| AttachedFilesUrlPrefix          | String        | true     | false    |               | URL-prefix för bifogade filer.                       |
| Encoding                        | String        | true     | false    |               | Teckenkodning för HTML-filen.                |
| ExportActiveWorksheetOnly       | Boolean       | true     | false    |               | Exporterar endast det aktiva kalkylbladet.                   |
| ExportChartImageFormat          | String        | true     | false    |               | Bildformat som används för inbäddade diagram.               |
| ExportImagesAsBase64            | Boolean       | true     | false    |               | Kodar bilder som Base64-strängar.                    |
| HiddenColDisplayType            | String        | true     | false    |               | Hur dolda kolumner visas.                    |
| HiddenRowDisplayType            | String        | true     | false    |               | Hur dolda rader visas.                       |
| HtmlCrossStringType             | String        | true     | false    |               | Bestämmer hur korssträngsdata renderas.        |
| IsExpImageToTempDir             | Boolean       | true     | false    |               | Exporterar bilder till en temporär katalog.             |
| PageTitle                       | String        | true     | false    |               | Titel som används för den genererade HTML-sidan.              |
| ParseHtmlTagInCell              | Boolean       | true     | false    |               | Parser HTML-taggar i cellvärden.             |
| CellNameAttribute               | String        | true     | false    |               | Attributnamn som innehåller cellreferensen.        |
| SaveFormat                      | String        | true     | false    |               | Formatidentifierare för HTML-filer.                |
| CachedFileFolder                | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.              |
| ClearData                       | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                  |
| CreateDirectory                 | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.   |
| EnableHttpCompression           | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.           |
| RefreshChartCache               | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.           |
| SortNames                       | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                   |
| ValidateMergedAreas             | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.              |
| MergeAreas                      | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                 |
| SortExternalNames               | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                     |
| CheckExcelRestriction           | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.    |
| UpdateSmartArt                  | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.      |
| EncryptDocumentProperties       | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.     |

## Egenskaper för ImageSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| ChartImageType            | String        | true     | false    |               | Bildformat som används för diagramrendering.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | Namn som tilldelas inbäddade bilder i SVG-utdata.    |
| HorizontalResolution      | Integer       | true     | false    |               | Horisontell DPI för den exporterade bilden.              |
| ImageFormat               | String        | true     | false    |               | Målbildsformat (PNG, JPG etc.).              |
| IsCellAutoFit             | Boolean       | true     | false    |               | Auto-justerar cellinnehåll till bildstorlek.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | Renderar varje kalkylblad på en separat sida.         |
| OnlyArea                  | Boolean       | true     | false    |               | Exporterar endast det definierade området av kalkylbladet.    |
| PrintingPage              | String        | true     | false    |               | Sidlayout som används för utskrift.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | Visar en statusdialog under utskrift.             |
| Quality                   | Integer       | true     | false    |               | Kompressionskvalitet för JPEG-bilder (0‑100).       |
| TiffCompression           | String        | true     | false    |               | Komprimeringstyp för TIFF-bilder.                  |
| VerticalResolution        | Integer       | true     | false    |               | Vertikal DPI för den exporterade bilden.                |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för bildfiler.             |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.            |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.         |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.            |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.               |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.   |

## Egenskaper för JsonSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| ExportArea                | Class         | true     | false    |               | Definierar kalkylbladsområdet att exportera.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | Anger om första raden innehåller kolumnrubriker. |
| ExportAsString            | Boolean       | true     | false    |               | Exporterar alla värden som strängar.                           |
| Indent                    | String        | true     | false    |               | Sträng som används för indentering (t.ex. två blanksteg).          |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för JSON-filer.                    |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.                  |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                      |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.               |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.                  |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.         |

## Egenskaper för MarkdownSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                                  |
| ------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------------ |
| Encoding                  | String        | true     | false    |               | Teckenkodning för markdown-filen.                    |
| FormatStrategy            | String        | true     | false    |               | Strategi som används för att formatera markdown (t.ex. GitHub, CommonMark). |
| LineSeparator             | String        | true     | false    |               | Radbrytningstecken att använda.                              |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för markdown-filer.                    |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.                      |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                          |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.           |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.                   |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.                   |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                           |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.                      |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                         |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                             |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.            |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.              |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.             |

## Egenskaper för OoxmlSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| ExportCellName            | Boolean       | true     | false    |               | Inkluderar cellnamn i den exporterade filen.            |
| UpdateZoom                | Boolean       | true     | false    |               | Uppdaterar zoomnivån i utdokumentet.       |
| EnableZip64               | Boolean       | true     | false    |               | Aktiverar ZIP64-tillägg för stora filer.            |
| EmbedOoxmlAsOleObject     | Boolean       | true     | false    |               | Bäddar in OOXML som ett OLE-objekt.                       |
| CompressionType           | String        | true     | false    |               | Typ av kompression tillämpad (t.ex. Normal, Maximum). |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för OOXML-filer.               |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.              |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                  |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.           |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.           |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.              |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                 |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.     |

## Egenskaper för PclSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| fontFullName              | String        | true     | false    |               | Fullständigt namn på det teckensnitt som ska användas.                      |
| fontPclName               | String        | true     | false    |               | PCL-specifikt teckensnittsnamn.                            |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för PCL-filer.               |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.            |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.         |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.            |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.               |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.   |

## Egenskaper för PDFSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                          |
| ------------------------- | ------------- | -------- | -------- | ------------- | ---------------------------------------------------- |
| DisplayDocTitle           | Boolean       | true     | false    |               | Använder dokumentets titel som PDF-titel.            |
| ExportDocumentStructure   | Boolean       | true     | false    |               | Bevarar dokumentets logiska struktur.     |
| EmfRenderSetting          | String        | true     | false    |               | Inställningar för rendering av EMF-bilder.                   |
| CustomPropertiesExport    | String        | true     | false    |               | Styr export av anpassade dokumentegenskaper.       |
| OptimizationType          | String        | true     | false    |               | Typ av PDF-optimisering (t.ex. Size, Speed).        |
| Producer                  | String        | true     | false    |               | Namn på PDF-producentapplikationen.                |
| PDFCompression            | String        | true     | false    |               | Komprimeringsalgoritm för PDF-strömmar.               |
| FontEncoding              | String        | true     | false    |               | Kodning som används för inbäddade teckensnitt.                    |
| Watermark                 | Class         | true     | false    |               | Vattenmärkinställningar som appliceras på PDF:en.               |
| CalculateFormula          | Boolean       | true     | false    |               | Beräknar formler innan export.                   |
| CheckFontCompatibility    | Boolean       | true     | false    |               | Validerar teckensnittskompatibilitet för PDF-rendering.      |
| Compliance                | String        | true     | false    |               | PDF/A- eller PDF/X-konformitetsnivå.                     |
| DefaultFont               | String        | true     | false    |               | Teckensnitt som används när ett källteckensnitt inte är tillgängligt.         |
| OnePagePerSheet           | Boolean       | true     | false    |               | Placerar varje kalkylblad på en separat PDF-sida.        |
| PrintingPageType          | String        | true     | false    |               | Anger sidtyp för utskrift.                |
| SecurityOptions           | Class         | true     | false    |               | Säkerhetsinställningar såsom lösenord och rättigheter. |
| desiredPPI                | Integer       | true     | false    |               | Önskad upplösning i bildpunkter per tum.                  |
| jpegQuality               | Integer       | true     | false    |               | JPEG-bildkvalitet (0‑100).                          |
| ImageType                 | String        | true     | false    |               | Bildtyp som används för rasterisering.                   |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för PDF-filer.                 |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.              |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                  |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.   |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.           |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.           |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                   |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.              |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                 |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                     |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.    |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.      |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.     |

## Egenskaper för PptxSaveOptions

| Egenskapsnamn                     | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                            |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ------------------------------------------------------ |
| IgnoreHiddenRows                  | Boolean       | true     | false    |               | Hoppar över dolda rader vid export.                       |
| AdjustFontSizeForRowType          | String        | true     | false    |               | Kontrollerar teckensnittsstorleksjustering baserat på radtyp.       |
| ExportViewType                    | String        | true     | false    |               | Bestämmer vilken vy (bild, anteckningar) som ska exporteras.        |
| DefaultFont                       | String        | true     | false    |               | Teckensnitt som används när ett källteckensnitt inte är tillgängligt.           |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Kontrollerar om arbetsbokens standardteckensnitt tillämpas.   |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Validerar teckensnittskompatibilitet för målformatet.    |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Styr tecken-nivå-teckensnittssubstitution.            |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Placerar varje kalkylblad på en separat bild.             |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Fyller alla kolumner i ett ark på en bild.            |
| IgnoreError                       | Boolean       | true     | false    |               | Ignorerar icke-kritiska fel under konvertering.         |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | Genererar en tom bild om det inte finns något att rendera. |
| PageIndex                         | Integer       | true     | false    |               | Index för den första bilden att exportera.                    |
| PageCount                         | Integer       | true     | false    |               | Antal bilder att exportera.                            |
| PrintingPageType                  | String        | true     | false    |               | Anger sidtyp för utskrift.                  |
| GridlineType                      | String        | true     | false    |               | Bestämmer hur rutnätslinjer renderas.                 |
| TextCrossType                     | String        | true     | false    |               | Definierar krysstyp för textrendering.             |
| DefaultEditLanguage               | String        | true     | false    |               | Standard språk för textredigering.                     |
| EmfRenderSetting                  | String        | true     | false    |               | Inställningar för EMF-rendering.                            |
| MergeAreas                        | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                   |
| SortExternalNames                 | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                       |
| UpdateSmartArt                    | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.        |
| SaveFormat                        | String        | true     | false    |               | Formatidentifierare för PPTX-filer.                  |
| CachedFileFolder                  | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.                |
| ClearData                         | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                    |
| CreateDirectory                   | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.     |
| EnableHttpCompression             | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.             |
| RefreshChartCache                 | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.             |
| SortNames                         | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                     |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.                |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.      |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.       |

## Egenskaper för SqlScriptSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| CheckIfTableExists        | Boolean       | true     | false    |               | Kontrollerar om måltabellen redan finns.          |
| ColumnTypeMap             | String        | true     | false    |               | Mappning av kolumnnamn till SQL-datatyper.               |
| CheckAllDataForColumnType | Boolean       | true     | false    |               | Skannar alla rader för att avgöra kolumntyper.                    |
| AddBlankLineBetweenRows   | Boolean       | true     | false    |               | Infogar en tom rad mellan genererade rader.             |
| Separator                 | String        | true     | false    |               | Sträng som används för att separera kolumner (t.ex. komma, tab).      |
| OperatorType              | String        | true     | false    |               | SQL-operatör som används (INSERT, UPDATE etc.).                |
| PrimaryKey                | Integer       | true     | false    |               | Kolumnindex som fungerar som primärnyckel.               |
| CreateTable               | Boolean       | true     | false    |               | Genererar ett CREATE TABLE-statement.                      |
| IdName                    | String        | true     | false    |               | Namn på identifieringskolumnen.                           |
| StartId                   | Integer       | true     | false    |               | Startvärde för autoinkrementerande ID:n.                 |
| TableName                 | String        | true     | false    |               | Namn på måldatabastabellen.                       |
| ExportAsString            | Boolean       | true     | false    |               | Exporterar alla värden som strängar.                           |
| ExportArea                | Class         | true     | false    |               | Definierar kalkylbladsområdet att exportera.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | Anger om första raden innehåller kolumnrubriker. |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för SQL-skriptfiler.              |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.                  |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                      |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.               |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.                  |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.         |

## Egenskaper för SvgSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| SheetIndex                | Integer       | true     | false    |               | Index för kalkylbladet att exportera.                  |
| ChartImageType            | String        | true     | false    |               | Bildformat som används för diagramrendering.             |
| EmbeddedImageNameInSvg    | String        | true     | false    |               | Namn som tilldelas inbäddade bilder i SVG-utdata.    |
| HorizontalResolution      | Integer       | true     | false    |               | Horisontell DPI för den exporterade SVG:en.                |
| ImageFormat               | String        | true     | false    |               | Målbildsformat för raster-element.           |
| IsCellAutoFit             | Boolean       | true     | false    |               | Auto-justerar cellinnehåll till SVG-storlek.           |
| OnePagePerSheet           | Boolean       | true     | false    |               | Renderar varje kalkylblad på en separat SVG-sida.     |
| OnlyArea                  | Boolean       | true     | false    |               | Exporterar endast det definierade området av kalkylbladet.    |
| PrintingPage              | String        | true     | false    |               | Sidlayout som används för utskrift.                     |
| PrintWithStatusDialog     | Boolean       | true     | false    |               | Visar en statusdialog under utskrift.             |
| Quality                   | Integer       | true     | false    |               | Kompressionskvalitet för rasterbilder.             |
| TiffCompression           | String        | true     | false    |               | Komprimeringstyp för TIFF-bilder inbäddade i SVG.  |
| VerticalResolution        | Integer       | true     | false    |               | Vertikal DPI för den exporterade SVG:en.                  |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för SVG-filer.               |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.            |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.         |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.            |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.               |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.   |

## Egenskaper för TxtSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                                             |
| ------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------------------------- |
| QuoteType                 | String        | true     | false    |               | Typ av citat som används (t.ex. dubbla, enkla).                            |
| Separator                 | String        | true     | false    |               | Kolumnseparator-tecken (t.ex. komma, tab).                          |
| SeparatorString           | String        | true     | false    |               | Fullständig sträng som används som separator när mer än ett tecken behövs. |
| AlwaysQuoted              | Boolean       | true     | false    |               | Tvingar alla fält att citeras.                                         |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för TXT-filer.                                    |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.                                 |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                                     |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.                      |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.                              |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.                              |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                                      |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.                                 |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                                    |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                                        |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.                       |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.                         |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.                        |

## Egenskaper för XlsSaveOptions & XlsbSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                        |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------- |
| MatchColor                | Boolean       | true     | false    |               | Bevarar exakta cellfärger vid export.         |
| WpsCompatibility          | Boolean       | true     | false    |               | Aktiverar kompatibilitet med WPS Office.             |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för XLS/XLSB-filer.          |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.            |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                |
| CreateDirectory           | Boolean       | true     | false    |               | Skapar målmappen om den inte finns. |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.         |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.         |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                 |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.            |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.               |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                   |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.  |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.    |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.   |

## Egenskaper för XmlSaveOptions

| Egenskapsnamn             | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                              |
| ------------------------- | ------------- | -------- | -------- | ------------- | -------------------------------------------------------- |
| SheetIndexes              | Array         | true     | false    |               | Lista över kalkylbladsindex att inkludera i exporten.      |
| ExportArea                | Class         | true     | false    |               | Definierar kalkylbladsområdet att exportera.                    |
| HasHeaderRow              | Boolean       | true     | false    |               | Anger om första raden innehåller kolumnrubriker. |
| XmlMapName                | String        | true     | false    |               | Namn på XML-kartan applicerad på kalkylbladet.            |
| SheetNameAsElementName    | Boolean       | true     | false    |               | Använder kalkylbladsnamnet som XML-elementnamn.             |
| DataAsAttribute           | Boolean       | true     | false    |               | Exporterar celldata som XML-attribut istället för element. |
| SaveFormat                | String        | true     | false    |               | Formatidentifierare för XML-filer.                     |
| CachedFileFolder          | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.                  |
| ClearData                 | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                      |
| CreateDirectory           | String        | true     | false    |               | Skapar målmappen om den inte finns.       |
| EnableHttpCompression     | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.               |
| RefreshChartCache         | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.               |
| SortNames                 | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                       |
| ValidateMergedAreas       | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.                  |
| MergeAreas                | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                     |
| SortExternalNames         | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                         |
| CheckExcelRestriction     | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.        |
| UpdateSmartArt            | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.          |
| EncryptDocumentProperties | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.         |

## Egenskaper för XpsSaveOptions

| Egenskapsnamn                     | Egenskapstyp | Nullable | ReadOnly | Standardvärde | Beskrivning                                           |
| --------------------------------- | ------------- | -------- | -------- | ------------- | ----------------------------------------------------- |
| DefaultFont                       | String        | true     | false    |               | Teckensnitt som används när ett källteckensnitt inte är tillgängligt.          |
| CheckWorkbookDefaultFont          | Boolean       | true     | false    |               | Kontrollerar om arbetsbokens standardteckensnitt tillämpas.  |
| CheckFontCompatibility            | Boolean       | true     | false    |               | Validerar teckensnittskompatibilitet för målformatet.   |
| IsFontSubstitutionCharGranularity | Boolean       | true     | false    |               | Styr tecken-nivå-teckensnittssubstitution.           |
| OnePagePerSheet                   | Boolean       | true     | false    |               | Placerar varje kalkylblad på en separat XPS-sida.         |
| AllColumnsInOnePagePerSheet       | Boolean       | true     | false    |               | Fyller alla kolumner i ett ark på en sida.            |
| IgnoreError                       | Boolean       | true     | false    |               | Ignorerar icke-kritiska fel under konvertering.        |
| OutputBlankPageWhenNothingToPrint | Boolean       | true     | false    |               | Genererar en tom sida om det inte finns något att rendera. |
| PageIndex                         | Integer       | true     | false    |               | Index för den första sidan att exportera.                    |
| PageCount                         | Integer       | true     | false    |               | Antal sidor att exportera.                            |
| PrintingPageType                  | String        | true     | false    |               | Anger sidtyp för utskrift.                 |
| GridlineType                      | String        | true     | false    |               | Bestämmer hur rutnätslinjer renderas.                |
| TextCrossType                     | String        | true     | false    |               | Definierar krysstyp för textrendering.            |
| DefaultEditLanguage               | String        | true     | false    |               | Standard språk för textredigering.                    |
| EmfRenderSetting                  | String        | true     | false    |               | Inställningar för EMF-rendering.                           |
| MergeAreas                        | Boolean       | true     | false    |               | Slår ihop intilliggande celler när möjligt.                  |
| SortExternalNames                 | Boolean       | true     | false    |               | Sorterar externa namngivna referenser.                      |
| UpdateSmartArt                    | Boolean       | true     | false    |               | Uppdaterar SmartArt-objekt till den senaste versionen.       |
| SaveFormat                        | String        | true     | false    |               | Formatidentifierare för XPS-filer.                  |
| CachedFileFolder                  | String        | true     | false    |               | Mapp som används för temporära cachelagrade filer.               |
| ClearData                         | Boolean       | true     | false    |               | Raderar befintligt data innan spara.                   |
| CreateDirectory                   | Boolean       | true     | false    |               | Skapar målmappen om den inte finns.    |
| EnableHttpCompression             | Boolean       | true     | false    |               | Aktiverar HTTP-kompression för svaret.            |
| RefreshChartCache                 | Boolean       | true     | false    |               | Uppdaterar cachelagrat diagramdata innan spara.            |
| SortNames                         | Boolean       | true     | false    |               | Sorterar namngivna intervall alfabetiskt.                    |
| ValidateMergedAreas               | Boolean       | true     | false    |               | Validerar sammanslagna celler för konsekvens.               |
| CheckExcelRestriction             | Boolean       | true     | false    |               | Verkställer Excel-specifika begränsningar under konvertering.     |
| EncryptDocumentProperties         | Boolean       | true     | false    |               | Krypterar dokumentegenskaper i utdatafilen.      |
---