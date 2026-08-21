---
title: "Arbeta med Excel-diagram"
second_title: "Dokument"
linktype: "diagram"
type: docs
url: /sv/charts/
aliases: [/arbeta-med-diagram/]
keywords: "Aspose, Cells, Excel, diagram, API, REST, moln, kalkylark"
description: "Lär dig hur du hanterar Excel-diagram med Aspose.Cells Cloud API. Steg-för-steg-guide, kodexempel och felhantering för att hämta, lägga till, uppdatera, ta bort och konvertera diagram till bildformat."
weight: 100
ArticleTitle: "Arbeta med Excel-diagram – Aspose.Cells Cloud-dokumentation"
---

## Arbeta med diagram i en Excel-fil

**Senast uppdaterad:** Juli 2026  

Excel-diagram är visuella representationer av data som hjälper användare att snabbt förstå trender och mönster.  
Aspose.Cells Cloud API gör det möjligt för utvecklare att programmeringsmässigt arbeta med dessa diagram i Excel-arbetsböcker som lagras i molnet. Med API:et kan du hämta befintliga diagram, lägga till nya, ändra deras egenskaper (t.ex. titlar, axlar och textfält), ta bort oönskade diagram samt konvertera diagram till bildformat för rapportering eller vidare bearbetning. Följande länkar ger direktåtkomst till de detaljerade operationsidor som beskriver varje stödd diagramrelaterad åtgärd.

### Snabbreferens

| Åtgärd | HTTP-metod | Endpoint (mall) | Dokumentation |
|--------|------------|-----------------|---------------|
| Hämta diagram | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Hämta diagram från ett kalkylblad](/sv/cells/get-chart-from-a-worksheet/) |
| Lägg till diagram | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Lägg till ett diagram i ett kalkylblad](/sv/cells/add-a-chart-in-a-worksheet/) |
| Ta bort alla diagram | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Ta bort alla diagram från ett kalkylblad](/sv/cells/delete-all-charts-from-a-worksheet/) |
| Ta bort diagram | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Ta bort ett diagram från ett kalkylblad](/sv/cells/delete-a-chart-from-a-worksheet/) |
| Konvertera diagram till bild | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Konvertera diagram till bild](/sv/cells/convert-chart-to-image/) |
| Hämta diagramområde | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Hämta diagramområde från ett kalkylblad](/sv/cells/get-chart-area-from-a-worksheet/) |
| Hämta fyllningsformat | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Hämta fyllningsformat för ett diagramområde från ett kalkylblad](/sv/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Hämta textfält | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Hämta diagramtextfält från ett kalkylblad](/sv/cells/get-chart-legend-from-a-worksheet/) |
| Uppdatera textfält | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Uppdatera diagramtextfält i ett kalkylblad](/sv/cells/update-chart-legend-in-a-worksheet/) |
| Visa textfält | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Visa diagramtextfält i ett kalkylblad](/sv/cells/show-chart-legend-in-a-worksheet/) |
| Dölj textfält | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Dölj diagramtextfält i ett kalkylblad](/sv/cells/hide-chart-legend-in-a-worksheet/) |
| Hämta titel | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Hämta diagramtitel från ett kalkylblad](/sv/cells/get-chart-title-from-a-worksheet/) |
| Ställ in titel | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Ställ in diagramtitel i Excel-kalkylblad](/sv/cells/set-chart-title-in-excel-worksheet/) |
| Uppdatera titel | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Uppdatera diagramtitel i Excel-kalkylblad](/sv/cells/update-chart-title-in-excel-worksheet/) |
| Ta bort titel | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Ta bort diagramtitel i ett kalkylblad](/sv/cells/delete-chart-title-in-a-worksheet/) |
| Uppdatera diagramegenskaper | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Uppdatera diagramegenskaper](/sv/cells/charts/properties/update/) |
| Hämta kategoriaxis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Hämta diagramkategoriaxis](/sv/cells/charts/category-axis/get/) |
| Hämta värdeaxis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Hämta diagramvärdeaxis](/sv/cells/charts/value-axis/get/) |
| Hämta andra kategoriaxis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Hämta diagram andra kategoriaxis](/sv/cells/charts/second-category-axis/get/) |
| Hämta andra värdeaxis | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Hämta diagram andra värdeaxis](/sv/cells/charts/second-value-axis/get/) |
| Uppdatera kategoriaxis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Uppdatera diagramkategoriaxis](/sv/cells/charts/category-axis/update/) |
| Uppdatera värdeaxis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Uppdatera diagramvärdeaxis](/sv/cells/charts/value-axis/update/) |
| Uppdatera andra kategoriaxis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Uppdatera diagram andra kategoriaxis](/sv/cells/charts/second-category-axis/update/) |
| Uppdatera andra värdeaxis | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Uppdatera diagram andra värdeaxis](/sv/cells/charts/second-value-axis/update/) |

- [Hämta diagram från ett kalkylblad](/sv/cells/get-chart-from-a-worksheet/)
- [Lägg till ett diagram i ett kalkylblad](/sv/cells/add-a-chart-in-a-worksheet/)
- [Ta bort alla diagram från ett kalkylblad](/sv/cells/delete-all-charts-from-a-worksheet/)
- [Ta bort ett diagram från ett kalkylblad](/sv/cells/delete-a-chart-from-a-worksheet/)
- [Konvertera diagram till bild](/sv/cells/convert-chart-to-image/)
- [Hämta diagramområde från ett kalkylblad](/sv/cells/get-chart-area-from-a-worksheet/)
- [Hämta fyllningsformat för ett diagramområde från ett kalkylblad](/sv/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Hämta diagramtextfält från ett kalkylblad](/sv/cells/get-chart-legend-from-a-worksheet/)
- [Uppdatera diagramtextfält i ett kalkylblad](/sv/cells/update-chart-legend-in-a-worksheet/)
- [Visa diagramtextfält i ett kalkylblad](/sv/cells/show-chart-legend-in-a-worksheet/)
- [Dölj diagramtextfält i ett kalkylblad](/sv/cells/hide-chart-legend-in-a-worksheet/)
- [Hämta diagramtitel från ett kalkylblad](/sv/cells/get-chart-title-from-a-worksheet/)
- [Ställ in diagramtitel i Excel-kalkylblad](/sv/cells/set-chart-title-in-excel-worksheet/)
- [Uppdatera diagramtitel i Excel-kalkylblad](/sv/cells/update-chart-title-in-excel-worksheet/)
- [Ta bort diagramtitel i ett kalkylblad](/sv/cells/delete-chart-title-in-a-worksheet/)
- [Uppdatera diagramegenskaper](/sv/cells/charts/properties/update/)
- [Hämta diagramkategoriaxis](/sv/cells/charts/category-axis/get/)
- [Hämta diagramvärdeaxis](/sv/cells/charts/value-axis/get/)
- [Hämta diagram andra kategoriaxis](/sv/cells/charts/second-category-axis/get/)
- [Hämta diagram andra värdeaxis](/sv/cells/charts/second-value-axis/get/)
- [Uppdatera diagramkategoriaxis](/sv/cells/charts/category-axis/update/)
- [Uppdatera diagramvärdeaxis](/sv/cells/charts/value-axis/update/)
- [Uppdatera diagram andra kategoriaxis](/sv/cells/charts/second-category-axis/update/)
- [Uppdatera diagram andra värdeaxis](/sv/cells/charts/second-value-axis/update/)