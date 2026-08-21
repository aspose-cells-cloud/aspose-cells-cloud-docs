---
title: "Split Text API – Dela upp Excel-celler i kolumner | Aspose.Cells Cloud"
secondtitle: "Dokument"
ArticleTitle: "Excel Text Splitter – Dela upp cellinnehåll i flera kolumner | Aspose.Cells Cloud"
linktitle: "Dela text"
type: docs
url: /sv/split-text/
keywords: "Aspose, Cells, Split Text API, Excel, avgränsare, textsegmentering, molntjänst"
description: "Dela enkelt Excel-celltext i separata kolumner eller rader med Aspose.Cells Cloud. Stöder anpassade avgränsare, masker, radbrytningar och valfritt bibehållande av avgränsare. Kom igång med curl eller SDK:er på några minuter."
weight: 100
---

Dela upp Excel-celltext i flera kolumner med anpassade segmenteringsregler. Dela innehåll med avgränsare och skriv utresultatet till angivna interval med Aspose.Cells Cloud:s webb-API för textdelning.

## **Introduktion**: Dela text

API:et för textsegmentering delar upp cellinnehåll i flera celler baserat på angivna avgränsare, mönster eller radbrytningar och skriver ut resultaten till ett målområde. Det stöder flexibla delningsmetoder, riktad utmatning (kolumner eller rader) och alternativ för att bevara avgränsare – idealiskt för att tolka konkatenerad data, CSV-liknande innehåll eller flerradig text i strukturerade format.

- **Dela cell efter specifikt tecken** – bryt ner cellinnehåll i flera celler genom att välja ett valfritt tecken som avgränsare (komma, mellanslag, semikolon, etc.).
- **Dela celler efter sträng** – separera celler med en valfri kombination av tecken som du anger.
- **Dela text efter mask** – använd jokertecken för att dela upp text baserat på ett visst mönster, vilket erbjuder en ännu mer flexibel och kraftfull metod för textdelning.
- **Dela cellinnehåll efter radbrytning** – skapa en mer organiserad presentation genom att dela vid radbrytningar.
- **Dela celler i kolumner eller rader** – välj hur delningsresultaten ska skrivas: antingen i successiva kolumner eller rader.
- **Ta bort eller behåll avgränsare** – bestäm om avgränsarna ska tas bort eller behållas i början eller slutet av de resulterande cellerna.

## **SplitText API**

**Förutsättningar**: För att använda detta API behöver du ett giltigt Aspose Cloud-access-token, och arbetsboken som ska bearbetas måste laddas upp till Aspose Cloud-lagring eller tillhandahållas direkt i begäran. API:et stöder vanliga kalkylarkformat som XLSX, XLS, ODS och CSV.

### Web API

