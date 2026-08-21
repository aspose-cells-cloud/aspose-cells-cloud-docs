---
title: "Sök text i fjärranslutna Excel-arbetsböcker – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Sök text i fjärranslutna Excel-arbetsböcker – Hitta specifik data"
linktitle: "Sök i innehåll i fjärranslutna kalkylark"
type: docs
url: /sv/search-content-in-remote-spreadsheet/
keywords: "Aspose.Cells, Excel-söknings-API, molnkalkylark, textsökning, REST"
description: "Sök efter text, nummer eller formler i Excel-filer lagrade i molnlagring med Aspose.Cells Cloud. Stöder skiftlägesokänsliga frågor, val av mapp och lösenordsskyddade arbetsböcker."
weight: 100
---

### **Sök i innehåll i fjärranslutna kalkylark via API**

Sök programmatiskt efter specifik text i valfritt Excel-kalkylark med Aspose.Cells Cloud API. Hitta text, nummer eller formler i filer som lagras i molnlagring. Detta REST-baserade API möjliggör automatiserad dataupptäckt, innehållsanalys och arbetsflöden för granskning av kalkylark.

### **Webb-API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/content
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Förfrågningsparametrar:**

| Parameternamn    | Typ     | Väg/Förfrågningssträng/HTTPBody | Beskrivning                                                                                                                                                      |
| :--------------- | :------ | :----------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name             | Sträng  | Väg                            | **Obligatoriskt**. Filnamnet på Excel-arbetsboken (inklusive tillägg) där textsökningen ska utföras, t.ex. `sales_data.xlsx`.                                 |
| searchText       | Sträng  | Förfrågningssträng             | **Obligatoriskt**. Den exakta strängen, siffan eller del av innehållet som ska hittas i hela arbetsboken eller i ett eller flera kalkylblad.                     |
| ignoringCase     | Boolean | Förfrågningssträng             | **Valfritt**. Bestämmer om skiftlägeskänslighet ska användas. Ställ in på `true` för skiftlägesokänslig sökning (t.ex. matchar “Report” även “REPORT”); standard är `false`. |
| folder           | Sträng  | Förfrågningssträng             | **Valfritt**. Mappsökvägen i din molnlagring som innehåller målarbetsboken. Om utelämnad antas rotmappen.                                                       |
| storageName      | Sträng  | Förfrågningssträng             | **Valfritt**. Namnidentifierare för en anpassad molnlagringstjänst. Om inte angiven använder API:et standardlagring kopplad till kontot.                       |
| region           | Sträng  | Förfrågningssträng             | **Valfritt**. Språkinställning (t.ex. `sv-SE`) som tillämpas under sökningen, vilken kan påverka textnormalisering eller sorteringsregler.                      |
| password         | Sträng  | Förfrågningssträng             | **Valfritt**. Lösenord för dekryptering som krävs för att komma åt ett lösenordsskyddat Excel-dokument. Utelämna denna parameter om filen inte är krypterad.   |

**Glosor**

- **searchText** – Den exakta strängen att hitta; kan vara en delmatchning.
- **ignoringCase** – `true` gör sökningen skiftlägesokänslig; `false` tvingar skiftlägeskänslighet.
- **folder** – Sökväg till mappen som innehåller arbetsboken.
- **storageName** – Identifierare för en anpassad lagringskonfiguration.
- **region** – Språkkod som påverkar regler för textjämförelse.
- **password** – Dekrypteringslösenord för skyddade arbetsböcker.

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "sträng",
      "Worksheet": "sträng",
      "Position": "sträng",
      "Content": "sträng"
    }
  ]
}
```

Svaret innehåller en lista över celler (`CellName`) där den sökta texten hittades, tillsammans med kalkylbladsnamn och matchande text. Om inga matchningar hittas är `TextItems`-arrayen tom och förfrågan returnerar ändå HTTP 200 OK.

### Felkoder

- **400 Bad Request** – Ogiltig URI för Aspose.Cells Cloud API.  
  ```json
  {"code":400,"message":"Invalid request URI"}
  ```
- **401 Unauthorized** – Ogiltig åtkomsttoken, klient-ID eller klienthemlighet.  
  ```json
  {"code":401,"message":"Invalid access token"}
  ```
- **404 Not Found** – Kalkylarkfilen är inte tillgänglig.  
  ```json
  {"code":404,"message":"File not found"}
  ```
- **500 Server Error** – Ett oväntat tillstånd hindrade API:et från att slutföra förfrågan.  
  ```json
  {"code":500,"message":"Internal server error"}
  ```

## Var bör vi använda sökfunktionen i Spreadsheet API?

- **Omfattande revision av arbetsbokens följsamhet** – Skanna snabbt hela Excel-filen för att identifiera alla känsliga termer (t.ex. “Konfidentiell klausul”, “Internt data”) för företagsdata säkerhets- och följsamhetskontroller.
- **Fråga om datakoppling mellan kalkylblad** – När projektinformation är spridd över flera kalkylblad, sök efter ett specifikt projektnummer eller kundnamn och omedelbart hitta all relevant data.
- **Batchgranskning av mallinnehåll** – Efter automatisk rapportgenerering, skanna flera Excel-filer i batch för att bekräfta att alla förinställda platshållare (t.ex. `{{Datum}}`) har korrekt ersatt, vilket garanterar rapportens kompletthet och korrekthet.
- **Historisk dataarkivering och utvinning** – Analysera äldre filer, sök efter specifika händelsekoder eller affärs termer, och snabbt förstå historisk affärslogik för datadiggravering.

## Varför bör du använda sökfunktionen i Spreadsheet API?

- **Utvecklarvänlig** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling med omfattande dokumentation. Jämfört med att bygga anpassade lösningar minskas utvecklingsinsatsen avsevärt.
- **Lägre arbetskostnad** – Automatiserar upprepade sökuppgifter och frigör utvecklare från manuell dataextraktion.
- **Betala per användning** – Inga upfront-kostnader; du betalar endast för de API-anrop du faktiskt använder.
- **Ingen underhållsbehov** – Aspose hanterar servrar, uppdateringar och kompatibilitet, så du kan fokusera på din applikations logik.
- **Bevarar avancerat Excel-format** – Resultat kan exporteras till universellt tillgängligt PDF-format och behålla originalstilen.

## Hur man använder sökfunktionen i Spreadsheet API med SDK:er

### OpenAPI-specifikation

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteSpreadsheet" rel="noopener noreferrer">OpenAPI-specifikation</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera sökning i innehåll i kalkylark med minimal kod. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur Aspose.Cells-webbtjänster anropas med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}