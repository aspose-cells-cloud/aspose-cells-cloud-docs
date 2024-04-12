---
title: IconSe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/iconset/
description: "Aspose.Cells Molnmodellspecifikation: IconSet. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
weight: 50
---
## **ikonuppsättning**

 Beskriv IconSets villkorliga formateringsregel. Denna regel för villkorlig formatering tillämpar ikoner på celler enligt deras värden.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| CfIcons| Behållare| Sann| Falsk|| Få den från samlingen|
| Cfvos| Behållare| Sann| Falsk|| Hämta CFValueObjects-instansen.|
| IsCustom| Boolean| Sann| Falsk|| Indikerar om ikonuppsättningen är anpassad. Standardvärdet är falskt.|
| Omvänd| Boolean| Sann| Falsk||Hämta eller ställ in flaggan som anger om standardordningen för ikonerna i denna ikonuppsättning ska ändras. Standardvärdet är falskt.|
| ShowValue| Boolean| Sann| Falsk|| Hämta eller ställ in flaggan som anger om värdena för cellerna som denna ikonuppsättning används på ska visas. Standardvärdet är sant.|
| IconSetType| Sträng| Sann| Falsk|| Hämta eller Ställ in vilken typ av ikonuppsättning som ska visas. Att ställa in typen kommer att automatiskt kontrollera om den nuvarande Cfvos räkning överensstämmer med den nya typen. Om det inte överensstämmer kommer gamla Cfvos att rengöras och standard Cfvos kommer att läggas till.|