```http
POST https://api.aspose.cloud/v4.0/cells/content/split/text
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäraparametrar för **splitText** API:et

| Parameternamn                  | Typ     | Plats    | Obligatorisk? | Standardvärde  | Beskrivning                                                                                                                                         |
| ------------------------------ | ------- | -------- | ------------- | -------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet                    | Fil     | FormData | Ja            | —              | Kalkylarkfilen som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV, etc.                                                               |
| delimiters                     | Sträng  | Query    | Nej           | —              | En eller flera avgränsartecken som används för att dela upp text i celler (t.ex. `","`, `";"`, `Mellanslag`, `Radbrytning`, `Tab`, `Pipe`, `Anpassad`). |
| keepDelimitersInResultingCells | Boolean | Query    | Nej           | false          | När satt till `true` behålls avgränsartecknen i de resulterande delade cellerna.                                                                   |
| keepDelimitersPosition         | Sträng  | Query    | Nej           | None           | Var avgränsarna ska behållas om `keepDelimitersInResultingCells` är `true`. Alternativ: `None`, `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`. |
| howToSplit                     | Sträng  | Query    | Nej           | SplitToColumns | Metod för textsegmentering. Alternativ: `None`, `SplitToColumns`, `SplitToRows`.                                                                   |
| outPositionRange               | Sträng  | Query    | Ja            | —              | Måломråde där delningsresultaten ska skrivas (t.ex. `"D1:F10"`).                                                                                    |
| worksheet                      | Sträng  | Query    | Nej           | —              | Namn på kalkylbladet där textdelning ska tillämpas. Om utelämnas används det första kalkylbladet.                                                   |
| range                          | Sträng  | Query    | Nej           | —              | Källcellområde till vilket delningsåtgärden tillämpas (t.ex. `"A1:A10"`). Om utelämnas bearbetas alla använda celler i kalkylbladet.                 |
| outPath                        | Sträng  | Query    | Nej           | —              | Lagringsmappsökväg i molnet där den bearbetade arbetsboken sparas. Om utelämnas sparas filen i källmappen.                                           |
| outStorageName                 | Sträng  | Query    | Nej           | —              | Namn på molnlagringen där utdatafilen ska lagras.                                                                                                   |
| region                         | Sträng  | Query    | Nej           | —              | Språkinställning för textsegmentering, vilket kan påverka tolkning av avgränsare och teckenkodning (t.ex. `"en-US"`, `"ja-JP"`).                      |
| password                       | Sträng  | Query    | Nej           | —              | Lösenord för att öppna ett lösenordsskyddat kalkylark.                                                                                              |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Felkoder

- **400 Bad Request** – Ogiltig Aspose.Cells Cloud API-URI eller felaktigt formaterade parametrar.
- **401 Unauthorized** – Saknat eller ogiltigt access-token (eller client-id/secret).
- **404 Not Found** – Den angivna kalkylarkfilen kunde inte nås.
- **500 Server Error** – Ett internt bearbetningsfel uppstod i kalkylarket.

## Var bör vi använda Split Text API:et?

### **CSV & Textfilimportrensning**

Vid import av data från externa system ofta sammanfogas fält till en enda cell:

- **ERP/CRM-dataimporter** – dela upp `"John Doe;johndoe@email.com;555-1234"` i separata kolumner för namn, e-post och telefonnummer.
- **Databasexporter** – tolka kombinerade nycklar som `"ORD-2024-001|Premium|Express"` i ordernummer, nivå och fraktmetod.
- **Loggfilanalys** – dela upp semi-strukturerade loggar som `"2024-01-15 10:30:00|ERROR|ConnectionTimeout"` för filtrering.

### **Migration av äldre system**

- Gamla system dumpar flervärdesfält i en enda cell; dela upp dem för att matcha nya databasscheman.
- Konvertera flat-filexporter till normaliserade Excel-tabeller redo för Power BI eller Tableau.

### **Datarensering & standardisering**

- **Avgränsarnormalisering** – konvertera blandade avgränsare (`"A,B;C|D"`) till ett enhetligt format med flera avgränsares delning.
- **Mellanslagsrensning** – dela upp med mellanslag för att identifiera och ta bort extra mellanslag mellan ord.
- **Finansiell data** – dela upp kombinerade transaktionskoder som `"DEP-CHK-3847"` i transaktionstyp, källa och referens.
- **Medicinska journaler** – tolka patientdata som `"Smith,Jane_F_1985"` i efternamn, förnamn, kön och födelseår.

## Varför bör du använda Split Text API:et?

- **Specifika tecken** – dela upp med valfritt enkelt tecken (komma, semikolon, tab, mellanslag).
- **Strängkombinationer** – använd flerteckensavgränsare som `||`, `->` eller anpassade separatorer.
- **Radbrytningar** – tolka flerradiga celler direkt i separata rader (adresser, kommentarer, beskrivningar).
- **Anpassade avgränsare** – definiera valfri teckenkombination som avgränsare för egna datformat.
- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och följs med omfattande dokumentation. Jämfört med att bygga egna lösningar minskas utvecklingsarbete betydligt.
- **Kostnadseffektivt** – du kan ta bort dubletter utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnader.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/SplitText) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Användning av SDK är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, så att du enkelt kan implementera textdelning för celler med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitText.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitText.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitText.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitText.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitText.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitText.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitText.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitText.go" >}}  
{{</tab>}}  
{{< /tabs >}}
---