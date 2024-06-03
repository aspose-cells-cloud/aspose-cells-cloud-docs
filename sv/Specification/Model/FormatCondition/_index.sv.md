---
title: FormatConditio
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/formatcondition/
description: "Aspose.Cells Molnmodellspecifikation: FormatCondition. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, FormatCondition
weight: 50
---
## **formatCondition**

 Representerar villkorligt formateringsvillkor.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| Prioritet| Heltal| Sann| Falsk||Prioriteten för denna villkorliga formateringsregel. Detta värde används för att bestämma vilket format som ska utvärderas och renderas. Lägre numeriska värden har högre prioritet än högre numeriska värden, där '1' är högsta prioritet.|
| Typ| Sträng| Sann| Falsk|| Hämtar och ställer in om det villkorliga formatet Typ.|
| StoppOmTrue| Boolean| Sann| Falsk|| Det är sant att inga regler med lägre prioritet kan tillämpas över denna regel när denna regel utvärderas till sann. Gäller endast Excel 2007;|
| Över medel| Klass: Övermedel| Sann| Falsk|| Hämta den villkorliga formateringens "AboveAverage"-instans. Standardinstansens regel markerar celler som ligger över genomsnittet för alla värden i intervallet. Gäller endast för typ = Övermedel.|
| Färgskala| Klass: Färgskala| Sann| Falsk||Hämta den villkorliga formateringens "ColorScale"-instans. Standardinstansen är en "grön-gul-röd" 3ColorScale . Gäller endast för typ = ColorScale.|
| DataBar| Klass: DataBar| Sann| Falsk|| Hämta den villkorliga formateringens "DataBar"-instans. Standardinstansens färg är blå. Endast giltig för typ är DataBar.|
| Formel 1| Sträng| Sann| Falsk|| Hämtar och ställer in värdet eller uttrycket som är kopplat till villkorlig formatering.|
| Formel 2| Sträng| Sann| Falsk|| Hämtar och ställer in värdet eller uttrycket som är kopplat till villkorlig formatering.|
| IconSet| Klass:IconSet| Sann| Falsk|| Hämta den villkorliga formateringens "IconSet"-instans. Standardinstansens IconSetType är TrafficLights31. Gäller endast för typ = IconSet.|
| Operatör| Sträng| Sann| Falsk|| Hämtar och ställer in operatortypen för villkorsformat.|
| Stil| Klass: Stil| Sann| Falsk|| Hämtar eller ställer in stil för villkorligt formaterade cellområden.|
| Text| Sträng| Sann| Falsk||Textvärdet i en regel för villkorlig formatering "text innehåller". Gäller endast för typen = innehåller text, inte innehåller text, börjar med och slutar med. Standardvärdet är null.|
| Tidsperiod| Sträng| Sann| Falsk|| Den tillämpliga tidsperioden i en "datum inträffar..." villkorlig formateringsregel. Gäller endast för typ = timePeriod. Standardvärdet är TimePeriodType.Today.|
| Topp 10| Klass: Top10| Sann| Falsk|| Hämta den villkorliga formateringens "Top10"-instans. Standardinstansens regel framhäver celler vars värden hamnar i parentesen översta 10. Gäller endast för typ är Top10.|
| länk| Klass: Länk| Sann| Falsk|||

**Förälders namn** : [LinkElement](/specification/model/linkelement)

**Barnens namn** : 
	-  [StyleFormatCondition](styleformatcondition) 
