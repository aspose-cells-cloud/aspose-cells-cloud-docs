---
title: "Aspose.Cells Cloud – Ersätt text i lokala Excel-filer (Sök- och ersätt-API)"
secondtitle: "Dokument"
ArticleTitle: "Massersättning av text i lokala Excel-filer – Sök- och ersätt-API"
linktitle: "Ersätt kalkylbladsinnehåll"
type: docs
url: /replace-spreadsheet-content/
keywords: "ersätt text i Excel, Aspose.Cells sök och ersätt, API för lokala kalkylark, ersätt Excel-fil, API för att ersätta innehåll"
description: "Ersätt text i lokala Excel-arbetsböcker utan att ladda upp till molnet. Använd Aspose.Cells Clouds sök- och ersätt-API för att uppdatera specifika intervall, kalkylblad eller hela filer i ett enda anrop."
weight: 100
---

Ersätt specificerad text i lokala Excel-kalkylark utan att ladda upp till molnet. Uppdatera innehåll i arbetsböcker effektivt med Aspose.Cells Clouds sök- och ersätt-API för offlineredigering.

## **Ersätt kalkylbladsinnehåll – API**

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/replace/content
```

### **Säkerhet och autentisering**

Aspose.Cells Clouds API är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Förfrågningsparametrar:**

| Parametername | Typ   | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                                                                               |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Fil   | FormData                   | Den lokala kalkylarkfil som ska bearbetas. Stödda format inkluderar XLSX, XLS, ODS, CSV m.fl.                                                                                                             |
| searchText     | Sträng | Frågesträng                 | Den textsträng som ska sökas efter i det angivna kalkylbladet och cellområdet.                                                                                                                          |
| replaceText    | Sträng | Frågesträng                 | Den textsträng som kommer att ersätta alla förekomster av `searchText` inom det angivna intervallet.                                                                                                     |
| worksheet      | Sträng | Frågesträng                 | _(Valfritt)_ Namnet på det kalkylblad där sök- och ersättoperationen ska utföras. Om utelämnas tillämpas operationen på det första kalkylbladet.                                                         |
| cellArea       | Sträng | Frågesträng                 | _(Valfritt)_ Det specifika cellintervallet (t.ex. `"A1:D20"`, `"B5:F15"`) där textsökning och ersättning ska ske. Om utelämnas tillämpas operationen på alla använda celler i det angivna kalkylbladet.    |
| region         | Sträng | Frågesträng                 | _(Valfritt)_ Anger lokalisering för texthantering, vilket kan påverka skiftlägeskänslighet och teckenkodning i sökoperationer (t.ex. `"sv-SE"`, `"en-US"`, `"fr-FR"`).                                       |
| password       | Sträng | Frågesträng                 | _(Valfritt)_ Om den uppladdade kalkylarkfilen är lösenordsskyddad anger du lösenordet för att öppna och bearbeta filen.                                                                                 |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Svaret är en binär ström som innehåller den uppdaterade arbetsboken. Spara den med lämplig filtillägg (t.ex. `.xlsx`).

### **Felkoder**

- **400 Bad Request** – Ogiltig Aspose.Cells Cloud API-URI eller felaktigt formade parametrar.
- **401 Unauthorized** – Ogiltigt eller saknat åtkomsttoken; skaffa ett nytt token.
- **404 Not Found** – Kalkylarkfilen är inte tillgänglig eller det angivna kalkylbladet finns inte.
- **500 Server Error** – Ett internt bearbetningsfel uppstod i kalkylarkfilen; kontakta support om problemet kvarstår.

## Var bör vi använda API:et för att ersätta innehåll i kalkylark?

- **Batchbearbetning av lokala Excel-filer** – Automatisera sök- och ersättning över många arbetsböcker som lagras lokalt.
- **Lokala dataflöden** – Integrera API:et i schemalagda jobb som modifierar rapporter innan de arkiveras eller distribueras.
- **Lokal rapportgenerering** – Dynamiskt infoga värden i mallarbetsböcker utan att ladda upp dem till molnet.

## Varför bör du använda API:et för att ersätta innehåll i kalkylark?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och omfattande dokumentation. Jämfört med att bygga egna lösningar minskas utvecklingsarbetet avsevärt.
- **Lägre arbetskostnader** – Minskar behovet av dedikerad personal för manuell dokumentkonsolidering.
- **Betala per användning** – Inga förvalskostnader; du betalar endast för de API-anrop du faktiskt använder.
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.
- **Bevarar komplex Excel-formatering** – Den ursprungliga arbetsbokens formatering, formler och diagram bevaras efter ersättning.

## Hur man använder API:et för att ersätta innehåll i kalkylark med SDK:n

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceSpreadsheetContent) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:n

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. SDK:n hanterar de underliggande detaljerna och gör det möjligt att implementera ersättningsoperationer med minimal kod. Se den officiella **Aspose.Cells Cloud SDK GitHub**-lagret för en komplett lista över stödda språk.

Följande kodexempel visar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:n:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ReplaceTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ReplaceTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ReplaceTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ReplaceTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ReplaceTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ReplaceTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ReplaceTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ReplaceTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}