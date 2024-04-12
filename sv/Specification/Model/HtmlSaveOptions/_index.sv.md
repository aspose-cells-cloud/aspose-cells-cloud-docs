---
title: HtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/htmlsaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: HtmlSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **htmlSparaalternativ**

 Representerar alternativ för att spara .html-fil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| ExportPageHeaders| Boolean| Sann| Falsk|||
| ExportPageFooters| Boolean| Sann| Falsk|||
| ExportRowColumnHeadings| Boolean| Sann| Falsk|||
| ShowAllSheets| Boolean| Sann| Falsk|||
| Bildalternativ| Class:ImageOrPrintOptions| Sann| Falsk|||
| SaveAsSingleFile| Boolean| Sann| Falsk|| Anger om HTML-filen sparas som en enda fil. Standardvärdet är falskt.|
| ExportHiddenWorksheet| Boolean| Sann| Falsk|| Anger om HTML-filen sparas som en enda fil. Standardvärdet är falskt.|
| ExportGridLines| Boolean| Sann| Falsk||Anger om rutnätslinjerna exporteras. Standardvärdet är falskt.|
| Presentationspreferens| Boolean| Sann| Falsk|| Anger om html- eller mht-fil är presentationspreferens. Standardvärdet är falskt. Om du vill få en vackrare presentation, ställ in värdet på sant.|
| CellCssPrefix| Sträng| Sann| Falsk|| Hämtar och ställer in prefixet för css-namnet, standardvärdet är "".|
| TabellCssId| Sträng| Sann| Falsk|| Hämtar och ställer in prefixet för typen css-namn som tr,col,td och så vidare, de finns i tabellelementet som har det specifika TableCssId-attributet. Standardvärdet är "".|
| IsFullPathLink| Boolean| Sann| Falsk|| Anger om fullständig sökvägslänk används i sheet00x.htm,filelist.xml och tabstrip.htm. Standardvärdet är falskt.|
| Exportera arbetsbladCSSSeparat| Boolean| Sann| Falsk|| Anger om kalkylbladets css exporteras separat. Standardvärdet är falskt.|
| ExportSimilarBorderStyle| Boolean| Sann| Falsk|||
| MergeEmptyTdForcely| Boolean| Sann| Falsk||Indikerar om man tvingar samman ett tomt TD-element vid export av fil till html. Storleken på html-filen kommer att minskas avsevärt efter att värdet ställts in på sant. Standardvärdet är falskt. Om du vill importera html-filen till Excel eller exportera perfekta rutnätslinjer när du sparar filen till html, vänligen behåll standardvärdet.|
| ExportCellCoordinate| Boolean| Sann| Falsk|| Anger om excel-koordinater för icke-tomma celler exporteras när filen sparas till html. Standardvärdet är falskt. Om du vill importera utdata-html till excel, behåll standardvärdet.|
| ExportExtraHeadings| Boolean| Sann| Falsk|| Anger om extra rubriker exporteras när textens längd är längre än maxvisningskolumnen. Standardvärdet är falskt. Om du vill importera html-filen till Excel, behåll standardvärdet.|
| ExportHeadings| Boolean| Sann| Falsk||Anger om rubriker exporteras när filen sparas till html. Standardvärdet är falskt. Om du vill importera html-filen till Excel, behåll standardvärdet.|
| ExportFormula| Boolean| Sann| Falsk|| Anger om formeln exporteras när filen sparas till html. Standardvärdet är sant. Om du vill importera utdata-html till excel, behåll standardvärdet|
| AddTooltipText| Boolean| Sann| Falsk|| Anger om man lägger till verktygstipstext när data inte kan visas helt.|
| ExportBogusRowData| Boolean| Sann| Falsk|| Anger om falsk data på nedre raden exporteras. Standardvärdet är true.Om du vill importera html- eller mht-filen till Excel, behåll standardvärdet.|
| ExcludeOusedStyles| Boolean| Sann| Falsk|| Anger om oanvända stilar exkluderas. Standardvärdet är falskt. Om du vill importera html- eller mht-filen till Excel, behåll standardvärdet.|
| ExportDocumentProperties| Boolean| Sann| Falsk||Anger om dokumentegenskaper exporteras. Standardvärdet är sant. Om du vill importera html- eller mht-filen till Excel, behåll standardvärdet.|
| ExportWorksheetProperties| Boolean| Sann| Falsk|| Anger om kalkylbladsegenskaper exporteras. Standardvärdet är sant. Om du vill importera html- eller mht-filen till Excel, behåll standardvärdet.|
| ExportWorkbookProperties| Boolean| Sann| Falsk|| Anger om arbetsboksegenskaper exporteras. Standardvärdet är sant. Om du vill importera html- eller mht-filen till Excel, behåll standardvärdet.|
| ExportFrameScriptsAndProperties| Boolean| Sann| Falsk|| Anger om ramskript och dokumentegenskaper exporteras. Standardvärdet är true.Om du vill importera html- eller mht-filen till Excel, behåll standardvärdet.|
| AttachedFilesDirectory| Sträng| Sann| Falsk|| Mappen som de bifogade filerna kommer att sparas i. Endast för att spara till html-ström.|
| AttachedFilesUrlPrefix| Sträng| Sann| Falsk||Ange URL-prefixet för bifogade filer som bild i html-filen. Endast för att spara till html-ström.|
| Kodning| Sträng| Sann| Falsk|||
| ExportActiveWorksheetOnly| Boolean| Sann| Falsk|| Indikerar om hela arbetsboken exporteras till html-fil.|
| ExportChartImageFormat| Sträng| Sann| Falsk|| Hämta eller ställ in formatet för diagrambilden innan du exporterar|
| ExportImagesAsBase64| Boolean| Sann| Falsk|||
| HiddenColDisplayType| Sträng| Sann| Falsk|| Hidden kolumn (bredden på denna kolumn är 0) i excel, innan du sparar den i html-format, om HtmlHiddenColDisplayType är "Remove", skulle den dolda kolumnen inte matas ut, om värdet är "Hidden", skulle kolumnen matas ut, men var dolt, standardvärdet är "Dold"|
| HiddenRowDisplayType| Sträng| Sann| Falsk||Hidden rad (höjden på den här raden är 0) i excel, innan du sparar den i html-format, om HtmlHiddenRowDisplayType är "Remove", skulle den dolda raden inte matas ut, om värdet är "Hidden", skulle raden matas ut, men var dolt, standardvärdet är "Dold"|
| HtmlCrossStringType| Sträng| Sann| Falsk|| Indikerar om en korscellsträng kommer att visas på samma sätt som MS Excel när en Excel-fil sparas i html-format. Som standard är värdet Default, så för korscellsträngar är det liten skillnad mellan html-filerna som skapats av Aspose.Cells och MS Excel. Men prestandan för att skapa stora html-filer, inställning av värdet till Cross skulle vara flera gånger snabbare än ställa in den till Default eller Fit2Cell.|
| IsExpImageToTempDir| Boolean| Sann| Falsk|| Indikerar om bildfiler exporteras till temporär katalog. Endast för att spara till html-ström.|
| Namn på sidan| Sträng| Sann| Falsk||Titeln på html-sidan. Endast för att spara till html-ström.|
| ParseHtmlTagInCell| Boolean| Sann| Falsk|| Analysera HTML-tagg i cell, som ,som cellvärde eller som HTML-tagg, standard är sant|
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
|Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : (SaveOptions)[saveoptions]