---
title: "Aspose.Cells Cloud Web API – Översätt kalkylark till målspråk"
second_title: "Dokument"
ArticleTitle: "Så här översätter du hela ett kalkylark med Aspose.Cells Cloud AI-översättnings-API"
linktitle: "Översätt kalkylark"
type: docs
url: /sv/translate-spreadsheet/
keywords: "Aspose.Cells Cloud, API för översättning av kalkylark, AI-översättning, översättning av kalkylark, targetLanguage, översättning över flera kalkylblad, molnbaserad bearbetning av kalkylark, översättning i Aspose.Cells Cloud"
description: "Översätt hela en Excel-arbetsbok med Aspose.Cells Cloud AI. Bevara formler, diagram och formatering medan texten översätts till valfritt stödjt språk. Lär dig om slutpunkten, parametrar, SDK-exempel, begränsningar och felhantering."
weight: 100
---

**TranslateSpreadsheet**-slutpunkten, en del av **Translate Spreadsheet API**, läser varje textelement i en arbetsbok, skickar innehållet till en AI-drivna översättningstjänst och returnerar en ny kalkylarkfil där all text har översatts till det angivna **targetLanguage**-målspråket. Operationen bevarar originalutseendet, cellstilar, formler och **den** strukturen över flera kalkylblad, vilket gör den idealisk för att globalisera rapporter, instrumentpaneler och datadrivna dokument. Stödda filformat inkluderar XLS, XLSX, XLSM, CSV och ODS. Fel returneras vid ogiltiga språkkoder, autentiseringsfel eller driftstörningar i översättningstjänsten.

## **Translate Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **Begärparametrar:**

| Parameternamn | Typ   | Plats    | Obligatoriskt/valfritt | Beskrivning                                                                                                                                                                                                 |
| :------------ | :---- | :------- | :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet   | Fil   | Obligatoriskt | FormData          | Den Excel-arbetsbok som ska översättas. Tillåtna filtillägg: .xls, .xlsx, .xlsm, .csv, .ods. Maximal filstorlek: 50 MB. Exempel: `budget.xlsx`.                                                               |
| targetLanguage | sträng | Obligatoriskt | Frågeparameter    | ISO 639‑1-språkkod för önskat utdataspråk (t.ex. "es" för spanska, "fr" för franska, "de" för tyska). Måste vara ett språk som stöds av den underliggande AI-tjänsten.                              |
| region        | sträng | Valfritt     | Frågeparameter    | Identifierare för kalkylarksregion som påverkar språk- och landspecifik formatering såsom datum, nummer och valuta. Vanliga värden: "US", "EU", "CN". Om utelämnas används arbetsbokens ursprungliga regionsinställning. |
| password      | sträng | Valfritt     | Frågeparameter    | Lösenord för att öppna en lösenordsskyddad arbetsbok. Lämna tomt om filen inte är lösenordsskyddad.                                                                                                             |

### **Svar**

Lyckat svar (200 OK)  
Headrar:  
Content‑Type: application/octet-stream // eller text/csv när CSV-utdata begärs  
Content‑Disposition: attachment; filename="translated.xlsx"  
Content‑Length: <storlek i byte>

Brödtext:  
<binär ström som innehåller den översatta kalkylarkfilen>

Felsvar följer standardfelmodellen för Aspose.Cells Cloud (application/json) med fälten `code`, `message` och valfria `details`.

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Översättning lyckades; svaret innehåller åtgärdens detaljer.      |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Obehörig              | Ogiltigt eller saknat JWT-token.                                  |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör man använda Translate Spreadsheet API?

- **Internationell finansrapportering** – Översätt kvartalsvisa Excel-rapporter till flera språk för regionala kontor, samtidigt som formler och diagramlayouter bevaras.
- **Mångspråkiga marknadsföringsinstrumentpaneler** – Generera automatiskt lokala versioner av säljprestandainstrumentpaneler för globala team.
- **Distribution av utbildningsinnehåll** – Översätt betygshandböcker, uppgiftsark eller läroplaner för elever i olika länder utan manuell kopiering och klistra in.
- **Föreskriftskompatibilitet** – Skapa språkspecifika kompatibilitetskalkylark som behåller valideringsregler och listor för datavalidering.

## Varför bör du använda Translate Spreadsheet API?

- **AI-driven noggrannhet** – Utnyttjar avancerade neurala översättningsmodeller för kontextmedveten, högkvalitativ språköversättning.
- **Ingen störning av layouten** – Bevarar cellformler, villkorsformatering, diagram och kalkylbladsordning exakt som i källfilen.
- **Flerkalkylbladsbearbetning med ett anrop** – Översätter alla kalkylblad i ett enda anrop, vilket eliminerar behovet av att loopa igenom varje kalkylblad för sig.
- **Sömlös molnintegration** – Fungerar med Aspose.Cells Cloud-autentisering och möjliggör automatiska pipeline i CI/CD, serverlösa funktioner eller företagsbakändssystem.

## Så här använder du Translate Spreadsheet API med SDK:er

### Specifikation för Translate Spreadsheet API

[Translate Spreadsheet API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den döljer de lågnivådetaljer som krävs och gör det möjligt att sammanfoga kalkylark med bara lite kod.  
Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.  
Följande kodexempel visar hur du interagerar med Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}