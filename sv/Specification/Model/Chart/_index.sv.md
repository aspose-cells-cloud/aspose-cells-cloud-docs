---
title: Röding
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/chart/
description: "Aspose.Cells Molnmodellspecifikation: Diagram. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, kalkylblad, Cloud REST API, diagram
weight: 50
---
## **Diagram**

 Kapslar in objektet som representerar ett enda Excel-diagram.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| AutoScaling| Boolean| Sann| Falsk|| Sant om Microsoft Excel skalar ett 3D-diagram så att det i storlek är närmare motsvarande 2D-diagram. Egenskapen RightAngleAxes måste vara True.|
| Bakvägg| Klass: Väggar| Sann| Falsk|| Returnerar ett objekt som representerar bakväggen i ett 3D-diagram.|
| Kategoriaxel| Klass: Axel| Sann| Falsk|| Hämtar diagrammets X-axel.|
| ChartArea| Klass: ChartArea| Sann| Falsk|| Hämtar diagramområdet i kalkylbladet.|
| ChartDataTable| Klass:ChartDataTable| Sann| Falsk|| Representerar diagramdatatabellen.|
| ChartObject| Klass: LinkElement| Sann| Falsk|| Representerar diagramformen;|
| DepthProcent| Heltal| Sann| Falsk||Representerar djupet på ett 3D-diagram som en procentandel av diagrammets bredd (mellan 20 och 2000 procent).|
| Elevation| Heltal| Sann| Falsk|| Representerar höjden av 3D-sjökortsvyn, i grader.|
| FirstSliceAngle| Heltal| Sann| Falsk|| Hämtar eller ställer in vinkeln för det första cirkeldiagrammet eller munkdiagrammet, i grader (medsols från lodrät). Gäller endast paj-, 3D-paj- och munkdiagram, 0 till 360.|
| Golv| Klass: Golv| Sann| Falsk|| Returnerar ett objekt som representerar väggarna i ett 3D-diagram.|
| GapDepth| Heltal| Sann| Falsk|| Hämtar eller ställer in avståndet mellan dataserierna i ett 3D-diagram, i procent av markörens bredd. Värdet på den här egenskapen måste vara mellan 0 och 500.|
| GapWidth| Heltal| Sann| Falsk|| Returnerar eller ställer in utrymmet mellan stapel- eller kolumnkluster, som en procentandel av stapelns eller kolumnbredden. Värdet på den här egenskapen måste vara mellan 0 och 500.|
| Höjdprocent| Heltal| Sann| Falsk||Returnerar eller ställer in höjden på ett 3D-diagram som en procentandel av diagrammets bredd (mellan 5 och 500 procent).|
| HidePivotField Buttons| Boolean| Sann| Falsk|| Indikerar om knapparna för pivotdiagramfältet endast döljs när diagrammet är pivotdiagram.|
| Is3D| Boolean| Sann| Falsk|| Anger om diagrammet är ett 3d-diagram.|
| Är rektangulärt med hörn| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som anger om diagramområdet är rektangulärt hörn. Standard är sant.|
| Legend| Klass: Legend| Sann| Falsk|| Får diagramlegenden.|
| namn| Sträng| Sann| Falsk|| Representerar diagramnamn.|
| NSerien| Klass:SeriesItems| Sann| Falsk|| Får en samling som representerar dataserien i diagrammet.|
| Utskriftsformat| Klass: LinkElement| Sann| Falsk|| Representerar sidkonfigurationsbeskrivningen i det här diagrammet.|
| Perspektiv| Heltal| Sann| Falsk|| Returnerar eller ställer in perspektivet för 3D-diagramvyn. Måste vara mellan 0 och 100. Den här egenskapen ignoreras om egenskapen RightAngleAxes är True.|
| PivotSource| Sträng| Sann| Falsk||Källan är data från pivottabellen. Om PivotSource inte är tomt är diagrammet PivotChart.|
| Placering| Sträng| Sann| Falsk|| Representerar hur diagrammet är fäst vid cellerna under det.|
| PlotArea| Klass: PlotArea| Sann| Falsk|| Hämtar diagrammets plotområde som inkluderar axelmarkeringsetiketter.|
| PlotEmptyCellsType| Sträng| Sann| Falsk|| Hämtar och ställer in hur de tomma cellerna ska plottas.|
| PlotVisibleCells| Boolean| Sann| Falsk|| Indikerar om endast plotta synliga celler.|
| Utskriftsstorlek| Sträng| Sann| Falsk|| Hämtar och ställer in den utskrivna diagramstorleken.|
| RightAngleAxes| Boolean| Sann| Falsk|| Sant om diagrammets axlar är i rät vinkel. Gäller endast för 3-D-diagram (förutom Column3D och 3-D-cirkeldiagram).|
| Rotations vinkel| Heltal| Sann| Falsk|| Representerar rotationen av 3D-diagramvyn (rotationen av plotområdet runt z-axeln, i grader).|
| SecondCategoryAxis| Klass: LinkElement| Sann| Falsk|| Hämtar diagrammets andra X-axel.|
| SecondValueAxis| Klass: LinkElement| Sann| Falsk|| Hämtar diagrammets andra Y-axel.|
| Serieaxel| Klass: LinkElement| Sann| Falsk|| Hämtar diagrammets serieaxel.|
| Former| Klass: LinkElement| Sann| Falsk|| Returnerar alla ritningsformer i det här diagrammet.|
|ShowDataTable| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som anger om diagrammet visar en datatabell.|
| ShowLegend| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som anger om diagramförklaringen kommer att visas. Standard är sant.|
| Sidovägg| Klass: LinkElement| Sann| Falsk|| Returnerar ett objekt som representerar sidoväggen i ett 3D-diagram.|
| SizeWithWindow| Boolean| Sann| Falsk|| Sant om Microsoft Excel ändrar storleken på diagrammet för att matcha storleken på diagrambladets fönster.|
| Stil| Heltal| Sann| Falsk|| Får och ställer in den inbyggda stilen.|
| Titel| Klass: LinkElement| Sann| Falsk|| Representerar diagramtitel.|
| Typ| Sträng| Sann| Falsk|| Representerar diagramtyp.|
| ValueAxis| Klass: Axel| Sann| Falsk|| Hämtar diagrammets Y-axel.|
| Väggar| Klass: LinkElement| Sann| Falsk|| Returnerar ett objekt som representerar väggarna i ett 3D-diagram.|
| WallsAndGridlines2D| Boolean| Sann| Falsk|| Sant om rutnät ritas tvådimensionellt på ett 3D-diagram.|
| länk| Klass: Länk| Sann| Falsk|||

**Förälders namn** : [LinkElement](/specification/model/linkelement)

