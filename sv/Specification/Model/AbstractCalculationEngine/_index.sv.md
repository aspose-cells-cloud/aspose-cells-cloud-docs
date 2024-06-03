---
title: AbstractCalculationEngin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/abstractcalculationengine/
description: "Aspose.Cells Molnmodellspecifikation: AbstractCalculationEngine. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, AbstractCalculationEngine
weight: 50
---
## **abstractCalculationEngine**

Representerar användarens anpassade beräkningsmotor för att utöka standardberäkningsmotorn Aspose.Cells.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralRequired| Boolean| Sann| Falsk|| Indikerar om denna motor behöver den bokstavliga texten av parametern när den gör beräkningar. Standardvärdet är falskt.|
| IsParamArrayModeRequired| Boolean| Sann| Falsk|| Indikerar om denna motor behöver parametern för att beräknas i arrayläge. Standardvärdet är falskt. Om det krävs vid beräkning av anpassade funktioner måste den här egenskapen ställas in som sann.|
| ProcessBuiltInFunctions| Boolean| Sann| Falsk|| Huruvida inbyggda funktioner som har stöds av den inbyggda motorn bör kontrolleras och bearbetas av denna implementering. Standard är falskt. Om användaren behöver ändra beräkningslogiken för vissa inbyggda funktioner, ska denna egenskap ställas in som true. I annat fall lämna den här egenskapen som falsk för prestationsöverväganden.|

