---
title: MHtmlSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/mhtmlsaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: MHtmlSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, MHtmlSaveOptions
weight: 50
---
## **mHtmlSaveOptions**

 Representerar alternativ för att spara .mhtml-fil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| AttachedFilesDirectory| Sträng| Sann| Falsk|| Mappen som de bifogade filerna kommer att sparas i. Endast för att spara till html-ström.|
| AttachedFilesUrlPrefix| Sträng| Sann| Falsk||Ange URL-prefixet för bifogade filer som bild i html-filen. Endast för att spara till html-ström.|
| Kodning| Sträng| Sann| Falsk|| Om inte inställt, använd Encoding.UTF8 som standardkodningstyp.|
| ExportActiveWorksheetOnly| Boolean| Sann| Falsk|| Indikerar om hela arbetsboken exporteras till html-fil.|
| ExportChartImageFormat| Sträng| Sann| Falsk|| Hämta eller ställ in formatet för diagrambilden innan du exporterar|
| ExportImagesAsBase64| Boolean| Sann| Falsk|| Anger om bilder sparas i Base64-format till HTML, MHTML eller EPUB.|
| HiddenColDisplayType| Sträng| Sann| Falsk|| Hidden kolumn (bredden på denna kolumn är 0) i excel, innan du sparar den i html-format, om HtmlHiddenColDisplayType är "Remove", skulle den dolda kolumnen inte matas ut, om värdet är "Hidden", skulle kolumnen matas ut, men var dolt, standardvärdet är "Dold"|
| HiddenRowDisplayType| Sträng| Sann| Falsk||Hidden rad (höjden på den här raden är 0) i excel, innan du sparar den i html-format, om HtmlHiddenRowDisplayType är "Remove", skulle den dolda raden inte matas ut, om värdet är "Hidden", skulle raden matas ut, men var dolt, standardvärdet är "Dold"|
| HtmlCrossStringType| Sträng| Sann| Falsk|| Indikerar om en korscellsträng kommer att visas på samma sätt som MS Excel när en Excel-fil sparas i html-format. Som standard är värdet Default, så för korscellsträngar är det liten skillnad mellan html-filerna som skapats av Aspose.Cells och MS Excel. Men prestandan för att skapa stora html-filer, inställning av värdet till Cross skulle vara flera gånger snabbare än ställer in den till Default eller Fit2Cell.|
| IsExpImageToTempDir| Boolean| Sann| Falsk|| Indikerar om bildfiler exporteras till temporär katalog. Endast för att spara till html-ström.|
| Namn på sidan| Sträng| Sann| Falsk||Titeln på html-sidan. Endast för att spara till html-ström.|
| ParseHtmlTagInCell| Boolean| Sann| Falsk|| Analysera HTML-tagg i cell, som ,som cellvärde eller som HTML-tagg, standard är sant|
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
| Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : [Spara Alternativ](/specification/model/saveoptions)

