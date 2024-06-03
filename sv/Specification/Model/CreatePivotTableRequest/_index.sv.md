---
title: CreatePivotTableReques
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/createpivottablerequest/
description: "Aspose.Cells Molnmodellspecifikation: CreatePivotTableRequest. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, CreatePivotTableRequest
weight: 50
---
## **skapa PivotTableRequest**

 Indikerar att skapa pivottabellsbegäran

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| namn| Sträng| Sann| Falsk|| Pivottabellens namn|
| Källdata| Sträng| Sann| Falsk|| Data för den nya PivotTable-cachen.|
| DestCellName| Sträng| Sann| Falsk||Cellen i det övre vänstra hörnet av pivottabellrapportens målområde.|
| UseSameSource| Boolean| Sann| Falsk|| Anger om samma datakälla används när en annan befintlig pivottabell har använt den här datakällan. Om egenskapen är sann kommer den att spara minne.|
| PivotFieldRows|Array<Integer> | Sann| Falsk|| Representerar radfält i en pivottabellrapport.|
| Pivotfältkolumner|Array<Integer> | Sann| Falsk|| Representerar kolumnfält i en pivottabellrapport.|
| PivotFieldData|Array<Integer> | Sann| Falsk|| Representerar datafält i en pivottabellrapport.|

