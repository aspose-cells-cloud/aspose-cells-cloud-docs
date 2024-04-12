---
title: PdfSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/pdfsaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: PdfSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **pdfSaveOptions**

 Representerar alternativ för att spara pdf-fil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| DisplayDocTitle| Boolean| Sann| Falsk|| Indikerar om fönstrets namnlist ska visa dokumentets titel.|
| ExportDocumentStructure| Boolean| Sann| Falsk|| Indikerar om dokumentstruktur ska exporteras.|
| EmfRenderSetting| Sträng| Sann| Falsk|| Inställning för rendering av Emf-metafil.|
| CustomPropertiesExport| Sträng| Sann| Falsk|| Anger hur CustomDocumentPropertyCollection exporteras till filen PDF.|
| OptimizationType| Sträng| Sann| Falsk|| Hämtar och ställer in pdf-optimeringstyp.|
| Producent| Sträng| Sann| Falsk|| Hämtar och ställer in producent av genererade pdf-dokument.|
| Pdf-komprimering| Sträng| Sann| Falsk||Ange komprimeringsalgoritmen.|
| FontEncoding| Sträng| Sann| Falsk|| Hämtar eller ställer in inbäddad teckensnittskodning i pdf.|
| Vattenstämpel| Klass: Rendering Watermark| Sann| Falsk|| Hämtar eller ställer in vattenstämpel till utmatning.|
| Beräkna Formel| Boolean| Sann| Falsk|| Anger om man beräknar formler innan pdf-filen sparas. Standardvärdet är falskt.|
| CheckFontCompatibility| Boolean| Sann| Falsk|| Anger om teckensnittskompatibilitet kontrolleras för varje tecken i texten. Standardvärdet är sant. Inaktivera den här egenskapen kan ge bättre prestanda. Men när standardtypsnittet eller det angivna teckensnittet för text/tecken inte kan användas för att återge det, kan oläsbara tecken (som block) förekomma i den genererade pdf-filen. För en sådan situation bör användaren behålla denna egenskap som sann så att alternativa teckensnitt kan sökas och användas för att återge texten istället;|
| Efterlevnad| Sträng| Sann| Falsk|| Arbetsboken konverteras till pdf enligt PdfCompliance i den här egenskapen.|
| DefaultFont| Sträng| Sann| Falsk||När tecken i Excel är unicode och inte är inställda med korrekt typsnitt i cellstil, kan de visas som block i pdf, bild. Ställ in standardteckensnittet som MingLiu eller MS Gothic för att visa dessa tecken. Om den här egenskapen inte är inställd kommer Aspose.Cells att använda systemets standardteckensnitt för att visa dessa unicode-tecken.|
| OnePagePerSheet| Boolean| Sann| Falsk|| Om OnePagePerSheet är sant , kommer allt innehåll på ett ark endast att matas ut till en sida som resultat. Pappersstorleken för sidinställningarna kommer att vara ogiltig och de andra inställningarna för sidinställningarna kommer fortfarande att gälla.|
| PrintingPageType| Sträng| Sann| Falsk|| Indikerar vilka sidor som inte kommer att skrivas ut.|
| Säkerhetsalternativ| Klass: PdfSecurityOptions| Sann| Falsk|| Ställ in detta alternativ när säkerhet behövs i xls2pdf-resultat.|
| önskad PPI| Heltal| Sann| Falsk||Ställ in önskad PPI (pixlar per tum) för omsamplingsbilder och jpeg-kvalitet. Alla bilder konverteras till JPEG med den angivna kvalitetsinställningen, och bilder som är större än den angivna PPI (pixlar per tum) kommer att samplas om. Önskade pixlar per tum. 220 hög kvalitet. 150 skärmkvalitet. 96 e-postkvalitet.|
| jpeg kvalitet| Heltal| Sann| Falsk|| Ställ in önskad PPI (pixlar per tum) för omsamplingsbilder och jpeg-kvalitet. Alla bilder konverteras till JPEG med den angivna kvalitetsinställningen, och bilder som är större än den angivna PPI (pixlar per tum) kommer att samplas om. 0 - 100 % JPEG kvalitet.|
| ImageType| Sträng| Sann| Falsk|| Representerar bildtypen vid konvertering av diagram och form.|
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
|Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : (SaveOptions)[saveoptions]