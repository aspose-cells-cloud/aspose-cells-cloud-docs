---
title: "AutoFitterOptions – Egenskaper och användningsguide | Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "AutoFitterOptions"
type: docs
url: /sv/auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Excel autojustering, radhöjd, sammanslagna celler, API"
description: "Lär dig hur du styr autojustering av radhöjd, hantering av sammanslagna celler, dolda rader/kolumner, språkinställningar och återgivningsalternativ med AutoFitterOptions-objektet i Aspose.Cells Cloud API."
weight: 79
ArticleTitle: "AutoFitterOptions – Egenskaper och användningsguide för Aspose.Cells Cloud"
---

# AutoFitterOptions-egenskaper

`AutoFitterOptions`-objektet låter dig finjustera den automatiska justeringen av radhöjd som utförs av Aspose.Cells Cloud. Det är användbart när du behöver exakt kontroll över hantering av sammanslagna celler, dolda rader/kolumner, språkspecifik formatering eller beteende kopplat till återgivning.

**Förutsättningar** – För att använda dessa alternativ måste du autentiseras med en giltig OAuth 2.0-åtkomsttoken som innehåller omfattningen **Cells.ReadWrite**. Begäran fungerar med alla SDK-versioner som stöder v3.0-apidokumentationen.

| Namn                       | Typ         | Beskrivning                                                                                     | Anteckningar                                                                                                |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | Bestämmer hur sammanslagna celler justeras automatiskt.                                        | Tillåtna värden: `All`, `First`, `None`. Standard: `All`. Exempel på JSON: `"AutoFitMergedCellsType":"All"` |
| **IgnoreHidden**           | **boolean** | När värdet är **true** ignoreras dolda rader och kolumner under autojusteringsprocessen.         | Standard: `false`. Exempel på JSON: `"IgnoreHidden":false`                                                 |
| **OnlyAuto**               | **boolean** | Indikerar om endast rader vars höjd inte har anpassats manuellt ska justeras automatiskt.       | Standard: `false`. Exempel på JSON: `"OnlyAuto":false`                                                     |
| **DefaultEditLanguage**    | **string**  | Anger standardspråk för redigering i arbetsboken.                                               | Standard: systemets språk (t.ex. `"sv-SE"`). Exempel på JSON: `"DefaultEditLanguage":"en-US"`               |
| **MaxRowHeight**           | **double**  | Maximal radhöjd (i punkter) som tillämpas vid autojustering av rader. Värdet **0** innebär ingen gräns. | Standard: `0`. Exempel på JSON: `"MaxRowHeight":0`                                                          |
| **AutoFitWrappedTextType** | **string**  | Styr hur text som har radbrytning i celler justeras automatiskt.                               | Tillåtna värden: `All`, `OnlyWrapped`, `None`. Standard: `All`. Exempel på JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | Anger formateringsstrategin som används under autojusteringsåtgärden.                          | Vanliga värden: `AutoFit`, `PreserveExisting`. Standard: `AutoFit`. Exempel på JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | Indikerar om autojusteringen ska utföras för återgivningsändamål (t.ex. PDF, bild).            | Tillåtna värden: `True`, `False`. Standard: `False`. Exempel på JSON: `"ForRendering":"False"`              |

Nedan visas ett typiskt JSON-innehåll som kan skickas till API:et vid konfigurering av `AutoFitterOptions`.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Ett exempel på ett `cURL`-anrop som tillämpar dessa alternativ på en arbetsbok:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Referens för slutpunkt**

| Metod | URL | Obligatoriska parametrar | Beskrivning |
|-------|-----|-------------------------|-------------|
| PUT   | `/cells/workbook/autoFitter` | `autoFitterOptions` (JSON-nyttolast) | Tillämpar de angivna `AutoFitterOptions` på målarbetsboken. |
| GET   | `/cells/workbook/autoFitter` | *inga* | Hämtar de aktuella inställningarna för `AutoFitterOptions` för arbetsboken. |

**Begärandeparametrar för PUT-slutpunkten**

| Parameter                | Typ     | Obligatorisk | Beskrivning |
|--------------------------|---------|--------------|-------------|
| AutoFitMergedCellsType   | string  | Ja           | Hur sammanslagna celler justeras automatiskt (`All`, `First`, `None`). |
| IgnoreHidden             | boolean | Nej          | Om dolda rader/kolumner ska ignoreras. |
| OnlyAuto                 | boolean | Nej          | Justera endast rader utan manuella höjdställningar. |
| DefaultEditLanguage      | string  | Nej          | Redigeringspråk (t.ex. `sv-SE`). |
| MaxRowHeight             | double  | Nej          | Maximal radhöjd i punkter; `0` = obegränsad. |
| AutoFitWrappedTextType   | string  | Nej          | Hur radbrytad text hanteras (`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | Nej          | Formateringsstrategi (`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | Nej          | Tillämpa autojustering för återgivning (`True`, `False`). |

Typiska svarskoder:

- **200 OK** – Åtgärden slutfördes framgångsrikt.  
- **400 Bad Request** – Ogiltig JSON-nyttolast eller icke-stött värde.  
- **401 Unauthorized** – Saknad eller ogiltig autentiseringstoken.  
- **500 Internal Server Error** – Oväntat serverfel.

**Exempel på GET-svar**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Dessa exempel visar hur du konfigurerar och anropar `AutoFitterOptions`-modellen i Aspose.Cells Cloud API.