---
title: "Aspose.Cells Cloud Web API – Översätt textfil med AI-drivna språkkonverteringar"
secondtitle: "Dokument"
ArticleTitle: "Hur man översätter textfiler med Aspose.Cells Cloud AI-översättnings-API"
linktitle: "Översätt textfil"
type: docs
url: /translate-text-file/
keywords: "Aspose.Cells, Cloud API, AI-översättning, översätt textfil, multilingual konvertering, REST PUT, målspråkskod, filuppladdningsöversättning, översättning av ren text, kalkylblad AI"
description: "Lär dig hur du använder Aspose.Cells Cloud AI TranslateTextFile-slutpunkten för att konvertera textfiler till valfritt stödd språk. Stödjer både multipart-filuppladdning och ren text i förfrågansbrödtext, bevarar formatet och returnerar en nedladdningsbar översatt fil."
weight: 100
---

**TranslateTextFile**-slutpunkten använder Aspose.Cells Cloud AI-tjänster för att översätta innehållet i en textfil till ett angivet målspråk. Den stöder två driftlägen: (1) **Filuppladdningsläge** – skicka en textfil via multipart/form-data och få en översatt fil i returen; (2) **Direktinnehållsläge** – skicka ren text i förfrågansbrödtext och få den översatta texten direkt. Tjänsten bevarar ursprungliga radbrytningar och format, lägger automatiskt till suffixet "_translated" till filnamnet och returnerar resultatet som en nedladdningsbar ström. Idealiskt för batchöversättning av dokument, integration i multilingual arbetsflöden eller just-i-tid-översättning av användarskapat innehåll.

## **Översätt Textfil API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **Förfrågningsparametrar:**

| Parameter Name | Typ    | Plats   | Obligatoriskt/Valfritt | Beskrivning                                                                                                                                                                                                 |
| :------------- | :----- | :------ | :-------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | Obligatoriskt | FormData          | Källtextfilen som ska översättas. Måste vara en ren text (.txt) eller ett stödd kalkylbladsformat. Exempel: ladda upp `document.txt` via multipart/form-data-fältet med namnet "file".                              |
| targetLanguage | Sträng | Obligatoriskt | Frågeparameter    | ISO-639-1-språkkod för önskat utdataresultat (t.ex. "es" för spanska, "fr" för franska, "de" för tyska). Koden är skiftlägesokänslig.                                                                     |
| region         | Sträng | Valfritt   | Frågeparameter    | Kalkylbladsregionidentifierare som påverkar lokalspecifika format som datum, nummer och valuta. Vanliga värden: "US", "EU", "CN". Om utelämnas används arbetsbokens ursprungliga regionsinställning. |
| password       | Sträng | Valfritt   | Frågeparameter    | Lösenord som krävs för att öppna krypterade kalkylbladsfiler. Behövs inte för ren textfiler.                                                                                                                     |

### **Svar**

Lyckat svar (200 OK)
Headers:
Content-Type: application/octet-stream // binär ström av den översatta filen
Content-Disposition: attachment; filename="<original_name>\_translated.txt"
Content-Length: <storlek i byte>

Body: binär ström innehållande den översatta texten, med bevarade ursprungliga radbrytningar och format.

**HTTP-statuskoder**

| Kod | Betydelse               | Beskrivning                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Översättningen lyckades; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig förfrågan           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).      |
| 401  | Auktorisering saknas          | Ogiltigt eller saknat JWT-token.                                     |
| 413  | För stor förfrågning         | Den uppladdade filen överskrider storleksgränsen.                                 |
| 500  | Internt serverfel | Oväntat serverfel.                                          |

## Var bör man använda API:et för att översätta textfiler?

- **Multilinguella dokumentationsportaler** – Översätt automatiskt användarmanualer eller hjälpfiler som laddats upp som textdokument och leverera lokaliserade versioner vid behov.
- **Innehållshanteringssystem (CMS)** – Integrera i ett CMS-arbetsflöde för att översätta blogginlägg eller artiklar innan publicering till internationella målgrupper.
- **Enterprise-datapipelines** – Använd i batchjobb som bearbetar stora mängder CSV- eller TXT-rapporter och konverterar dem till språket för regionala kontor, samtidigt som ursprungliga format bevaras.
- **Kundtjänstplattformar** – Översätt inkommande textbaserade ärenden eller chattloggar i realtid för att stödja supportmedarbetare som jobbar i olika språk.

## Varför bör man använda API:et för att översätta textfiler?

- **AI-drivna översättningskvalitet** – Använder moderna neurala översättningsmodeller för naturliga, sammanhangsbaserade översättningar.
- **Dubbel indataflexibilitet** – Akterar både filuppladdning och ren text i förfrågansbrödtext, vilket förenklar integration med diverse klientapplikationer.
- **Bevarar ursprungligt layout** – Behåller radbrytningar, indrag och specialtecken, vilket eliminierar efterbehandlingsbehov.
- **Sömlös filhantering** – Returnerar en klart nedladdningsbar fil med automatiskt genererat "_translated"-suffix, vilket minskar komplexiteten i klientkoden.

## Hur man använder API:et för att översätta textfiler med SDK:er

### API-specifikation för Översätt Textfil

[API-specifikation för Översätt Textfil](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraherar bort de detaljerade nivåerna, vilket gör det möjligt att sammanfoga kalkylblad med kort kod.
Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.
Följande kodexempel visar hur man interagerar med Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}