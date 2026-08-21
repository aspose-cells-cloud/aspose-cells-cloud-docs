---
title: "Arbetsblad – Sidinställning"
second_title: "Dokument"
linktitle: "Sidinställning"
type: docs
url: /page-setup/
keywords: "Aspose.Cells, pageSetup, arbetsblad, utskriftsinställningar, marginaler, orientering, pappersstorlek, sidhuvud, sidfot, skalning"
description: "Lär dig hur du konfigurerar utskriftslayout för Excel-arbetsblad med Aspose.Cells Cloud:s PageSetup-objekt. Innehåller en lista över egenskaper, standardvärden, intervall och kodexempel i C#, Java och Python."
weight: 20
ArticleTitle: "Arbetsblad – Sidinställning – Konfigurera utskriftslayout med Aspose.Cells Cloud"
---

# **PageSetup**

Excel-utskriftssidinställningar

## Översikt

**PageSetup**-objektet definierar utskriftslayoutalternativen för ett Excel-arbetsblad, till exempel marginaler, orientering, skalning, sidhuvud, sidfot och andra utskriftsrelaterade inställningar. Genom att konfigurera dessa egenskaper kan utvecklare skapa utskriftsvänliga arbetsböcker som matchar önskad utseende och sidindelning.

Här är ett kort C#-exempel som visar hur vanliga sidinställningsegenskaper ställs in med Aspose.Cells Cloud SDK:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initiera API-klienten (ersätt med dina autentiseringsuppgifter)
var apiInstance = new CellsApi("DIN_KLIENT_ID", "DIN_KLIENT_HEMILGHET");

// Definiera PageSetup-inställningarna
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Verkställ inställningarna på arbetsblad nummer ett i arbetsboken
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Detta kodstycke ställer in arbetsbladet i liggande orientering, använder A4-papper, centrera innehållet horisontellt och vertikalt samt applicerar en skalningsfaktor på 100 %.

## Egenskaper

| Egenskapsnamn         | Egenskapstyp | Nullable | ReadOnly | Standardvärde  | Beskrivning                                                                 |
| --------------------- | ------------ | -------- | -------- | -------------- | ---------------------------------------------------------------------------- |
| BlackAndWhite         | bool         | false    | false    | false          | Skriver ut arbetsbladet i svartvitt läge.                                    |
| BottomMargin          | float        | true     | false    | 2,54 cm        | Storlek på nedre marginalen i centimeter.                                    |
| CenterHorizontally    | bool         | false    | false    | false          | Centrerar arket horisontellt vid utskrift.                                   |
| CenterVertically      | bool         | false    | false    | false          | Centrerar arket vertikalt vid utskrift.                                      |
| FirstPageNumber       | int          | true     | false    | 1              | Det första sidnumret som används vid utskrift av arket.                     |
| FitToPagesTall        | int          | false    | false    | 1              | Antal sidor i höjdled som arbetsbladet skalas till.                          |
| FitToPagesWide        | int          | false    | false    | 1              | Antal sidor i breddled som arbetsbladet skalas till.                         |
| FooterMargin          | float        | true     | false    | 2,54 cm        | Avstånd från sidans nedre kant till sidfoten, i centimeter.                  |
| HeaderMargin          | float        | true     | false    | 2,54 cm        | Avstånd från sidans övre kant till sidhuvudet, i centimeter.                 |
| IsAutoFirstPageNumber | bool         | false    | false    | false          | Tilldelar det första sidnumret automatiskt.                                  |
| IsHFAlignMargins      | bool         | false    | false    | true           | Om true, matchas marginalerna för sidhuvud/sidfot med sidans marginaler.     |
| IsHFDiffFirst         | bool         | false    | false    | false          | Indikerar att sidhuvudet/sidfoten på första sidan skiljer sig från andra sidor. |
| IsHFDiffOddEven       | bool         | false    | false    | false          | Indikerar att sidhuvudet/sidfoten på udda sidor skiljer sig från jämna sidor. |
| IsHFScaleWithDoc      | bool         | false    | false    | false          | Skalas sidhuvud och sidfot tillsammans med dokumentet (Excel 2007+).        |
| IsPercentScale        | bool         | false    | false    | true           | När false styr `FitToPagesWide` och `FitToPagesTall` skalningen.             |
| LeftMargin            | float        | true     | false    | 2,54 cm        | Storlek på vänster marginal i centimeter.                                    |
| Order                 | string       | true     | false    | "DownThenOver" | Ordningen som Excel använder för att numrera sidor vid utskrift av stora arbetsblad. |
| Orientation           | string       | false    | false    | "Portrait"     | Sidorientering: **Landscape** eller **Portrait**.                            |
| PaperSize             | string       | true     | false    | "A4"           | Pappersstorlek som används vid utskrift.                                     |
| PrintArea             | string       | true     | false    | (inget)        | Cellintervall som ska skrivas ut (t.ex. `"A1:D20"`).                         |
| PrintComments         | string       | true     | false    | "NoComments"   | Hur kommentarer skrivs ut tillsammans med arket.                             |
| PrintCopies           | int          | true     | false    | 1              | Antal exemplar att skriva ut.                                                 |
| PrintDraft            | bool         | false    | false    | false          | Skriver ut arbetsbladet i utkastläge (utan grafik).                          |
| PrintErrors           | string       | true     | false    | "Display"      | Typ av utskriftsfel som visas.                                                |
| PrintGridlines        | bool         | false    | false    | false          | Skriver ut cellernas rutnät.                                                  |
| PrintHeadings         | bool         | false    | false    | false          | Skriver ut rad- och kolumnrubriker.                                           |
| PrintQuality          | int          | true     | false    | 600            | Utskriftskvalitetsinställning (punkter per tum).                             |
| PrintTitleColumns     | string       | true     | false    | (inget)        | Kolumner som ska upprepas på vänster sida av varje utskriven sida.           |
| PrintTitleRows        | string       | true     | false    | (inget)        | Rader som ska upprepas längst upp på varje utskriven sida.                   |
| RightMargin           | float        | true     | false    | 2,54 cm        | Storlek på höger marginal i centimeter.                                       |
| TopMargin             | float        | true     | false    | 2,54 cm        | Storlek på övre marginal i centimeter.                                        |
| Zoom                  | int          | false    | false    | 100            | Skalningsfaktor i procent (10–400 %).                                         |
| Header                | object       | true     | false    | (inget)        | Konfiguration för sidhuvud.                                                   |
| Footer                | object       | true     | false    | (inget)        | Konfiguration för sidfot.                                                     |

## Relaterade objekt

- **Header** – Konfigurerar arbetsbladets sidhuvud.  
- **Footer** – Konfigurerar arbetsbladets sidfot.  
- **PrintOptions** – Ytterligare utskriftsrelaterade inställningar, till exempel sidbrytningar och utskriftsområde.  
---