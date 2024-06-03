---
title: Cel
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/cell/
description: "Aspose.Cells Molnmodellspecifikation: Cell. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, Cell
weight: 50
---
## **cell**

 Kapslar in objektet som representerar en enskild arbetsbokscell.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| namn| Sträng| Sann| Falsk|| Får namnet på cellen.|
| Rad| Heltal| Sann| Falsk|| Hämtar radnummer (nollbaserat) för cellen.|
| Kolumn| Heltal| Sann| Falsk|| Hämtar kolumnnummer (nollbaserat) för cellen.|
| Värde| Sträng| Sann| Falsk|| Hämtar värdet som finns i den här cellen.|
| Typ| Sträng| Sann| Falsk|| Representerar cellvärdestyp.|
| Formel| Sträng| Sann| Falsk||Hämtar eller ställer in en formel för .|
| IsFormula| Boolean| Sann| Falsk|| Representerar om den angivna cellen innehåller formel.|
| IsMerged| Boolean| Sann| Falsk|| Kontrollerar om en cell är en del av ett sammanslaget område eller inte.|
| IsArrayHeader| Boolean| Sann| Falsk|| Indikerar cellens formel är och matrisformel och det är den första cellen i matrisen.|
| IsInArray| Boolean| Sann| Falsk|| Anger om cellformeln är en matrisformel.|
| IsErrorValue| Boolean| Sann| Falsk|| Kontrollerar om värdet på den här cellen är ett fel.|
| IsInTable| Boolean| Sann| Falsk|| Anger om denna cell är en del av tabellformeln.|
| IsStyleSet| Boolean| Sann| Falsk|| Indikerar om cellens stil är inställd. Om returnera false betyder det att den här cellen har ett standardcellformat.|
| HtmlString| Sträng| Sann| Falsk|| Hämtar och ställer in html-strängen som innehåller data och vissa format i denna cell.|
| Stil| Klass: LinkElement| Sann| Falsk|||
| Arbetsblad| Sträng| Sann| Falsk|| Hämtar föräldrakalkylbladet.|
| länk| Klass: Länk| Sann| Falsk|||

**Förälders namn** : [LinkElement](/specification/model/linkelement)

