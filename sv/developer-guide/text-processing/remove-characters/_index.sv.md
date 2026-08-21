---
title: "Aspose.Cells Cloud Remove Characters Web API – Ta bort anpassade tecken och delsträngar från Excel (Online Short‑Code)"
second_title: "Dokument"
ArticleTitle: "Excel Text Cleaner – Ta bort tecken och delsträngar från valt område"
linktitle: "Ta bort tecken"
type: docs
url: /sv/remove-characters/
keywords: "Aspose.Cells, ta bort tecken, Excel API, textrengöring, kalkylark"
description: "Ta bort anpassade tecken, teckenuppsättningar och delsträngar från Excel-cellerna i ett valt område. Ta bort text på specifika positioner med Aspose.Cells API för exakt datarengöring."
weight: 100
---

Rengör Excel-data genom att ta bort anpassade tecken, teckenuppsättningar eller delsträngar från ett valt cellområde. Ta bort text på specifika positioner med Aspose.Cells API för exakt dataformatering.

## Introduktion

Rengör och standardisera enkelt din Excel-data genom att ta bort specifika, oönskade tecken. Vårt tillägg erbjuder flera målriktade sätt att rengöra dina celler:

- **Ta bort anpassade tecken**  
  Ta bort alla specifika symboler du definierar. Ange helt enkelt varje tecken i fältet, så tar tillägget bort alla förekomster direkt från dina valda celler. Perfekt för att eliminera unika avgränsare, stavfel eller specialtecken.

- **Ta bort teckenuppsättningar (massrengöring)**
  - **Icke-utskrivna tecken** – Rengör din data från osynliga tecken som stör analys och formatering (radbrytningar, vagnreturer, tabulatorer och andra kontrolltecken såsom ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Texttecken (alla bokstäver)** – Isolera siffror och symboler genom att ta bort alla bokstäver (A‑Z, a‑z) från det valda området.
  - **Siffratecken (alla siffror)** – Extrahera ren text genom att ta bort alla siffror (0‑9), vilket är idealiskt för att rengöra produktnamn eller textbeskrivningar.
  - **Symboler** – Ta bort ett stort antal symboler, inklusive matematiska (t.ex. ±, √), geometriska (t.ex. ∆, °), tekniska, valuta (t.ex. £, ¢) och bokstavsliknande symboler (t.ex. ™, ®, ©).
  - **Skiljetecken** – Skapa rensad text utan skiljetecken genom att ta bort alla skiljetecken såsom punkter, kommatecken, citationstecken och bindestreck.

- **Ta bort en specifik delsträng**  
  Gå vidare än enskilda tecken och ta bort hela ord eller specifika tecken sekvenser. Ta bort vanliga prefix, suffix eller andra onödiga textfraser enkelt från dina dataset.

**Version 4.0 – Uppdaterad 2024‑11‑15**

## RemoveCharacters API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud APIs är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäran parametrar

| Parameter Name    | Typ    | Plats              | Beskrivning                                                                                                                                                                                                                      |
| ----------------- | ------ | ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet       | Fil    | FormData           | Kalkylarkfilen som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV, etc.                                                                                                                                             |
| removeTextMethod  | Sträng | Frågeparameter       | Anger metoden för textborttagning. Alternativ: `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. Standard är `None`.                                                                                 |
| characterSets     | Sträng | Frågeparameter       | Fördefinierade teckenuppsättningar att ta bort när `RemoveCharacterSets` är valt. Alternativ: `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. Flera uppsättningar kan kombineras med kommatecken. |
| removeCustomValue | Sträng | Frågeparameter       | Anpassade tecken eller delsträngar att ta bort vid användning av `RemoveCustomCharacter` eller `RemoveSubString`.                                                                                                              |
| worksheet         | Sträng | Frågeparameter _(valfritt)_ | Namnet på det kalkylblad där textborttagning ska utföras. **Om utelämnas bearbetas det första kalkylbladet i arbetsboken.**                                                                                                     |
| range             | Sträng | Frågeparameter _(valfritt)_ | Cellområdet där textborttagning ska utföras (t.ex. `"A1:C10"`). **Om utelämnas tillämpas åtgärden på alla använda celler i det angivna kalkylbladet.**                                                                          |
| outPath           | Sträng | Frågeparameter _(valfritt)_ | Sökväg till mapp i molnlagring där den bearbetade arbetsboken kommer att sparas. Om utelämnas sparas filen i källmappen.                                                                                                         |
| outStorageName    | Sträng | Frågeparameter _(valfritt)_ | Namnet på molnlagringen där utdatafilen kommer att lagras.                                                                                                                                                                      |
| region            | Sträng | Frågeparameter _(valfritt)_ | Anger regional inställning för teckenuppsättningsdefinitioner (t.ex. `"en-US"`, `"ja-JP"`).                                                                                                                                      |
| password          | Sträng | Frågeparameter _(valfritt)_ | Lösenord för en skyddad arbetsbok, om krävs.                                                                                                                                                                                    |

### Svar

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

- **400 Bad Request** – Ogiltig Aspose.Cells Cloud API URI.
- **401 Unauthorized** – Ogiltig åtkomsttoken eller felaktigt klient-ID och hemlighet.
- **404 Not Found** – Kalkylarkfilen är inte tillgänglig.
- **500 Server Error** – Kalkylarket stötte på ett fel vid hämtning av beräkningsdata.

## Var bör du använda Remove Characters API?

- **Dataimport/-export** – Rengör importerade CSV/data genom att ta bort osynliga tecken och formateringsfel.
- **Databashantering** – Standardisera produktkoder, ID-nummer och namn genom att ta bort oönskade symboler eller skiljetecken.
- **Finansiell analys** – Extrahera renta siffror genom att ta bort valutatecken och texttecken.
- **Textbehandling** – Ta bort radbrytningar och tabulatorer för ren textanalys och rapportering.
- **Lagerhantering** – Rengör produktnamn genom att ta bort onödiga prefix eller suffix.

## Varför använda Remove Characters API?

- **Spara tid** – Ta bort flera typer av tecken i massor direkt istället för manuell rengöring.
- **Säkerställa noggrannhet** – Eliminera dolda tecken som orsakar analysfel och formateringsproblem.
- **Standardisera data** – Uppnå konsekvent formatering över dataset och system.
- **Förbättra analys** – Få ren, analysklar data genom att isolera siffror eller text enligt behov.
- **Fixa importfel** – Ta bort problematiska tecken som bryter databaser och formler.
- **Utvecklarvänlig** – Aspose.Cells Cloud tillhandahåller SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling med omfattande dokumentation. Jämfört med att bygga egna lösningar minskar detta avsevärt utvecklingsarbete.
- **Kostnadsbesparande** – Ta bort tecken utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnader.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att snabba upp utvecklingen. SDK hanterar underliggande detaljer och låter dig implementera **Ta bort tecken** för celler med minimal kod. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}