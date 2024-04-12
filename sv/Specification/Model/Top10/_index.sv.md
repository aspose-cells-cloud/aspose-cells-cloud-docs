---
title: Topp1
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/top10/
description: "Aspose.Cells Molnmodellspecifikation: Top10. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **topp 10**

Beskriv Top10-regeln för villkorlig formatering. Denna regel för villkorlig formatering markerar celler vars värden hamnar i den övre N eller nedre N-parentesen, enligt vad som anges.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| IsBottom| Boolean| Sann| Falsk|| Hämta eller ställ in om en "top/bottom n"-regel är en "bottom n"-regel. Standardvärdet är falskt.|
| IsPercent| Boolean| Sann| Falsk|| Hämta eller ställ in om en "topp/botten n"-regel är en "topp/botten n procent"-regel. Standardvärdet är falskt.|
| Rang| Heltal| Sann| Falsk|| Hämta eller ställ in värdet på "n" i en "top/bottom n" villkorlig formateringsregel. Om IsPercent är sant måste värdet vara mellan 0 och 100. Annars måste det mellan 0 och 1000. Standardvärdet är 10.|

