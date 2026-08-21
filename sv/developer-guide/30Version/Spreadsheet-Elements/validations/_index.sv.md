---
title: "Arbeta med Excel-datavalidering"
second_title: "Dokument"
linktitle: "Valideringar"
type: docs
url: /sv/validations/
keywords: "Excel-datavalidering, Aspose.Cells Cloud, REST API, kalkylark, Office i molnet"
description: "Lär dig hur du lägger till, hämtar, uppdaterar, raderar och rensar Excel-datavalideringsregler med Aspose.Cells Cloud REST API. Innehåller exempel för .NET, Java, Python och PHP."
weight: 100
ArticleTitle: "Arbeta med Excel-datavalidering - Aspose.Cells Cloud API-dokumentation"
---

Excel-datavalidering är en funktion i Microsoft Excel som används för att styra vad en användare kan ange i en cell i ett kalkylark. Den kan begränsa inmatningar till ett visst datumintervall, enbart heltal eller till och med skapa rullgardinslistor som sparar utrymme och visar värden i en enda cell. Du kan också definiera ett anpassat meddelande som visas när en användare anger ett felaktigt värde eller ett ogiltigt format.

Exempelvis kan en användare ange ett möte som schemalagt mellan 09:00 och 18:00.

Datavalidering kan användas för att säkerställa att ett värde är ett positivt tal, ett datum mellan den 15:e och den 30:e i en månad, ett datum inom de nästa 30 dagarna eller ett textinlägg med färre än 25 tecken, och så vidare.

### API-översikt

| Åtgärd | HTTP-metod | Slutpunkt | Beskrivning |
|--------|------------|-----------|-------------|
| Lägg till | POST | `/cells/{file}/worksheets/{sheet}/validations` | Skapa en valideringsregel |
| Hämta | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Hämta en specifik regel |
| Hämta alla | GET | `/cells/{file}/worksheets/{sheet}/validations` | Lista alla regler |
| Uppdatera | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Ändra en regel |
| Radera | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Ta bort en regel |
| Rensa | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Ta bort alla regler |

## Arbeta med valideringar i en Excel-fil

- [Hur man lägger till en valideringsregel i ett Excel-kalkylark](/cells/validations/add/)
- [Hur man hämtar en valideringsregel från ett Excel-kalkylark](/cells/validations/get/)
- [Hur man hämtar alla valideringsregler från ett Excel-kalkylark](/cells/validations/get-all/)
- [Hur man raderar en valideringsregel från ett Excel-kalkylark](/cells/validations/delete/)
- [Hur man rensar alla valideringsregler från ett Excel-kalkylark](/cells/validations/clear/)
- [Hur man uppdaterar en valideringsregel i ett Excel-kalkylark](/cells/validations/update/)
---