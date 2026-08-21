---
title: "Sök i kalkylbladsinnehåll – Aspose.Cells Cloud API (Sök text i Excel)"
second_title: "Dokument"
ArticleTitle: "Sök text i lokala Excel-kalkylblad – Hitta specifik data"
linktitle: "Sök i kalkylbladsinnehåll"
type: docs
url: /search-spreadsheet-content/
keywords: "Aspose.Cells, Excel-söknings-API, sökning i kalkylbladsinnehåll, moln-baserat kalkylblads-API, textuppslag"
description: "Använd Aspose.Cells Cloud API för att söka efter text, nummer eller formler i lokala Excel-filer. Stöder skiftlägesokänsliga frågor, arbetsbladsnivåns sökomfattning och säker autentisering."
weight: 100
---

## **Sök i kalkylbladsinnehåll API**

Sök programmässigt efter specifik text i valfritt Excel-kalkylblad med Aspose.Cells Cloud API. API:t kan hitta text, nummer eller formler i lokala filer som lagras i molnet, vilket möjliggör automatiserad dataupptäckt, innehållsanalys och arbetsflöden för granskning av kalkylblad.

### **Webb-API**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

Om du föredrar att använda rå HTTP visar följande cURL-exempel samma begäran:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begärandeparametrar**

| Parameter    | Typ     | Plats    | Beskrivning                                                                                 |
| ------------ | ------- | -------- | ------------------------------------------------------------------------------------------- |
| spreadsheet  | Fil     | FormData | Excel-filen som ska genomsökas.                                                              |
| searchText   | Sträng  | Fråga    | Texten (eller numeriska värdet) som ska hittas i arbetsboken.                                |
| ignoringCase | Boolesk | Fråga    | Ställ in till `true` för att utföra en skiftlägesokänslig sökning.                          |
| worksheet    | Sträng  | Fråga    | Namnet på arbetsbladet som ska begränsa sökningen. Om utelämnas skannas alla arbetsblad.     |
| cellArea     | Sträng  | Fråga    | Ett intervall i A-1-format (t.ex. `A1:C10`) som begränsar sökområdet.                        |
| region       | Sträng  | Fråga    | Geografisk region för tjänsten (t.ex. `us-east-1`).                                         |
| password     | Sträng  | Fråga    | Lösenord som krävs för att öppna en skyddad arbetsbok.                                       |

### **Svar**

API:t returnerar ett `SearchResult`-objekt som innehåller ett fält med matchande celler. Varje element innehåller arbetsbladsnamn, celladress och den matchade texten.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### Felkoder

- **400 Bad Request** – Begärandets URI eller parametrar är ogiltiga.
- **401 Unauthorized** – Saknad eller ogiltig åtkomsttoken eller felaktiga klientuppgifter.
- **404 Not Found** – Det angivna kalkylbladet kan inte nås.
- **500 Internal Server Error** – Ett oväntat serverfel uppstod vid bearbetning av arbetsboken.

## Var bör vi använda sökfunktionen för innehåll i kalkylblad?

- **Omfattande granskning av arbetsbokens överensstämmelse** – Skanna hela arbetsboken för att hitta känsliga termer (t.ex. "Konfidentiell klausul", "Internt data") för säkerhets- och överensstämmelsekontroller av data.
- **Fråga om quersheet-datakoppling** – Hitta ett projektnummer eller ett kundnamn som förekommer på flera arbetsblad, vilket möjliggör snabb quersheet-integration.
- **Batchverifiering av mallinnehåll** – Efter generering av rapporter, verifiera att alla platshållare som `{{Date}}` har ersatts korrekt i en hel batch Excel-filer.
- **Arkivering och utvinning av historisk data** – Sök i äldre Excel-filer efter specifika händelsekoder eller affärstermer för att påskynda data-arkeologi och analys.

## Varför bör du använda sökfunktionen för innehåll i kalkylblad?

- **Utvecklarvänlig** – SDK:er finns för många språk, vilket minskar utvecklingsarbetet jämfört med att bygga en anpassad lösning.
- **Minskat arbetskostnad** – Automatiserar uppgifter som annars kräver manuell granskning av kalkylblad.
- **Betala per användning** – Du betalar endast för de API-anrop du faktiskt gör.
- **Ingen underhållsbelastning** – Inga servrar att hantera, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.
- **Bevarar komplex formatering** – Resultaten kan exporteras till PDF med originalutseendet i Excel bevarat.

## Hur man använder sökfunktionen för trasiga länkar i kalkylblad med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Användning av en SDK är det snabbaste sättet att integrera sökfunktionen. SDK:n abstraher HTTP-lagret, så att du kan anropa API:t med minimal kod. Se den fullständiga listan över SDK:er i [GitHub-repositoriet](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur man anropar operationen Sök i kalkylbladsinnehåll med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
---