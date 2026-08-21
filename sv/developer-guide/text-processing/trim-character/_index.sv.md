---
title: "Aspose.Cells Cloud Texttrimning Web API – Ta bort extra mellanslag och radbrytningar"
second_title: "Dokument"
ArticleTitle: "Excel-datarenslare – Trimma tecken, mellanslag och radbrytningar automatiskt – Online, kortkod"
linktitle: "Trimma tecken"
type: docs
url: /sv/trim-character/
keywords: "Excel, texttrimning, ta bort mellanslag, radbrytningar, Aspose.Cells, datarenslning, kalkylark, normalisera cellformat"
description: "Trimma extra mellanslag, radbrytningar och oönskade tecken från Excel-celler med Aspose.Cells Cloud API. Säkerställ ren och konsekvent kalkylarksdata."
weight: 100
---

Trimma automatiskt onödiga tecken, extra mellanslag och radbrytningar från Excel-celler med Aspose.Cells Trimma-tecken-API. Renslägg datauppgifter och upprätthåll konsekvent formatering i dina kalkylark.

## **Översikt**

- **Trimma första och sista mellanslagen**
  - Ta bort extra mellanslag i början och slutet av texten
  - Förbättra datautseendet, renlighet och läsbarhet
- **Hantering av extra mellanslag mellan ord**
  - Ta bort extra mellanslag mellan ord
  - Lös formatförvirring orsakad av data från flera källor

- **Speciella mellanslag som tas bort**
  - Tydligt ta bort icke-brytbara mellanslag
  - Säkerställa dataprecisering och konsekvens

- **Radbrytningshantering**
  - Ta bort extra eller alla radbrytningar
  - Håll cellinnehållet organiserat och professionellt utseende

## **TrimCharacter API**

Innan du anropar API:et, se till att du har ett giltigt Aspose Cloud-konto, en `client_id`/`client_secret` och en åtkomsttoken med **Cells**-omfattningen.

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/trim
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäranparametrar för **trimCharacter**-API:et är

| Parameternamn           | Typ     | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                                                          |
| :---------------------- | :------ | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet             | Fil     | FormData                   | Kalkylarksfilen som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV etc.                                                                                |
| trimContent             | Sträng  | Fråga                      | Anger de specifika tecken eller strängar som ska trimmas från cellinnehåll. Kan vara ett enskilt tecken, flera tecken eller ett anpassat mönster.                 |
| trimLeading             | Boolesk | Fråga                      | När `true` tas de angivna tecknen bort från början av varje cells innehåll.                                                                                        |
| trimTrailing            | Boolesk | Fråga                      | När `true` tas de angivna tecknen bort från slutet av varje cells innehåll.                                                                                        |
| trimSpaceBetweenWordTo1 | Boolesk | Fråga                      | När `true` reduceras flera på varandra följande mellanslag mellan ord till ett enda mellanslag i varje cell.                                                       |
| trimNonBreakingSpaces   | Boolesk | Fråga                      | När `true` tas icke-brytbara mellanslagstecken (Unicode U+00A0) bort från cellinnehåll.                                                                            |
| removeExtraLineBreaks   | Boolesk | Fråga                      | När `true` reduceras flera på varandra följande radbrytningar till en enda radbrytning i varje cell.                                                               |
| removeAllLineBreaks     | Boolesk | Fråga                      | När `true` tas alla radbrytningstecken bort från cellinnehåll.                                                                                                     |
| worksheet               | Sträng  | Fråga                      | _(Valfritt)_ Namnet på kalkylbladet där texttrimning ska tillämpas. Om utelämnas tillämpas åtgärden på det första kalkylbladet.                                     |
| range                   | Sträng  | Fråga                      | _(Valfritt)_ Cellintervallet där texttrimning ska tillämpas (t.ex. `"A1:C10"`). Om utelämnas tillämpas åtgärden på alla använda celler i det angivna kalkylbladet. |
| outPath                 | Sträng  | Fråga                      | _(Valfritt)_ Sökvägen till mappen i molnlagring där den bearbetade arbetsboken kommer att sparas. Om utelämnas sparas filen i källmappen.                           |
| outStorageName          | Sträng  | Fråga                      | Namnet på molnlagringen där utdatafilen kommer att lagras.                                                                                                          |
| region                  | Sträng  | Fråga                      | _(Valfritt)_ Anger lokalinställning för textbearbetning, vilket kan påverka hantering av mellanslag och radbrytningar för specifika språk (t.ex. `"sv-SE"`, `"ar-SA"`). |
| password                | Sträng  | Fråga                      | _(Valfritt)_ Om den uppladdade kalkylfilen är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                                  |

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

**Lyckat exempel (HTTP 200):** API:et returnerar en filström som innehåller den trimmade arbetsboken.

### Felkoder

- **400 Bad Request**: Ogiltig Aspose.Cells Cloud API-URI.
- **401 Unauthorized**: Ogiltig åtkomsttoken. Eller ogiltigt klient-id och hemligt nyckel.
- **404 Not Found**: Kalkylarksfilen är inte tillgänglig.
- **500 Server Error**: Kalkylbladet har stött på ett undantag vid hämtning av beräkningsdata.

## Var bör vi använda Trim Character API?

- **Normalisering av användarinmatning**: Renslägg manuellt inmatad tabelldata och ta bort överflödiga mellanslag och radbrytningar.
- **Underhåll av kunddatabas**: Renslägg överflödiga mellanslag och formateringsproblem i kundnamn, adresser och kontaktuppgifter.
- **Automatiserad rapportrenslning**: Renslägg datakällans format innan automatiska rapporter genereras.
- **Förberedelse inför datamigrering**: Renslägg formateringsproblem innan data migreras till det nya systemet.

## Varför bör du använda Trim Character API?

- **Lägre arbetskostnad**: Ta bort tidskrävande manuella insatser för datarenslning
- **Lägre felkostnad**: Undvik analysfel orsakade av formateringsproblem
- Betala per användning: Inga fastkostnader, endast fakturerad faktisk genomströmning
- **Ingen infrastrukturomkostnad**: Ingen behov av att underhålla servrar eller programvara
- **Stöd för flera format**: Stöder flera format som XLSX, XLS, CSV, ODS etc.
- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och finns med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskas utvecklingsarbetet avsevärt.
- **Kostnadseffektivt**: Du kan ta bort dubblelltecken utan att först ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/TrimCharacter) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar de underliggande detaljerna, så att du enkelt kan implementera Trim-tecken för celler med minimal kod.
Ta en titt på <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_TrimTextInSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_TrimTextInSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_TrimTextInSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_TrimTextInSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_TrimTextInSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_TrimTextInSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_TrimTextInSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_TrimTextInSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}

---