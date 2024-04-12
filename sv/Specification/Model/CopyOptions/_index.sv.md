---
title: CopyOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/copyoptions/
description: "Aspose.Cells Molnmodellspecifikation: CopyOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **copyOptions**

 Representerar kopieringsalternativen.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| Column CharacterWidth| Boolean| Sann| Falsk||Anger om kolumnbredden kopieras i teckenenhet.|
| CopyInvalidFormulasAsValues| Boolean| Sann| Falsk|| Om formeln inte är giltig för måldestinationen, kopiera endast värden.|
| CopyNames| Boolean| Sann| Falsk|| Anger om namnen kopieras.|
| ExtendToAdjacentRange| Boolean| Sann| Falsk|| Anger om intervallet utökas när intervallet kopieras till intilliggande intervall.|
| ReferToDestinationSheet| Boolean| Sann| Falsk|| När du kopierar intervallet i samma fil och diagrammet hänvisar till källarket betyder False att det kopierade diagrammets datakälla inte kommer att ändras. Sant betyder att det kopierade diagrammets datakälla refererar till målarket.|
| ReferToSheetWithSameName| Boolean| Sann| Falsk|| ms excel, när du kopierar formler som hänvisar till andra kalkylblad medan du kopierar ett kalkylblad till ett annat, bör de kopierade formlerna referera till källarbetsboken. Men i vissa situationer kan användaren behöva de kopierade formlerna hänvisa till kalkylblad med samma namn i samma arbetsbok, till exempel när dessa kalkylblad har kopierats före denna kopieringsoperation, då ska den här egenskapen behållas som sann.|

