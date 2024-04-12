---
title: SqlScriptSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/sqlscriptsaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: SqlScriptSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **sqlScriptSaveOptions**

Representerar alternativen för att spara .sql-fil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| CheckIfTableExists| Boolean| Sann| Falsk|| Kontrollera om tabellnamnet finns innan du skapar|
| ColumnTypeMap| Sträng| Sann| Falsk|| Hämtar och ställer in kartan över kolumntyp för olika databas.|
| CheckAllDataForColumnType| Boolean| Sann| Falsk|| Kontrollera alla data för att hitta kolumnernas datatyp.|
| AddBlankLineBetween Rows| Boolean| Sann| Falsk|| Infoga tom rad mellan varje data.|
| Separator| Sträng| Sann| Falsk|| Hämtar och ställer in teckenseparator för sql-skript.|
| Operatörstyp| Sträng| Sann| Falsk|| Hämtar och ställer in operatortypen för sql.|
| Primärnyckel| Heltal| Sann| Falsk|| Representerar vilken kolumn som är primärnyckeln i datatabellen.|
| Skapa bord| Boolean| Sann| Falsk|| Anger om sql för att skapa tabell exporteras.|
| IdName| Sträng| Sann| Falsk|| Hämtar och ställer in namnet på id-kolumnen.|
| StartId| Heltal| Sann| Falsk|| Hämtar och ställer in start-id.|
| Tabellnamn| Sträng| Sann| Falsk|| Hämtar och ställer in tabellnamnet.|
|ExportAsString| Boolean| Sann| Falsk|| Anger om all data exporteras som strängvärde.|
| ExportArea| Klass: CellArea| Sann| Falsk|| Hämtar eller ställer in exportintervallet.|
| HasHeaderRow| Boolean| Sann| Falsk|| Anger om intervallet innehåller rubrikrad.|
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
|Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : (SaveOptions)[saveoptions]