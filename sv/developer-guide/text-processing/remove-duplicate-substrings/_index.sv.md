---
title: "Aspose.Cells Cloud-tjänst för borttagning av dubblettsträngar – Deduplicera upprepade texter i Excel"
second_title: "Dokument"
ArticleTitle: "Excel-deduplicerare för dubblettsträngar – Rensa upprepad text i celler"
linktitle: "Ta bort dubblettsträngar"
type: docs
url: /remove-duplicate-substrings/
keywords: "Aspose.Cells, dubblettsträngar, Excel-API, textrenslighet, moln"
description: "Ta bort dubblettsträngar från Excel-cellerna via Aspose.Cells Cloud-API:et med bevarande av formatering och validering."
weight: 100
---

Ta bort dubblettsträngar från Excel-cellerna med intelligent detektering. Behåll originalformateringen oförändrad medan onödig text elimineras via Aspose.Cells deduplicerings-API.

## **Introduktion**: Ta bort onödiga tecken med precision

API:et för rensning av upprepade strängar tar bort dubblettsträngar inom individuella celler i ett Excel-område med bevarande av cellformatering, datavalidering och andra arbetsboksstrukturer. Den bearbetar varje cell oberoende och behåller bara den första förekomsten av varje dubblettsträng.


### **Alternativ för datakälla**

| Fält            | Typ   | Krävs | Beskrivning                                                      |
| --------------- | ----- | ----- | ---------------------------------------------------------------- |
| `workbook`      | fil   | Ja    | Excel-arbetsboksfil (.xlsx, .xlsm)                              |
| `range`         | sträng | Ja    | Målområde att bearbeta (t.ex. "A1:D100", "Sheet1!A:D")          |

### **Alternativ för avgränsare**

| Fält                              | Typ     | Standardvärde | Beskrivning                                                                                                                                                |
| --------------------------------- | ------- | ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `delimiters`                      | sträng  | `"preset"`    | Alternativ: `preset`, `custom`, `comma`, `semicolon`, `space`, `tab`, `line-break` eller en anpassad avgränsarsträng (flera tecken behandlas som en sammansatt) |
| `treatConsecutiveDelimitersAsOne` | boolean | `false`       | Kollapsa intilliggande avgränsare till en enda separator                                                                                                   |
| `caseSensitive`                   | boolean | `false`       | Avgör om jämförelsen är skiftlägeskänslig. När `false` ignoreras skiftläge vid identifiering av dubbletter.                                                |

## **RemoveDuplicateSubstrings API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:erna är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Requestparametrar för RemoveDuplicateSubstrings API**

| Parameternamn                   | Typ     | Path/Query String/HTTPBody | Beskrivning                                                                                                                                                                        |
| :------------------------------ | :------ | :------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet                     | Fil     | FormData                   | Den bearbetade filen. Stödda format inkluderar XLSX, XLS, ODS, CSV, etc.                                                                                                           |
| delimiters                      | Sträng  | Query                      | Anger ett eller flera avgränsartecken som används för att dela cellinnehåll i strängar för dubblettidentifiering och borttagning. Flera avgränsare kan anges (t.ex. `",;"`).         |
| treatConsecutiveDelimitersAsOne | Boolean | Query                      | När inställt på `true` behandlas på varandra följande avgränsartecken som en enda separator. När `false` bearbetas varje avgränsare individuellt.                                  |
| caseSensitive                   | Boolean | Query                      | När `true` beaktas skiftläge vid dubblettidentifiering (t.ex. "Text" ≠ "text"). När `false` ignoreras skiftläge vid jämförelse av dubbletter.                                        |
| worksheet                       | Sträng  | Query                      | _(Valfritt)_ Namnet på det kalkylblad där borttagning av dubblettsträngar ska appliceras. Om utelämnas appliceras operationen på det första kalkylbladet.                             |
| range                           | Sträng  | Query                      | _(Valfritt)_ Cellområdet där borttagning av dubblettsträngar ska appliceras (t.ex. `"A1:C10"`). Om utelämnas appliceras operationen på alla använda celler i det angivna kalkylbladet. |
| outPath                         | Sträng  | Query                      | _(Valfritt)_ Sökvägen till mappen i molnlagringen där den bearbetade arbetsboken kommer att sparas. Om utelämnas sparas filen i källmappen.                                        |
| outStorageName                  | Sträng  | Query                      | Namnet på molnlagringen där utdatafilen kommer att lagras.                                                                                                                         |
| region                          | Sträng  | Query                      | _(Valfritt)_ Anger lokalen för textbearbetning, vilket kan påverka tolkning av avgränsare och regler för skiftlägeskänslighet för vissa språk (t.ex. `"en-US"`, `"tr-TR"`).         |
| password                        | Sträng  | Query                      | _(Valfritt)_ Om den uppladdade arbetsboken är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                                                |

**Exempel på begäran (cURL)**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/remove/duplicate-substrings?delimiters=comma&caseSensitive=false" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Sample.xlsx" \
     -F "range=A1:D100"
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

### **Statuskoder**

| Kod | Betyder                                 | Beskrivning                                                                                      |
|-----|-----------------------------------------|--------------------------------------------------------------------------------------------------|
| 200 | OK                                      | Begäran lyckades och den bearbetade arbetsboken returneras.                                      |
| 202 | Accepterad                              | Begäran accepteras för asynkron bearbetning.                                                     |
| 400 | Felaktig begäran                        | Begäran är felaktigt formaterad eller innehåller ogiltiga parametrar.                           |
| 401 | Ej auktoriserad                         | Autentisering misslyckades eller token saknas/är ogiltig.                                       |
| 404 | Hittades inte                           | Den angivna arbetsboken eller resursen kunde inte hittas.                                        |
| 500 | Internt serverfel                       | Ett oväntat fel uppstod på serversidan.                                                          |

## Var bör vi använda API:et för borttagning av dubblettsträngar?

- **Scenario för datarenslighet och standardisering**: Städa upp taggar som `"VIP,Premium,VIP,Gold"` → `"VIP,Premium,Gold"`.
- **Teknisk och operativ data**: Städa loggposter med upprepade felkoder, ta bort dubbletter av bin/rack-identifikationer, etc.
- **Innehålls- och mediahantering**: Deduplicera färdighetsetiketter, ta bort onödiga certifieringsposter.

## Varför bör du använda API:et för borttagning av dubblettsträngar?

- **Automatisera manuella uppgifter**: Eliminera tröttsamma redigeringar och minska risk för människofel.  
- **Bevara dataintegritet**: Cellfärger, teckensnitt, ramar och villkorlig formatering förblir oförändrade; rullgardinslistor och valideringsregler bevaras.  
- **Flexibel bearbetning**: Avgränsaroberoende med valfri kontroll över skiftlägeskänslighet och rubrikskydd.  
- **Utvecklarvänlig**: Aspose.Cells Cloud tillhandahåller SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling med omfattande dokumentation.  
- **Kostnadseffektiv**: Operationen utförs i molnet, vilket undviker behovet av att lagra mellanliggande filer lokalt.  

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstrings) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Användning av SDK är det bästa sättet att snabba upp utvecklingen. SDK hanterar de underliggande detaljerna, så att du enkelt kan implementera borttagning av dubblettsträngar i celler med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

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
---