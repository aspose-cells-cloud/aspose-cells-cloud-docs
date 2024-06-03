---
title: Arbetsboksinställning
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/workbooksettings/
description: "Aspose.Cells Molnmodellspecifikation: WorkbookSettings. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, Arbetsboksinställningar
weight: 50
---
## **arbetsbok Inställningar**

 Representerar alla inställningar i arbetsboken.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| AutoCompressPictures| Boolean| Sann| Falsk||Anger ett booleskt värde som anger att programmet automatiskt komprimerade bilder i arbetsboken.|
| Autoåterställning| Boolean| Sann| Falsk|| Indikerar om filen är markerad för automatisk återställning.|
| BuildVersion| Sträng| Sann| Falsk|| Anger den inkrementella offentliga versionen av programmet.|
| CalcMode| Sträng| Sann| Falsk|| Den anger om formler ska beräknas manuellt, automatiskt eller automatiskt förutom för flera tabelloperationer.|
| CalculationId| Sträng| Sann| Falsk|| Anger versionen av beräkningsmotorn som används för att beräkna värden i arbetsboken.|
| Kontrollera kompatibilitet| Boolean| Sann| Falsk|| Indikerar om du kontrollerar kompatibilitet när du sparar arbetsbok. Anmärkningar: Standardvärdet är sant.|
| CheckExcelRestriction| Boolean| Sann| Falsk||Om kontrollera begränsning av excel-fil när användaren ändrar cellrelaterade objekt. Till exempel tillåter excel inte inmatning av strängvärden som är längre än 32K. När du matar in ett värde som är längre än 32K, t.ex. Cell.PutValue(string), får du ett undantag om den här egenskapen är sann. Om den här egenskapen är falsk kommer vi att acceptera ditt inmatade strängvärde som cellens värde så att du senare kan mata ut hela strängvärdet för andra filformat som CSV. Men om du har angett en sådan typ av värde som är ogiltigt för Excel-filformat, bör du inte spara arbetsboken som Excel-filformat senare. Annars kan det uppstå ett oväntat fel för den genererade Excel-filen.|
| CrashSave| Boolean| Sann| Falsk|| anger om programmet senast sparade arbetsboksfilen efter en krasch.|
| Skapa CalcChain| Boolean| Sann| Falsk|| Om skapar beräknade formler kedja. Standard är falskt.|
| DataExtractLoad| Boolean| Sann| Falsk||anger om programmet senast öppnade arbetsboken för dataåterställning.|
| Datum 1904| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som representerar om arbetsboken använder 1904-datumsystemet.|
| DisplayDrawingObjects| Sträng| Sann| Falsk|| Anger om och hur objekt ska visas i arbetsboken.|
| Aktivera makron| Boolean| Sann| Falsk|| Aktivera makron;|
| FirstVisible Tab| Heltal| Sann| Falsk|| Hämtar eller ställer in den första synliga kalkylbladsfliken.|
| HidePivotFieldList| Boolean| Sann| Falsk|| Hämtar och ställer in om fältlistan för pivottabellen ska döljas.|
| IsDefaultEncrypted| Boolean| Sann| Falsk|| Anger om kryptering av arbetsboken med standardlösenord om struktur och Windows i arbetsboken är låsta.|
| Är gömd| Boolean| Sann| Falsk|| Anger om denna arbetsbok är dold.|
| IsHScrollBarVisible| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som anger om det genererade kalkylarket kommer att innehålla en horisontell rullningslist.|
| ÄrMinimerad| Boolean| Sann| Falsk|| Representerar om det genererade kalkylarket kommer att öppnas Minimerat.|
| IsVScrollBarVisible| Boolean| Sann| Falsk||Hämtar eller ställer in ett värde som anger om det genererade kalkylarket kommer att innehålla en vertikal rullningslist.|
| Iteration| Boolean| Sann| Falsk|| Anger om aktivera iterativ beräkning för att lösa cirkulära referenser.|
| Språkkod| Sträng| Sann| Falsk|| Hämtar eller ställer in användargränssnittsspråket för Workbook-versionen baserat på CountryCode som har sparat filen.|
| MaxChange| Flytande| Sann| Falsk|| Returnerar eller ställer in det maximala antalet ändringar för att lösa en cirkulär referens.|
| MaxIteration| Heltal| Sann| Falsk|| Returnerar eller ställer in det maximala antalet iterationer för att lösa en cirkulär referens.|
| Minnesinställning| Sträng| Sann| Falsk|| Hämtar eller ställer in alternativen för minnesanvändning. Det nya alternativet kommer att tas som standardalternativ för nyskapade kalkylblad men träder inte i kraft för befintliga kalkylblad.|
| NumberDecimalSeparator| Sträng| Sann| Falsk|| Hämtar eller ställer in decimalavgränsaren för formatering/analys av numeriska värden. Standard är decimalavgränsaren för aktuell region.|
| NumberGroupSeparator| Sträng| Sann| Falsk|| Hämtar eller ställer in tecknet som skiljer grupper av siffror till vänster om decimalen i numeriska värden. Standard är gruppseparatorn för aktuell region.|
| ParsingFormulaOnOpen| Boolean| Sann| Falsk||Anger om formeln analyseras när filen läses.|
| PrecisionAsDisplayed| Boolean| Sann| Falsk|| Sant om beräkningar i den här arbetsboken kommer att göras med enbart precisionen för siffrorna när de visas|
| RecalculateBeforeSave| Boolean| Sann| Falsk|| Indikerar om du ska räkna om innan du sparar dokumentet.|
| Beräkna på Öppen| Boolean| Sann| Falsk|| Indikerar om alla formler ska beräknas på nytt när filen öppnas.|
| Rekommendera Endast läs| Boolean| Sann| Falsk|| Indikerar om alternativet Rekommenderat skrivskydd är valt.|
| Område| Sträng| Sann| Falsk|| Hämtar eller ställer in de regionala inställningarna för arbetsboken.|
| Ta bort personlig information| Boolean| Sann| Falsk|| Sant om personlig information kan tas bort från den angivna arbetsboken.|
| ReparationLoad| Boolean| Sann| Falsk|| Anger om programmet senast öppnade arbetsboken i säkert läge eller reparationsläge.|
| Delad| Boolean| Sann| Falsk|| Hämtar eller ställer in ett värde som anger om arbetsboken är delad.|
| SheetTabBarWidth| Heltal| Sann| Falsk|| Bredd på kalkylbladets flikfält (i 1/1000 av fönstrets bredd).|
| Visa flikar| Boolean| Sann| Falsk||Hämta eller ställer in ett värde oavsett om flikarna Arbetsbok visas.|
| Uppdatera AdjacentCellsBorder| Boolean| Sann| Falsk|| Indikerar om uppdatering av angränsande cellers kantlinje.|
| UpdateLinksType| Sträng| Sann| Falsk|| Hämtar och ställer in hur externa länkar uppdateras när arbetsboken öppnas.|
| WindowHeight| Flytande| Sann| Falsk|| Höjden på fönstret, i punktenhet.|
| Fönster Vänster| Flytande| Sann| Falsk|| Avståndet från klientområdets vänstra kant till fönstrets vänstra kant, i punktenhet.|
| WindowTop| Flytande| Sann| Falsk|| Avståndet från klientområdets övre kant till fönstrets övre kant, i punktenhet.|
| WindowWidth| Flytande| Sann| Falsk|| Fönstrets bredd, i punktenhet.|
| Författare| Sträng| Sann| Falsk|| Hämtar och ställer in författaren till filen.|
| CheckCustomNumberFormat| Boolean| Sann| Falsk|| Anger om anpassat nummerformat kontrolleras när Style.Custom ställs in.|
| ProtectionType| Sträng| Sann| Falsk|| Får arbetsbokens skyddstyp.|
| Globaliseringsinställningar| Klass:Globaliseringsinställningar| Sann| Falsk|| Hämtar och ställer in globaliseringsinställningarna.|
| Lösenord| Sträng| Sann| Falsk||Representerar arbetsboksfilkrypteringslösenord.|
| Skrivskydd| Klass:Skrivskydd| Sann| Falsk|| Ger åtkomst till arbetsbokens skrivskyddsalternativ.|
| Är Krypterad| Boolean| Sann| Falsk|| Hämtar ett värde som anger om ett lösenord krävs för att öppna den här arbetsboken.|
| Är skyddad| Boolean| Sann| Falsk|| Får ett värde som indikerar om strukturen eller fönstret i arbetsboken är skyddad.|
| MaxRow| Heltal| Sann| Falsk|| Hämtar max radindex, nollbaserat.|
| MaxColumn| Heltal| Sann| Falsk|| Hämtar max kolumnindex, nollbaserat.|
| Signifikanta siffror| Heltal| Sann| Falsk|| Hämtar och ställer in antalet signifikanta siffror. Standardvärdet är .|
| Kontrollera kompatibilitet| Boolean| Sann| Falsk|| Anger om du kontrollerar kompatibilitet med tidigare versioner när du sparar arbetsboken.|
| Pappersformat| Sträng| Sann| Falsk|| Hämtar och ställer in standardstorleken för utskriftspapper.|
| MaxRowsOfSharedFormula| Heltal| Sann| Falsk|| Hämtar och ställer in det maximala radnumret för delad formel.|
| Efterlevnad| Sträng| Sann| Falsk|| Anger OOXML-versionen för utdatadokumentet. Standardvärdet är Ecma376_2006.|
| QuotePrefixToStyle| Boolean| Sann| Falsk||Anger om inställningsegenskapen när strängvärdet (som börjar med enkla citattecken) skrivs in i cellen|
| Formelinställningar| Klass:Formelinställningar| Sann| Falsk|| Hämtar inställningarna för formelrelaterade funktioner.|
| ForceFullCalculate| Boolean| Sann| Falsk|| Beräknar helt varje gång en beräkning utlöses.|

