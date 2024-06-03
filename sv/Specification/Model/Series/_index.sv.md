---
title: Serie
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/series/
description: "Aspose.Cells Molnmodellspecifikation: Serie. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, Series
weight: 50
---
## **serier**

 Kapslar in objektet som representerar en enskild dataserie i ett diagram.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| Område| Klass: Område| Sann| Falsk|| Representerar bakgrundsområdet för serieobjektet.|
| Bar3DShapeType| Sträng| Sann| Falsk|| Hämtar eller ställer in 3D-formtypen som används med 3D-stapel- eller kolumndiagrammet.|
| Gräns| Klass: Linje| Sann| Falsk|| Representerar kanten på serieobjektet.|
| BubbleScale| Heltal| Sann| Falsk||Hämtar eller ställer in skalfaktorn för bubblor i den angivna diagramgruppen. Det kan vara ett heltalsvärde från 0 (noll) till 300, vilket motsvarar en procentandel av standardstorleken. Gäller endast bubbeldiagram.|
| Bubblestorlekar| Sträng| Sann| Falsk|| Hämtar eller ställer in bubbelstorlekarna för diagramserien.|
| CountOfDataValues| Heltal| Sann| Falsk|| Hämtar antalet datavärden.|
| Dataetiketter| Klass: DataLabels| Sann| Falsk|| Representerar DataLabels-objektet för den angivna ASerien.|
| Visningsnamn| Sträng| Sann| Falsk|| Hämtar seriens namn som visas på diagrammet.|
| DoughnutHoleSize| Heltal| Sann| Falsk|| Returnerar eller ställer in storleken på hålet i en munkdiagramgrupp. Hålstorleken uttrycks i procent av diagramstorleken, mellan 10 och 90 procent.|
| DownBars| Klass: DropBars| Sann| Falsk|| Returnerar ett objekt som representerar nedstaplarna på ett linjediagram. Gäller endast linjediagram.|
| DropLines| Klass: Linje| Sann| Falsk||Returnerar ett objekt som representerar dropplinjerna för en serie på linjediagrammet eller ytdiagrammet. Gäller endast linjediagram eller områdesdiagram.|
| Explosion| Heltal| Sann| Falsk|| Avståndet för en öppen pajskiva från mitten av cirkeldiagrammet uttrycks i procent av pajdiametern.|
| FirstSliceAngle| Heltal| Sann| Falsk|| Hämtar eller ställer in vinkeln för det första cirkeldiagrammet eller munkdiagrammet, i grader (medsols från lodrät). Gäller endast paj-, 3D-paj- och munkdiagram, 0 till 360.|
| GapWidth| Heltal| Sann| Falsk|| Returnerar eller ställer in utrymmet mellan stapel- eller kolumnkluster, som en procentandel av stapelns eller kolumnbredden. Värdet på den här egenskapen måste vara mellan 0 och 500.|
| Har 3DEffect| Boolean| Sann| Falsk|| Sant om serien har ett tredimensionellt utseende. Gäller endast bubbeldiagram.|
| HasDropLines| Boolean| Sann| Falsk|| Sant om diagrammet har dropplinjer. Gäller endast linjediagram eller områdesdiagram.|
| HasHiLoLines| Boolean| Sann| Falsk|| Sant om linjediagrammet har hög-låg linjer. Gäller endast linjediagram.|
| HasLeaderLines| Boolean| Sann| Falsk|| Sant om serien har ledarlinjer.|
| Har RadarAxisLabels| Boolean| Sann| Falsk|| Sant om ett radardiagram har kategoriaxeletiketter. Gäller endast radarsjökort.|
| HasSeriesLines| Boolean| Sann| Falsk||Sant om ett staplat kolumndiagram eller stapeldiagram har serielinjer eller om ett cirkeldiagram eller ett stapeldiagram har kopplingslinjer mellan de två sektionerna. Gäller endast staplade kolumndiagram, stapeldiagram, cirkeldiagram eller cirkeldiagram.|
| HasUpDownBars| Boolean| Sann| Falsk|| Sant om ett linjediagram har staplar upp och ner. Gäller endast linjediagram.|
| HiLoLines| Klass: Linje| Sann| Falsk|| Returnerar ett HiLoLines-objekt som representerar hög-låg-linjerna för en serie på ett linjediagram. Gäller endast linjediagram.|
| IsAutoSplit| Boolean| Sann| Falsk|| Indikerar om tröskelvärdet är automatiskt.|
| Är Färgvarierad| Boolean| Sann| Falsk|| Representerar om färgen på punkterna varieras. Diagrammet får endast innehålla en serie.|
| LeaderLines| Klass: Linje| Sann| Falsk||Representerar ledarlinjer på ett diagram. Ledarlinjer kopplar dataetiketter till datapunkter. Detta objekt är inte en samling; det finns inget objekt som representerar en enda ledarlinje.|
| LegendEntry| Klass: LegendEntry| Sann| Falsk|| Får legendposten enligt denna serie.|
| Markör| Klass: Markör| Sann| Falsk|| Får markören.|
| namn| Sträng| Sann| Falsk|| Hämtar eller ställer in namnet på dataserien.|
| Överlappning| Heltal| Sann| Falsk|| Anger hur staplar och kolumner är placerade. Kan vara ett värde mellan – 100 och 100. Gäller endast för 2-D stapel- och 2-D kolumndiagram.|
| PlotOnSecondAxis| Boolean| Sann| Falsk|| Indikerar om denna serie är plottad på andra värdeaxeln.|
| Poäng| Klass: LinkElement| Sann| Falsk|| Får samlingen av poäng i en serie i ett diagram.|
| SecondPlotSize| Heltal| Sann| Falsk|| Returnerar eller ställer in storleken på den sekundära delen av antingen ett cirkeldiagram eller ett cirkeldiagram, som en procentandel av storleken på den primära cirkeln. Kan vara ett värde från 5 till 200.|
| SerieLines| Klass: Linje| Sann| Falsk||Returnerar ett SeriesLines-objekt som representerar serielinjerna för ett staplat stapeldiagram eller ett staplat kolumndiagram. Gäller endast staplade stapel- och staplade kolumndiagram.|
| Skugga| Boolean| Sann| Falsk|| Sant om serien har en skugga.|
| Visa negativa bubblor| Boolean| Sann| Falsk|| Sant om negativa bubblor visas för diagramgruppen. Gäller endast för bubbeldiagram.|
| Storlek Representerar| Sträng| Sann| Falsk|| Hämtar eller ställer in vad bubbelstorleken representerar på ett bubbeldiagram.|
| Slät| Boolean| Sann| Falsk|| Representerar kurvutjämning. Sant om kurvutjämning är aktiverat för linjediagrammet eller punktdiagrammet. Gäller endast för linje och spridning kopplade med linjediagram.|
| SplitType| Sträng| Sann| Falsk|| Returnerar eller ställer in ett värde som bestämmer vilka datapunkter som finns i den andra cirkeln eller stapeln på en cirkel- eller stapeldiagram.|
| SplitValue| Flytande| Sann| Falsk||Returnerar eller ställer in ett värde som ska användas för att bestämma vilka datapunkter som finns i den andra cirkeln eller stapeln på en cirkel- eller stapeldiagram.|
| TrendLines| Klass: Trendlinjer| Sann| Falsk|| Returnerar ett objekt som representerar en samling av alla trendlinjer för serien.|
| Typ| Sträng| Sann| Falsk|| Hämtar eller ställer in en dataseries typ.|
| UpBars| Klass: DropBars| Sann| Falsk|| Returnerar ett DropBars-objekt som representerar uppstaplarna på ett linjediagram. Gäller endast linjediagram.|
| Värderingar| Sträng| Sann| Falsk|| Representerar data för diagramserien.|
| XErrorBar| Klass: ErrorBar| Sann| Falsk|| Representerar X-riktningsfelstapeln i serien.|
| XVärden| Sträng| Sann| Falsk|| Representerar x-värdena för diagramserien.|
| YErrorBar| Klass: ErrorBar| Sann| Falsk|| Representerar Y-riktningsfelstapeln i serien.|
| länk| Klass: Länk| Sann| Falsk|||

**Förälders namn** : [LinkElement](/specification/model/linkelement)

