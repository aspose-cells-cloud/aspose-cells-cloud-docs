---
title: "Arbeta med Excel-områden"
second_title: "Document"
linktitle: "Range"
type: docs
url: /sv/ranges/
aliases: [  /sv/working-with-ranges/ ]
keywords: "Aspose.Cells, Excel-område, REST API, SDK, .NET, Java, Python, sammanfoga celler, kopiera område, ange områdets värde"
description: "Lär dig hur du hämtar, ändrar, formaterar, sammanfogar, flyttar och kopierar Excel-områden med Aspose.Cells Cloud REST API. Inkluderar SDK-kodexempel för .NET, Java, Python och mer."
weight: 100
ArticleTitle: "Arbeta med Excel-områden – Aspose.Cells Cloud-dokumentation"
---

Ett **område** representerar en enskild cell, en hel rad, en hel kolumn, ett sammanhängande block av celler eller ett tredimensionellt (3‑D) område som sträcker sig över flera kalkylblad.

## Arbeta med områden i en Excel-fil

Aspose.Cells Cloud REST API tillhandahåller dedikerade slutpunkter för varje områdesåtgärd. Följande lista innehåller länkar till detaljerade användningsexempel samt motsvarande HTTP-metod och slutpunkt för snabbreferens.

- [Hämta namngivna områden i arbetsboken](/cells/get-named-ranges-inside-the-workbook/) – Hämtar alla namngivna områden som definierats i en arbetsbok och returnerar deras adresser och omfattning. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Hämta celldata baserat på namngivet område](/cells/get-cells-data-based-on-named-range/) – Returnerar värdena för de celler som tillhör ett angivet namngivet område. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Ändra radhöjd i ett område](/cells/cells/change-heights-of-rows-inside-the-range/) – Justerar höjden för varje rad som ligger inom det angivna området. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Ändra kolumnbredd i ett område](/cells/cells/change-widths-of-columns-inside-the-range/) – Ändrar kolumnbredden för alla kolumner som skär området. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Sammanfoga ett cellområde till en enskild cell](/cells/combines-a-range-of-cells-into-a-single-cell/) – Sammanfogar de valda cellerna till en enda cell och bevarar värdet i övre vänstra hörnet. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Kopiera ett område i ett kalkylblad med klistroptioner](/cells/copy-range-in-a-worksheet-with-paste-options/) – Kopierar ett källområde till ett målområde med valfria klistringstyper (värden, format, formler etc.). **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Ange områdets stil](/cells/set-the-style-of-the-range/) – Tillämpar typsnitt, fyllning, ram och justering till alla celler i området. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Delsammanfoga celler i ett område](/cells/unmerge-merged-cells-of-the-range/) – Återställer en tidigare sammanfogningsåtgärd och återställer de ursprungliga enskilda cellerna. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Flytta ett namngivet område tillsammans med ett Excel-kalkylblad](/cells/move-a-named-ranged-with-a-excel-worksheet/) – Flyttar ett namngivet område till en ny adress inom samma kalkylblad eller till ett annat kalkylblad. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Ange områdets värde i ett Excel-kalkylblad](/cells/ranges/set-value/) – Skriver ett enda värde eller en array av värden till det angivna området. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Alla förfrågningar och svar är i JSON-format. Inkludera `Authorization`-headern med din åtkomsttoken för autentisering.