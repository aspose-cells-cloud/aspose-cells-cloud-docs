---
title: ImageSaveOption
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/imagesaveoptions/
description: "Aspose.Cells Molnmodellspecifikation: ImageSaveOptions. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, ImageSaveOptions
weight: 50
---
## **imageSaveOptions**

 Representerar alternativ för att spara bildfil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| ChartImageType| Sträng| Sann| Falsk|| Ange diagrambildstyp vid konvertering.|
| EmbededImageNameInSvg| Sträng| Sann| Falsk|| Ange filnamnet på den inbäddade bilden i svg. Detta bör vara fullständig sökväg med katalog som "c:\\xpsEmbeded"|
| Horisontell upplösning| Heltal| Sann| Falsk|| Hämtar eller ställer in den horisontella upplösningen för genererade bilder, i punkter per tum. Tillämpar genererande bildmetoden förutom bilder i Emf-format. Standardvärdet är 96.|
| Bildformat| Sträng| Sann| Falsk|| Hämtar eller ställer in formatet för de genererade bilderna. Använd inte metoden som returnerar ett Bitmap-objekt. Standardvärdet är ImageFormat.Bmp. Använd inte metoden som returnerar ett Bitmap-objekt.|
| IsCellAutoFit| Boolean| Sann| Falsk|| Indikerar om bredden och höjden på cellerna automatiskt anpassas efter cellvärde. Standardvärdet är falskt.|
| OnePagePerSheet| Boolean| Sann| Falsk||Om OnePagePerSheet är sant , kommer allt innehåll på ett ark endast att matas ut till en sida som resultat. Pappersstorleken för sidinställningarna kommer att vara ogiltig och de andra inställningarna för sidinställningarna kommer fortfarande att gälla.|
| OnlyArea| Boolean| Sann| Falsk|| Om den här egenskapen är sann kommer endast Area att matas ut och ingen skala kommer att träda i kraft.|
| Utskriftssida| Sträng| Sann| Falsk|| Indikerar vilka sidor som inte kommer att skrivas ut.|
| PrintWithStatusDialog| Boolean| Sann| Falsk|| Om PrintWithStatusDialog = true , kommer det att finnas en dialogruta som visar aktuell utskriftsstatus. annars visas ingen sådan dialog.|
| Kvalitet| Heltal| Sann| Falsk|| Hämtar eller ställer in ett värde som bestämmer kvaliteten på de genererade bilderna som endast gäller när sidor sparas i Jpeg-format. Har endast effekt när du sparar till JPEG. Värdet måste vara mellan 0 och 100. Standardvärdet är 100.|
| TiffCompression| Sträng| Sann| Falsk|| Hämtar eller ställer in typen av komprimering så att den endast tillämpas när sidor sparas i Tiff-formatet. Har endast effekt när du sparar till TIFF. Standardvärdet är Lzw.|
| Vertikal upplösning| Heltal| Sann| Falsk||Hämtar eller ställer in den vertikala upplösningen för genererade bilder, i punkter per tum. Tillämpar genererande bildmetod förutom EMF-formatbild. Standardvärdet är 96.|
| SaveFormat| Sträng| Sann| Falsk|||
| Cachad filmapp| Sträng| Sann| Falsk|||
| Radera data| Boolean| Sann| Falsk|||
| Skapa katalog| Boolean| Sann| Falsk|||
| Aktivera HTTPCompression| Boolean| Sann| Falsk|||
| RefreshChartCache| Boolean| Sann| Falsk|||
| Sortera namn| Boolean| Sann| Falsk|||
| Validera sammanslagna områden| Boolean| Sann| Falsk|||

**Förälders namn** : [Spara Alternativ](/specification/model/saveoptions)

