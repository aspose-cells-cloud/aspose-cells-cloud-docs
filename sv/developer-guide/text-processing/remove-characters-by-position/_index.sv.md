---
title: "Aspose.Cells Cloud – Web API för att ta bort tecken efter position – Ta bort text från specifika platser i Excel"
second_title: "Dokument"
ArticleTitle: "Excel – teckenborttagare baserad på position – Ta bort text från specifika platser – Online-shortcode"
linktitle: "Ta bort tecken efter position"
type: docs
url: /sv/remove-characters-by-position/
keywords: "Aspose.Cells Cloud, ta bort tecken efter position, rensning av Excel-text, ta bort första N tecknen, ta bort sista N tecknen, ta bort text före markör, ta bort text efter markör, borttagning mellan värden"
description: "Använd Aspose.Cells Cloud Web API för att ta bort tecken från Excel-cellerna baserat på position – ta bort första/sista N tecknen eller text före/efter specifika markörer med hög precision."
weight: 100
---

Ta bort tecken från Excel-cellerna efter position: ta bort första/sista N tecknen, eller ta bort text före/efter angivna markörer. Exakt textrensning med Aspose.Cells Cloud Web API.


## **Introduktion**: Ta bort onödiga tecken efter position

**Positions lägen**

- `theFirstNCharacters` – ta bort N tecken från början
- `theLastNCharacters` – ta bort N tecken från slutet
- `allCharactersBeforeText` – ta bort allt före den första förekomsten av den angivna delsträngen
- `allCharactersAfterText` – ta bort allt efter den första förekomsten
- `BetweenValues` – ta bort delsträngen (och valfritt även avgränsarna själva) mellan två användardefinierade värden

**Alternativ**

- `caseSensitive` – bestämmer om sökningar efter `BeforeText`, `AfterText` och `BetweenValues` är skiftlägeskänsliga

## **RemoveCharactersByPosition API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:n är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begärandeparametrar för **RemoveCharactersByPosition** API:n är

| Parameternamn           | Typ     | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                                              |
| ----------------------- | ------- | --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Spreadsheet             | Fil     | FormData                    | Den kalkylbladsfil som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV, etc.                                                                                |
| Authorization           | Sträng  | Header                      | Bearer-token för autentisering (obligatorisk).                                                                                                                           |
| theFirstNCharacters     | Heltal  | Frågesträng                 | Antal tecken som ska tas bort från början av texten i varje vald cell (t.ex. `3` tar bort de första 3 tecknen).                                                         |
| theLastNCharacters      | Heltal  | Frågesträng                 | Antal tecken som ska tas bort från slutet av texten i varje vald cell (t.ex. `2` tar bort de sista 2 tecknen).                                                          |
| allCharactersBeforeText | Sträng  | Frågesträng                 | Tar bort alla tecken som förekommer före den angivna textsträngen i varje cell. Om texten förekommer flera gånger baseras borttagning på den första förekomsten.         |
| allCharactersAfterText  | Sträng  | Frågesträng                 | Tar bort alla tecken som förekommer efter den angivna textsträngen i varje cell. Om texten förekommer flera gånger baseras borttagning på den första förekomsten.        |
| worksheet               | Sträng  | Frågesträng                 | _(Valfritt)_ Namnet på kalkylbladet där teckenborttagning ska tillämpas. Om utelämnas tillämpas åtgärden på det första kalkylbladet.                                     |
| range                   | Sträng  | Frågesträng                 | _(Valfritt)_ Cellintervallet där teckenborttagning ska tillämpas (t.ex. `"A1:C10"`). Om utelämnas tillämpas åtgärden på alla använda celler i det angivna kalkylbladet.   |
| outPath                 | Sträng  | Frågesträng                 | _(Valfritt)_ Mappens sökväg i molnlagringen där den bearbetade arbetsboken kommer att sparas. Om utelämnas sparas filen i källmappen.                                   |
| outStorageName          | Sträng  | Frågesträng                 | Namnet på molnlagringen där utdatafilen kommer att lagras.                                                                                                               |
| region                  | Sträng  | Frågesträng                 | _(Valfritt)_ Anger lokalt språk för texthantering, särskilt relevant för språkspecifika teckenpositioner och kodning (t.ex. `"en-US"`, `"zh-CN"`).                     |
| password                | Sträng  | Frågesträng                 | _(Valfritt)_ Om den uppladdade kalkylbladsfilen är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                                 |

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

- **200 OK** – Begäran lyckades och den bearbetade filen returneras.
- **400 Bad Request**: Ogiltig Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Ogiltig åtkomsttoken eller ogiltigt klient-ID och hemlighet.
- **404 Not Found**: Kalkylbladsfilen är inte tillgänglig.
- **500 Server Error**: Ett fel uppstod i kalkylbladet vid hämtning av beräkningsdata.

## Var bör vi använda API:n för att ta bort tecken efter position?

- **Datastandardisering**: Rensa produktkoder (ta bort inledande nollor eller suffix), telefonnummer (ta bort landskoder)
- **Textextraktion**: Extrahera viktig information från loggfiler (ta bort tidsstämplar eller prefix)
- **Filbearbetning**: Organisera filnamn (ta bort enhetliga prefix eller datumsuffix)
- **Dataparsering**: Bearbeta strukturerad text (extrahera innehåll mellan hakparenteser eller specifika markörer)
- **Databashantering**: Rensa importerad data (ta bort tecken med fast format i rubrik/fot)

## Varför bör du använda API:n för att ta bort tecken efter position?

- **Exakt och effektiv**: Direkt positionsbaserad borttagning eliminerar behovet av komplexa reguljära uttryck.
- **Flexibel konfiguration**: Fem positionslägen plus ett skiftlägeskänsligt alternativ täcker många olika scenario.
- **Batchbearbetning**: Rensa hela kolumner med ett enda anrop, vilket ökar effektiviteten med upp till 10×.
- **Smart parsering**: Enkelt hantera extraktion av innehåll mellan två avgränsare.
- **Utvecklarvänlig**: Aspose.Cells Cloud tillhandahåller SDK:er för flera programmeringsspråk, vilket påskyndar utvecklingen och erbjuder omfattande dokumentation. Jämfört med att bygga egen textbearbetningslogik minskar detta utvecklingsarbetet betydligt.
- **Kostnadseffektiv**: Tecken kan tas bort utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharactersByPositionInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Användning av SDK:n är det bästa sättet att påskynda utvecklingen. SDK:n hanterar de underliggande detaljerna, så att du enkelt kan implementera borttagning av tecken efter position i celler med minimal kod.  
Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersByPosition.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersByPosition.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersByPosition.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersByPosition.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersByPosition.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersByPosition.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersByPosition.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersByPosition.go" >}}
{{</tab>}}
{{< /tabs >}}
---