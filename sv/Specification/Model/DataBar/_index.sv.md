---
title: DataBa
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/databar/
description: "Aspose.Cells Molnmodellspecifikation: DataBar. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, DataBar
weight: 50
---
## **datafält**

 Beskriv DataBar-regeln för villkorlig formatering. Den här villkorliga formateringsregeln visar ett graderat datafält i cellintervallet.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| AxisColor| Klass: Färg| Sann| Falsk|| Får färgen på axeln för celler med villkorlig formatering som datafält.|
| AxisPosition| Sträng| Sann| Falsk|| Hämtar eller ställer in positionen för axeln för datastaplarna som anges av en villkorlig formateringsregel.|
| BarBorder| Klass: DataBarBorder| Sann| Falsk|| Hämtar ett objekt som anger gränsen för ett datafält.|
| BarFillType| Sträng| Sann| Falsk|| Hämtar eller ställer in hur ett datafält fylls med färg.|
| Färg| Klass: Färg| Sann| Falsk|| Hämta eller ställ in denna DataBars färg.|
| Riktning| Sträng| Sann| Falsk||Hämtar eller ställer in riktningen som datafältet visas.|
| MaxCfvo| Klass: ConditionalFormattingValue| Sann| Falsk|| Hämta eller ställ in denna DataBars maxvärdeobjekt. Det går inte att ställa in null eller CFValueObject med typen FormatConditionValueType.Min.|
| Maxlängd| Heltal| Sann| Falsk|| Representerar den maximala längden på datafältet.|
| MinCfvo| Klass: ConditionalFormattingValue| Sann| Falsk|| Hämta eller ställ in denna DataBars minvärdeobjekt. Det går inte att ställa in null eller CFValueObject med typen FormatConditionValueType.Max.|
| MinLängd| Heltal| Sann| Falsk|| Representerar den minsta längden på datafältet.|
| NegativeBarFormat| Klass:NegativeBarFormat| Sann| Falsk|| Hämtar NegativeBarFormat-objektet som är kopplat till en regel för villkorlig formatering av datafält.|
| ShowValue| Boolean| Sann| Falsk|| Hämta eller ställ in flaggan som indikerar om värdena för cellerna som denna datafält används på ska visas. Standardvärdet är sant.|

