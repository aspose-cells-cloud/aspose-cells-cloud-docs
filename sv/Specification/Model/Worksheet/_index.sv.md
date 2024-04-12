---
title: Workshee
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/worksheet/
description: "Aspose.Cells Molnmodellspecifikation: Arbetsblad. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **arbetsblad**

 

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| Länkar| Behållare| Sann| Falsk|||
| DisplayRightToLeft| Boolean| Sann| Falsk|| Indikerar om det angivna kalkylbladet visas från höger till vänster istället för från vänster till höger. Standard är falskt.|
| DisplayZeros| Boolean| Sann| Falsk|| Sant om nollvärden visas.|
| FirstVisibleColumn| Heltal| Sann| Falsk|| Representerar första synliga kolumnindex.|
| FirstVisibleRow| Heltal| Sann| Falsk|| Representerar första synliga radindex.|
| namn| Sträng| Sann| Falsk|| Hämtar eller ställer in namnet på kalkylbladet.|
| Index| Heltal| Sann| Falsk|| Hämtar indexet för arket i kalkylbladssamlingen.|
| IsGridlinesVisible| Boolean| Sann| Falsk||Hämtar eller ställer in ett värde som anger om rutnätslinjerna är synliga. Standard är sant.|
| IsOutlineShown| Boolean| Sann| Falsk|| Indikerar om kontur ska visas.|
| IsPageBreakPreview| Boolean| Sann| Falsk|| Anger om det angivna kalkylbladet visas i normal vy eller förhandsvisning av sidbrytning.|
| Är synlig| Boolean| Sann| Falsk|| Representerar om arbetsbladet är synligt.|
| Är skyddad| Boolean| Sann| Falsk|| Indikerar om kalkylbladet är skyddat.|
| IsRowColumnHeadersVisible| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som anger om kalkylbladet kommer att visa rad- och kolumnrubriker. Standard är sant.|
| IsRulerVisible| Boolean| Sann| Falsk|| Indikerar om linjalen är synlig. Den här egenskapen används endast för förhandsgranskning av sidbrytningar.|
| Är vald| Boolean| Sann| Falsk|| Anger om detta kalkylblad är valt när arbetsboken öppnas.|
| TabColor| Klass: Färg| Sann| Falsk|| Representerar kalkylbladsflikfärg.|
| TransitionEntry| Boolean| Sann| Falsk|| Anger om alternativet Transition Formula Entry (Lotus-kompatibilitet) är aktiverat.|
| Övergångsutvärdering| Boolean| Sann| Falsk||Anger om alternativet Utvärdering av övergångsformel (Lotus-kompatibilitet) är aktiverat.|
| Typ| Sträng| Sann| Falsk|| Representerar kalkylbladstyp.|
| ViewType| Sträng| Sann| Falsk|| Hämtar och ställer in vytypen.|
| VisibilityType| Sträng| Sann| Falsk|| Indikerar det synliga tillståndet för detta ark.|
| Zoom| Heltal| Sann| Falsk|| Representerar skalningsfaktorn i procent. Det bör vara mellan 10 och 400.|
|Cells | Klass: LinkElement| Sann| Falsk|| Får samlingen.|
| Diagram| Klass: LinkElement| Sann| Falsk|| Får en samling|
| AutoShapes| Klass: LinkElement| Sann| Falsk|||
| OleObjects| Klass: LinkElement| Sann| Falsk|| Representerar en samling av i ett kalkylblad.|
| Kommentarer| Klass: LinkElement| Sann| Falsk|| Får samlingen.|
| Bilder| Klass: LinkElement| Sann| Falsk|| Får en samling.|
| MergedCells| Klass: LinkElement| Sann| Falsk|||
| Valideringar| Klass: LinkElement| Sann| Falsk|| Hämtar insamlingen av datavalideringsinställning i kalkylbladet.|
| Villkorsformat| Klass: LinkElement| Sann| Falsk|| Hämtar Conditional Formattings i kalkylbladet.|
| Hyperlänkar| Klass: LinkElement| Sann| Falsk|| Får samlingen.|

