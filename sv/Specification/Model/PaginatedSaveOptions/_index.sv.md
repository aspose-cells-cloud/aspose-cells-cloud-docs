---
title: PagineradSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: PaginatedSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, Paginerade Sparalternativ
weight: 50
---
## **paginerade Sparalternativ**

 Representerar alternativen för paginering.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| DefaultFont| Sträng| Sann| Falsk|| När tecknen i Excel är Unicode och inte är inställda med korrekt teckensnitt i cellstil, kan de visas som block i pdf, bild. Ställ in standardteckensnittet som MingLiu eller MS Gothic för att visa dessa tecken. Om den här egenskapen inte är inställd kommer Aspose.Cells att använda systemets standardteckensnitt för att visa dessa unicode-tecken.|
| CheckWorkbookDefaultFont| Boolean| Sann| Falsk|| När tecknen i Excel är Unicode och inte är inställda med korrekt typsnitt i cellstil, kan de visas som block i pdf, bild. Ställ in detta på sant för att försöka använda arbetsbokens standardteckensnitt för att visa dessa tecken först.|
| CheckFontCompatibility| Boolean| Sann| Falsk|| Anger om teckensnittskompatibilitet ska kontrolleras för varje tecken i texten.|
| IsFontSubstitutionCharGranularity| Boolean| Sann| Falsk||Indikerar om teckensnittet endast ska bytas ut när cellteckensnittet inte är kompatibelt med det.|
| OnePagePerSheet| Boolean| Sann| Falsk|| Om OnePagePerSheet är sant kommer allt innehåll på ett ark att matas ut till endast en sida i resultatet. Pappersstorleken för siduppsättningen kommer att vara ogiltig, och de andra inställningarna för siduppsättningen kommer fortfarande att gälla.|
| Alla kolumner i en sida per ark| Boolean| Sann| Falsk|| Om AllColumnsInOnePagePerSheet är sant, kommer allt kolumninnehåll på ett ark att matas ut till endast en sida i resultatet. Bredden på pappersstorleken för siduppsättningen kommer att ignoreras, och de andra inställningarna för siduppsättningen kommer fortfarande att gälla.|
| IgnoreError| Boolean| Sann| Falsk|| Indikerar om du behöver dölja felet under renderingen. Felet kan vara fel i form, bild, diagramrendering, etc.|
| OutputBlankPageWhenNothingToPrint| Boolean| Sann| Falsk|| Indikerar om en tom sida ska matas ut när det inte finns något att skriva ut.|
| Sidindex| Heltal| Sann| Falsk|| Hämtar eller ställer in det 0-baserade indexet för den första sidan som ska sparas.|
| Sidonummer| Heltal| Sann| Falsk|| Hämtar eller ställer in antalet sidor som ska sparas.|
| PrintingPageType| Sträng| Sann| Falsk|| Indikerar vilka sidor som inte kommer att skrivas ut.|
| GridlineType| Sträng| Sann| Falsk|| Hämtar eller ställer in rutnätstyp.|
| TextCrossType| Sträng| Sann| Falsk|| Hämtar eller ställer in visning av texttyp när textbredden är större än cellbredden.|
| DefaultEditLanguage| Sträng| Sann| Falsk|| Hämtar eller ställer in standardspråk för redigering.|
| EmfRenderSetting| Sträng| Sann| Falsk|||
| MergeAreas| Boolean| Sann| Falsk|||
| SortExternalNames| Boolean| Sann| Falsk|||
| UpdateSmartArt| Boolean| Sann| Falsk|||
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
| Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : [Spara Alternativ](/specification/model/saveoptions)

**Barnens namn** : 
	-  [DocxSaveOptions](docxsaveoptions) 
	-  [PptxSaveOptions](pptxsaveoptions) 
	-  [XpsSaveOptions](xpssaveoptions) 
