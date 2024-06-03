---
title: ConditionalFormattingValu
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/conditionalformattingvalue/
description: "Aspose.Cells Molnmodellspecifikation: ConditionalFormattingValue. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, ConditionalFormattingValue
weight: 50
---
## **conditionalFormattingValue**

 Beskriver värdena för interpolationspunkterna i en gradientskala, dataBar eller iconSet.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| IsGTE| Boolean| Sann| Falsk||Skaffa eller sätt flaggan Greater Than Or Equal. Använd endast för ikonuppsättningar, avgör om detta tröskelvärde använder operatorn större än eller lika med. 'false' indikerar att 'större än' används istället för 'större än eller lika med'. Standardvärdet är sant.|
| Typ| Sträng| Sann| Falsk|| Hämta eller ställ in typen av detta villkorliga formateringsvärdeobjekt. Om du ställer in typen till FormatConditionValueType.Min eller FormatConditionValueType.Max ställs "Value" automatiskt in på null.|
| Värde| Klass: Objekt| Sann| Falsk|| Hämta eller ställ in värdet för detta villkorliga formateringsvärdeobjekt. Den ska användas tillsammans med Type.|

