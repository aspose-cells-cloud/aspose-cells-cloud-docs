---
title: "Aspose.Cells Cloud Web API – Konvertera text till tal i Excel och rensa specialtecken"
secondtitle: "Dokument"
articletitle: "Excel-datarenare – Konvertera text till tal och ta bort onödiga tecken"
linktitle: "Konvertera text"
type: docs
url: /sv/convert-text/
keywords: "Aspose.Cells konvertera text, Excel text till tal, ta bort specialtecken Excel, ersätt radbrytningar Excel, normalisera accenterade tecken, Excel datarenings-API"
description: "Konvertera textformaterade tal till numeriska värden, ersätt onödiga tecken och radbrytningar samt normalisera accenterade tecken i Excel-filer med Aspose.Cells Cloud API."
weight: 100
---

Rensa Excel-data genom att konvertera textformaterade tal till numeriska värden, ersätta onödiga tecken och radbrytningar samt normalisera accenterade tecken till vanliga bokstäver med Aspose.Cells API.

## Översikt

**Konvertera tal som text, ta bort skräp, byt ut accenter – ett anrop, noll formler.**

- **Konvertera tal som lagras som text till tal**: Omvandla numerisk data lagrad som text till riktiga tal, vilket säkerställer exakta beräkningar och korrekt datadistribution.
- **Ersätt specifika tecken**: Ersätt alla förekomster av angivna tecken i valda celler samtidigt för att standardisera din data.
- **Konvertera radbrytningar till mellanslag, komma eller semikolon**: Förbättra läsbarheten genom att ersätta radbrytningar med mellanslag, kommatecken eller semikolon, vilket skapar en mer organiserad och visuellt tilltalande presentation.
- **Ersätt accenterade tecken**: Om din data är på olika språk kan du byta ut accenterade tecken som "é" eller "ü" mot deras icke-accenterade motsvarigheter, vilket förbättrar konsistens och tydlighet.

## **ConvertText API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/convert/text
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begärandeparametrar för **convertText** API är

| Parameternamn    | Typ    | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                                            |
| ---------------- | ------ | --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fil    | FormData                    | Den kalkylbladsfil som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV, etc.                                                                              |
| convertTextType  | Sträng | Frågesträng                 | Anger vilken typ av textkonvertering som ska tillämpas, t.ex. konvertera textformaterade tal till numeriska värden eller konvertera accenterade tecken till vanliga ekvivalenter. |
| sourceCharacters | Sträng | Frågesträng                 | Anger tecken, strängar eller mönster som ska ersättas eller tas bort från texten (t.ex. `"é,è,ê"`, `"#N/A"`, `"\\n"` för radbrytningar).                               |
| targetCharacters | Sträng | Frågesträng                 | Anger ersättningstecken eller strängar som ska ersätta källtecknen (t.ex. `"e"` för accenterade bokstäver, `""` för borttagning, `" "` för radbrytningar).             |
| worksheet        | Sträng | Frågesträng                 | _(Valfritt)_ Namnet på kalkylbladet där textkonvertering ska tillämpas. Om utelämnas tillämpas åtgärden på det första kalkylbladet.                                    |
| range            | Sträng | Frågesträng                 | _(Valfritt)_ Cellomfånget där textkonvertering ska tillämpas (t.ex. `"A1:C10"`). Om utelämnas tillämpas åtgärden på alla använda celler i det angivna kalkylbladet.     |
| outPath          | Sträng | Frågesträng                 | _(Valfritt)_ Sökvägen till molnlagringsmappen där den bearbetade arbetsboken kommer att sparas. Om utelämnas sparas filen i källmappen.                                |
| outStorageName   | Sträng | Frågesträng                 | Namnet på molnlagringen där utdatafilen kommer att lagras.                                                                                                            |
| region           | Sträng | Frågesträng                 | _(Valfritt)_ Anger lokalt språk för textkonverteringsregler, särskilt relevant för språkspecifik teckenhantering (t.ex. `"sv-SE"`, `"fr-FR"`).                        |
| password         | Sträng | Frågesträng                 | _(Valfritt)_ Om den uppladdade kalkylfilen är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                                     |

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

- **400 Bad Request (Ogiltig begäran)**: Ogiltig Aspose.Cells Cloud API-URI.
- **401 Unauthorized (Ej auktoriserad)**: Ogiltig åtkomsttoken eller ogiltigt klient-ID och hemligt nyckelord.
- **404 Not Found (Hittades inte)**: Kalkylbladsfilen är inte tillgänglig.
- **500 Server Error (Serverfel)**: Kalkylbladet stötte på ett fel medan beräkningsdata hämtades.

## Var bör vi använda Convert Text API?

- **Korrigering av talformat**: Konvertera tal som lagras som text (t.ex. "123,45") till numeriskt format lämpligt för beräkningar.
- **Rensning av specialtecken**: Ta bort onödiga specialsymboler, extra mellanslag eller osynliga tecken från data.
- **Radbrytningshantering**: Ersätt radbrytningar i celler med mellanslag eller andra avgränsare.
- **Normalisering av accenterade tecken**: Konvertera accenterade bokstäver (t.ex. "é", "ñ") till vanliga bokstäver ("e", "n").
- **Förbearbetning av CSV-filer**: Standardisera textformat innan CSV-filer importeras till Excel.

## Varför bör du använda Convert Text API?

- **Automatisk formatkonvertering**: Konvertera textformaterade tal till beräkningsbara värden i bulk med ett enda anrop.
- **Teckenstandardisering**: Hantera specialtecken, diakritiska tecken och kodningsproblem enhetligt.
- **Datakonsistens**: Säkerställ att textformatet är helt enhetligt över hela datasetet.
- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och tillhandahåller omfattande dokumentation. Jämfört med att bygga anpassade textbearbetningslösningar minskar detta avsevärt utvecklingsarbetet.
- **Kostnadseffektivt**: Du kan konvertera text utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnader.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/ConvertText) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar de underliggande detaljerna och låter dig enkelt implementera Konvertera text för celler med minimal kod.  
Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertText.go" >}}
{{</tab>}}
{{< /tabs >}}
---