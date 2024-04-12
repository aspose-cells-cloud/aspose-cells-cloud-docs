---
title: OoxmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/ooxmlsaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: OoxmlSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **ooxmlSaveOptions**

 Representerar alternativ för att spara ooxml-fil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| ExportCellName| Boolean| Sann| Falsk||Indikerar om export av cellnamn till Excel2007 .xlsx (.xlsm, .xltx, .xltm) fil. Om utdatafilen kan nås av SQL Server DTS måste detta värde vara sant. Om du ställer in värdet på false ökar prestandan kraftigt och filstorleken minskar när du skapar stora filer. Standardvärdet är falskt.|
| UpdateZoom| Boolean| Sann| Falsk|| Anger om skalningsfaktorn uppdateras innan filen sparas om egenskaperna PageSetup.FitToPagesWide och PageSetup.FitToPagesTall styr hur kalkylbladet skalas.|
| AktiveraZip64| Boolean| Sann| Falsk|| Använd alltid ZIP64-tillägg när du skriver zip-arkiv, även när det är onödigt.|
| EmbedOoxmlAsOleObject| Boolean| Sann| Falsk|| Anger om Ooxml-filer av OleObject bäddas in som ole-objekt.|
| CompressionType| Sträng| Sann| Falsk|| Hämtar och ställer in komprimeringstypen för ooxml-fil.|
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
|Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : (SaveOptions)[saveoptions]