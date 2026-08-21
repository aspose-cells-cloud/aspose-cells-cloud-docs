---
title: "Komprimera och reparera Excel-filer"
second_title: "Dokument"
type: docs
url: /compress-and-repair-excel-files/
linktitle: "Komprimera och reparera"
keywords: "Aspose.Cells, Excel-komprimering, Excel-reparation, moln-API, minska Excel-filstorlek, återställ korrupt arbetsbok, komprimera Excel-fil, reparera Excel-arbetsbok"
description: "Lär dig hur du komprimerar stora Excel-arbetsböcker och reparerar korrupta filer med Aspose.Cells Cloud API. Steg-för-steg-exempel, språk som stöds och bästa praxis."
weight: 100
ArticleTitle: "Komprimera och reparera Excel-filer – Aspose.Cells Cloud API"
---

Att komprimera en Excel-arbetsbok minskar dess filstorlek genom att ta bort oanvända stilar, bilder och delade strängar, medan reparation återställer integriteten hos korrupta arbetsböcker. Aspose.Cells Cloud API tillhandahåller dedikerade slutpunkter för båda åtgärderna.

- **[Komprimera data i en Excel-fil](https://docs.aspose.cloud/cells/compress-excel-files/).**
- **[Reparera Excel-filer](https://docs.aspose.cloud/cells/repair-excel-files/).**

**Komprimera arbetsbok API**  
Åtgärden **Komprimera** använder en enkel POST-begäran. Nedan följer en komplett specifikation för begäran/svaret:

| Metod | Slutpunkt | Nödvändiga parametrar | Begärandetext | Exempelsvar | Vanliga statuskoder |
|-------|-----------|-----------------------|---------------|----------------|---------------------|
| POST  | `/cells/compress` | `file` (binär) – arbetsboken som ska komprimeras; valfritt `outPath` (sträng) – målsökväg | *Ingen* (filen skickas som multipart/form‑data) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**Reparera arbetsbok API**  
Åtgärden **Reparera** använder också en POST-begäran. Dess specifikation är:

| Metod | Slutpunkt | Nödvändiga parametrar | Begärandetext | Exempelsvar | Vanliga statuskoder |
|-------|-----------|-----------------------|---------------|----------------|---------------------|
| POST  | `/cells/repair` | `file` (binär) – den korrupta arbetsboken; valfritt `outPath` (sträng) – var den reparerade filen ska sparas | *Ingen* (filen skickas som multipart/form‑data) | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

Dessa tabeller ger utvecklare de viktigaste uppgifterna som krävs för att anropa API:erna direkt utan att behöva söka vidare.

**Ytterligare resurser**  
- Se den fullständiga **[Komprimera Excel-filer](/compress-excel-files/)**-guiden för avancerade alternativ såsom borttagning av oanvända rader och kolumner.  
- Granska dokumentationen för **[Reparera Excel-filer](/repair-excel-files/)** för felsökningsTips och förklaringar till felkoder.  
-Utforska relaterade åtgärder som **[Hämta filinformation](/file-info/)** och **[Kalkylbladsåtgärder](/spreadsheet-operations/)** för en bredare förståelse av Aspose.Cells Cloud API.