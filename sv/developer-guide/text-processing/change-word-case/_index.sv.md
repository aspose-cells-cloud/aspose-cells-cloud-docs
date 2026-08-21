---
title: "Aspose.Cells Cloud – Ändra ords skifteläge (versal, gemener, versal i varje ord, versal i början av mening)"
ArticleTitle: "Excel skiftelägekonverterare – Versaler, gemener, versal i varje ord & versal i början av mening"
linktitle: "Ords skifteläge"
type: docs
url: /sv/change-word-case/
keywords: "ändra ords skifteläge API, Aspose.Cells, Excel-skiftelägekonvertering, versaler, gemener, versal i varje ord, versal i början av mening, textformatering"
description: "Konvertera enkelt textskifteläge i Excel-filer med Aspose.Cells Cloud API. Stöder versaler, gemener, versal i varje ord och versal i början av mening. Få kodexempel i C#, Java, Python och mer."
weight: 100
---

## **Ändra ords skifteläge**

Använd Aspose.Cells Cloud Web API för att omedelbart konvertera textskifteläge i ditt kalkylblad – byt mellan versaler, gemener, versal i varje ord (versal i första bokstaven i varje ord) eller versal i början av mening (versal i första bokstaven i varje mening) över ett valt område. Endast textceller påverkas; nummer, booleska värden, fel och tomma celler ignoreras. Formler, formatering och datavalidering förblir oförändrade.

- **UpperCase** – alla tecken blir versaler.
- **LowerCase** – alla tecken blir gemener.
- **ProperCase** – första bokstaven i varje ord blir versal, resten gemener.
- **SentenceCase** – första bokstaven i varje mening blir versal, resten gemener.

<img src="images/result.png" alt="Skärmdump före/efter skiftelägekonvertering" width="800" height="450" />

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```
### Begäringsparametrar för **UpdateWordCase** API

| Parameternamn   | Typ    | Plats      | Beskrivning                                                                                                                                                             |
| :-------------- | :----- | :--------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet     | Fil    | FormData   | Kalkylbladsfilen som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV osv.                                                                                 |
| wordCaseType    | String | Query      | Anger typen av textskiftelägekonvertering: `UpperCase`, `LowerCase`, `ProperCase` eller `SentenceCase`.                                                                |
| worksheet       | String | Query      | _(Valfritt)_ Namnet på det kalkylblad där skiftelägekonvertering ska tillämpas. Om utelämnas tillämpas åtgärden på det första kalkylbladet i arbetsboken.               |
| range           | String | Query      | _(Valfritt)_ Cellområdet där skiftelägekonvertering ska tillämpas (t.ex. `"A1:C10"`). Om utelämnas tillämpas åtgärden på alla använda celler i det angivna kalkylbladet. |
| outPath         | String | Query      | _(Valfritt)_ Sökvägen till mappen i molnlagring där den bearbetade arbetsboken kommer att sparas. Om utelämnas sparas filen i källmappen.                            |
| outStorageName  | String | Query      | Namnet på molnlagringen där utdatafilen kommer att lagras.                                                                                                            |
| region          | String | Query      | _(Valfritt)_ Anger lokalspråk för textskiftelägesregler, särskilt relevant för språkspecifik versalering (t.ex. `"en-US"`, `"tr-TR"`).                                |
| password        | String | Query      | _(Valfritt)_ Om den uppladdade kalkylbladsfilen är lösenordsskyddad, ange lösenordet för att öppna och bearbeta filen.                                                |

### Svar

Vid lyckad förfrågan returnerar tjänsten **200 OK** (eller **202 Accepted**) med ett JSON-payload som innehåller den binära strömmen av den bearbetade arbetsboken.

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

- **400 Bad Request** – Ogiltig Aspose.Cells Cloud API-URI.
- **401 Unauthorized** – Ogiltig åtkomsttoken eller felaktiga klientuppgifter.
- **404 Not Found** – Kalkylbladsfilen är inte tillgänglig.
- **500 Server Error** – Ett internt bearbetningsfel uppstod i kalkylbladet.

## Var bör vi använda API:et för att ändra ords skifteläge?

### Datarenskning och standardisering

- **Kunddatahantering** – Standardisera versalering av kundnamn och adressinformation (t.ex. `john doe` → `John Doe`).
- **Produktkatalogbearbetning** – Standardisera produkttitlar och beskrivningstexter (t.ex. `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Finansiell rapportgenerering** – Normalisera objektnamn och beskrivningsfält i finansiella rapporter.

### Integration av data från flera källor

- **Data warehouse ETL** – Standardisera textformat vid inläsning av data från olika system.
- **API-datamottagning** – Hantera data med inkonsekvent versalering som returneras av externa API:er.
- **Datarörelse mellan avdelningar** – Standardisera textformat i Excel-rapporter från olika avdelningar.

### Innehållshanteringssystem

- **Automatiserade pressmeddelanden** – Formatera automatiskt nyhetstitlar och innehåll (versalregler för titlar).
- **Produktdokumentationsgenerering** – Säkerställa konsekvens i formateringen av tekniska dokumentationstermer.
- **Kunskapsbasunderhåll** – Standardisera textformat i vanliga frågor och hjälpdokument.

### Integration av företagsapplikationer

- **CRM-systemintegration** – Formatera automatiskt namn och företagsinformation vid import/export av kunddata.
- **ERP-datbearbetning** – Standardisera nyckelfält som materialbeskrivningar och leverantörsnamn.
- **HR-hanteringssystem** – Standardisera anställdinformation och tjänstebetiketter.

### Batchdokumentbearbetning

- **Juridiskt dokumentförberedelse** – Batchbearbeta klausulformat i kontrakt och avtal.
- **Marknadsföringsmaterialgenerering** – Standardisera textformat för annonstexter och e-postmallar.
- **Akademisk avhandlingformatering** – Standardisera formateringskrav för referenser och titlar.

### Realtidsdatbearbetning

- **Användarinmatningsvalidering** – Realtidsformatering av formulärdata inlämnad av användare.
- **Chattbot-svar** – Standardisera textformat för automatiskt genererade svar.
- **Direktgenerering av rapporter** – Dynamisk skapande av enhetligt formaterade affärsrapporter.

### Internationalisering och lokalisering

- **Multispråkig databearbetning** – Hantera skillnader i versalregler för texter i olika språk.
- **Lokalisering av innehållsförberedelser** – Förbereda formaterat lokalt innehåll för olika regioner.
- **Översättningsprojekthantering** – Säkerställa konsekvent textformat före och efter översättning.

## Varför bör du använda API:et för att ändra ords skifteläge?

- **Utvecklarvänlig** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och omfattande dokumentation. Jämfört med att bygga egna lösningar minskas detta betydligt utvecklingsarbetet.
- **Kostnadseffektiv** – Du kan ändra ords skifteläge utan att först behöva ladda upp arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, så att du enkelt kan implementera **UpdateWordCase** för celler med minimal kod. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---