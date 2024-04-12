---
title: ColorScal
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/colorscale/
description: "Aspose.Cells Molnmodellspecifikation: ColorScale. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **färgskala**

 Beskriv ColorScales villkorliga formateringsregel. Denna villkorliga formateringsregel skapar en graderad färgskala på cellerna.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| MaxCfvo| Klass: ConditionalFormattingValue| Sann| Falsk|| Hämta eller ställ in denna ColorScales maxvärdeobjekt. Det går inte att ställa in null eller CFValueObject med typen FormatConditionValueType.Min.|
| MaxColor| Klass: Färg| Sann| Falsk||Hämta eller ställ in gradientfärgen för det maximala värdet i intervallet.|
| MidCfvo| Klass: ConditionalFormattingValue| Sann| Falsk|| Hämta eller ställ in denna ColorScales medelvärde objekt. Det går inte att ställa in CFValueObject med typen FormatConditionValueType.Max eller FormatConditionValueType.Min.|
| Mellanfärg| Klass: Färg| Sann| Falsk|| Hämta eller ställ in gradientfärgen för mittvärdet i intervallet.|
| MinCfvo| Klass: ConditionalFormattingValue| Sann| Falsk|| Hämta eller ställ in denna ColorScales minvärdeobjekt. Det går inte att ställa in null eller CFValueObject med typen FormatConditionValueType.Max.|
| MinColor| Klass: Färg| Sann| Falsk|| Hämta eller ställ in gradientfärgen för det lägsta värdet i intervallet.|

