---
title: "Aspose.Cells Cloud Add Text API – Lägg till text i flera Excel-cellr samtidigt – Infoga prefix, suffix och etiketter"
second_title: "Dokument"
ArticleTitle: "Bulk-textinfogning för Excel – Lägg till prefix, suffix och anpassad text i celler – Steg-för-steg-guide"
linktype: "AddText"
type: docs
url: /sv/add-text/
keywords: "Aspose Cells API, lägg till text i Excel, bulk-textinfogning, prefix suffix Excel, ersätt text i kalkylblad, Excel-automatisering, moln-baserad kalkylblad-API"
description: "Infoga prefix, suffix eller anpassade etiketter i många Excel-cellr i ett enda anrop med Aspose.Cells Cloud. Välj början, slutet, före eller efter en viss text. Stöder intervall, kalkylblad och hantering av tomma celler."
weight: 100
---

Infoga text i flera Excel-cellr i ett enda åtgärd. Lägg till prefix, suffix, etiketter eller anpassade tecken i början, slutet eller före/efter en specifik text i cellerna med Aspose.Cells API.

## Översikt

Infoga prefix, suffix eller ankarsträngar i alla celler i ett målintervall med ett enda API-anrop – inga formler, inga hjälpspalter.

- Infoga anpassad text på **valfri position** i varje cell

| Värde            | Beskrivning                                                                 |
| ---------------- | --------------------------------------------------------------------------- |
| `None`           | Ersätt originalinnehållet                                                   |
| `AtTheBeginning` | Infoga i början (prefix)                                                    |
| `AtTheEnd`       | Infoga i slutet (suffix)                                                    |
| `BeforeText`     | Infoga **före** första förekomsten av `selectText`; hoppa över om inte hittad |
| `AfterText`      | Infoga **efter** första förekomsten av `selectText`; hoppa över om inte hittad |

- Fyra lägesalternativ: prefix, suffix, före/efter en delsträng.
- Hoppa över tomma celler för att undvika oönskad fyllning.
- API:t påverkar endast **strängtyps-värden**; tal, booleska värden och formler konverteras först till text.
- **Tomma celler**
  - `skipEmptyCells = true` → tomma celler hoppas över.
  - `skipEmptyCells = false` → text läggs till i tomma celler (cellen blir av typen text).

- **Ankaren hittas inte**: När `position = BeforeText | AfterText` och `selectText` **inte finns**, förblir cellens värde oförändrat.

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametrar för API:et **AddText** är

| Parameternamn   | Typ     | Path/Query String/HTTPBody | Beskrivning                                                                                                                                              | Krävs |
| :-------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- | :---- |
| Spreadsheet     | Fil     | FormData                   | Kalkylbladsfilen som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV, etc.                                                                  | Ja    |
| text            | Sträng  | Query                      | Den text som ska läggas till i de angivna cellerna i kalkylbladet.                                                                                      | Ja    |
| position        | Sträng  | Query                      | Anger var texten ska infogas i förhållande till befintligt cellinnehåll. Alternativ: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`. | Ja    |
| selectText      | Sträng  | Query                      | _(Valfritt)_ Om angiven läggs texten till endast i celler som innehåller exakt denna delsträng. Används tillsammans med parametern `position`.          | Nej   |
| skipEmptyCells  | Boolean | Query                      | Om `true` hoppas tomma celler över; om `false` läggs text till i tomma celler.                                                                           | Nej   |
| worksheet       | Sträng  | Query                      | _(Valfritt)_ Namnet på det kalkylblad där texten kommer läggas till. Om utelämnas tillämpas operationen på första kalkylbladet som standard.            | Nej   |
| range           | Sträng  | Query                      | _(Valfritt)_ Cellintervallet där texten kommer läggas till (t.ex. `"A1:C10"`). Om utelämnas tillämpas operationen på alla använda celler i angivet kalkylblad. | Nej   |
| outPath         | Sträng  | Query                      | _(Valfritt)_ Sökvägen till mappen i molnlagringen där den bearbetade arbetsboken sparas. Om utelämnas sparas filen i källmappen.                         | Nej   |
| outStorageName  | Sträng  | Query                      | Namnet på molnlagringen där utdatafilen kommer lagras.                                                                                                   | Nej   |
| region          | Sträng  | Query                      | _(Valfritt)_ Anger lokalspråk för formatering av tal, datum och valuta i utdatafilen (t.ex. `"sv-SE"`, `"en-US"`, `"zh-CN"`, `"de-DE"`).                 | Nej   |
| password        | Sträng  | Query                      | _(Valfritt)_ Om den uppladdade kalkylfilen är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                        | Nej   |

**cURL-exempel**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Rapport&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

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

| Kod | Beskrivning |
| --- | ----------- |
| **400** Bad Request | Ogiltig URI för Aspose.Cells Cloud API eller saknar nödvändiga parametrar. |
| **401** Unauthorized | Ogiltig access token eller ogiltigt klient-ID och hemlighet. |
| **404** Not Found | Kalkylbladsfilen är inte tillgänglig. |
| **500** Server Error | Kalkylbladet stötte på ett problem vid hämtning av beräkningsdata. |

## Var bör vi använda API:et för att lägga till text i kalkylblad?

- **Dynamisk rapportetikettering**: Lägg till dynamiska titlar, datumtaggar eller anteckningar i automatiskt genererade finansrapporter och försäljningsrapporter.
- **Bulk-filvattenstämplning**: Lägg till företagslogotyper, sekretessvattenstämplar eller versionsinformation i en batch Excel-filer.
- **Malldatautfyllnad**: Fyll automatiskt i kundnamn, belopp och annan text på fördefinierade positioner i kontrakt- eller fakturamallar.
- **Dataklassificeringsetikettering**: Lägg automatiskt till klassificeringsetiketter eller statusetiketter (t.ex. “Väntar på granskning”, “Godkänd”) i datarader baserat på analyseresultat.
- **Datakvalitetsanteckningar**: Lägg till anteckningar om problematisk data under datarengöring.
- **Bulk-textformatering**: Lägg enhetligt till prefix eller suffix till produktnamn eller kundnamn.

## Varför bör du använda API:et för att lägga till text i kalkylblad?

- **Bulk-textinfogning**: Lägg till text i hundratals celler eller filer samtidigt, vilket sparar upp till 95 % tid jämfört med manuellt arbete.
- **Exakt positionsstyrning**: Stöder infogning av text med hög precision på sex positioner, inklusive början, slutet eller före/efter specifik text i en cell.
- **Smart villkorshantering**: Bestäm om text ska läggas till beroende på om en cell är tom eller innehåller specifik text.
- **Stöd för flera positioneringsstrategier**:
  - `AtTheBeginning`: Lägg till samma text före innehållet i alla valda celler.
  - `AtTheEnd`: Lägg till text efter innehållet i alla valda celler.
  - `BeforeText` / `AfterText`: Lägg till text endast före eller efter celler som innehåller specifik text.
  - `None`: Ersätt originalinnehållet.
- **Exakt intervallstyrning**: Tillåter specifikation av specifika kalkylblad eller cellintervall för operationer.
- **Villkorsstyrning för att hoppa över**: Stöder att hoppa över tomma celler för att undvika onödig textinfogning.
- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskas utvecklingsarbetet avsevärt.
- **Kostnadseffektivt**: Du kan lägga till text i en cell utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar de underliggande detaljerna så att du enkelt kan implementera Add Text för celler med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells-webbtjänster med diverse SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---