---
title: Över genomsnittet
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/aboveaverage/
description: "Aspose.Cells Molnmodellspecifikation: över genomsnittet. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **över medel**

 Beskriv AboveAverage-regeln för villkorlig formatering. Denna regel för villkorlig formatering markerar celler som ligger över eller under genomsnittet för alla värden i intervallet.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| IsAboveAverage| Boolean| Sann| Falsk||Hämta eller ställ in flaggan som anger om regeln är en regel "över genomsnittet". "true" indikerar "över genomsnittet". Standardvärdet är sant.|
| ÄrEqualAverage| Boolean| Sann| Falsk|| Hämta eller ställ in flaggan som indikerar om kriterierna "övermedel" och "undermedelvärde" inkluderar själva genomsnittet eller exklusive det värdet. "true" anger att inkludera medelvärdet i kriterierna. Standardvärdet är falskt.|
| StdDev| Heltal| Sann| Falsk|| Hämta eller ställ in antalet standardavvikelser som ska inkluderas över eller under genomsnittet i den villkorliga formateringsregeln. Ingångsvärdet måste vara mellan 0 och 3 (inkludera 0 och 3). Att sätta detta värde till 0 betyder att stdDev inte är inställt. Standardvärdet är 0.|

