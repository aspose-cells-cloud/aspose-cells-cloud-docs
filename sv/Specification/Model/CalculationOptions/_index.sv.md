---
title: Beräkningsalternativ
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/calculationoptions/
description: "Aspose.Cells Molnmodellspecifikation : CalculationOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **beräkningsalternativ**

 

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| CalcStackSize| Heltal| Sann| Falsk|| Anger stackstorleken för att beräkna celler rekursivt.|
| IgnoreError| Boolean| Sann| Falsk|| Anger om fel som uppstår vid beräkning av formler ska ignoreras. Felet kan vara en funktion som inte stöds, externa länkar etc. Standardvärdet är sant.|
| Precisionsstrategi| Sträng| Sann| Falsk|| Specificerar strategin för bearbetningsprecision av beräkning.|
| Rekursiv| Boolean| Sann| Falsk||Anger om de beroende cellerna beräknas rekursivt vid beräkning av en cell och det beror på andra celler. Standardvärdet är sant.|
| CustomEngine| Klass:AbstractCalculation Engine| Sann| Falsk|| Den anpassade formelberäkningsmotorn för att utöka standardberäkningsmotorn Aspose.Cells.|
| CalculationMonitor| Klass:AbstractCalculationMonitor| Sann| Falsk|| Monitorn för användaren att spåra framstegen i formelberäkningen.|
| Länkade datakällor|Array<Class:Workbook> | Sann| Falsk|| Anger datakällorna för externa länkar som används i formler.|

