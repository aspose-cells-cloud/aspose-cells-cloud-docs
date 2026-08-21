---
title: "Aspose.Cells Cloud – API för att upptäcka trasiga länkar i Excel – Skanna och validera kalkylbladslänkar i fjärrarbetsböcker"
second_title: "Dokument"
ArticleTitle: "Hitta och åtgärda trasiga länkar i fjärr-Excel – Molnbaserad länkverifierare för kalkylblad"
linktitle: "Sök efter trasiga länkar i fjärrkalkylblad"
type: docs
url: /sv/search-broken-links-in-remote-spreadsheet/
keywords: "Excel, trasiga länkar, API, moln, kalkylblad, validering, Aspose.Cells"
description: "Använd Aspose.Cells Cloud API för att skanna fjärr-Excel-arbetsböcker efter trasika externa länkar, ogiltiga formler och saknade datakällor."
weight: 100
---

## **Sök efter trasiga länkar i fjärrkalkylblad via API**

Identifiera automatiskt trasiga länkar i Excel-filer som lagras i molnlagring. Vårt API skannar angivna intervall efter trasiga externa hänvisningar, ogiltiga formler och saknade datakällor. Det stöder granskning av fjärrkalkylblad, automatiserad kvalitetskontroll och integration med molnlagringsleverantörer. Använd det REST-baserade API:et för att automatisera enterprise-nivåens arbetsflöden.

### **Webb-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/search/broken-links
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Förfrågningsparametrar:**

| Parametername  | Typ    | Sökväg/Frågesträng/HTTPBody | Beskrivning                                                                                                                                               |
| :------------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Sökväg                     | **Obligatoriskt.** Namnet på Excel-arbetsboksfilen som ska skannas efter trasiga länkar (t.ex. `Quarterly_Report.xlsx`).                                  |
| worksheet      | String | Frågesträng                | **Obligatoriskt.** Namnet på kalkylbladet där sökoperationen ska utföras. Ange det exakta arknamnet så som det visas i arbetsboken.                        |
| cellArea       | String | Frågesträng                | **Obligatoriskt.** Det cellintervall som ska analyseras efter trasiga länkar, angivet i A1-notation (t.ex. `C5:J50`). API:et söker endast inom detta område. |
| folder         | String | Frågesträng                | **Valfritt.** Sökvägen till mappen som innehåller arbetsboken i din molnlagring. Om utelämnad antas rotmappen användas.                                   |
| storageName    | String | Frågesträng                | **Valfritt.** Namnet på din anpassade molnlagringskonfiguration. Om utelämnad används systemets standardlagring.                                          |
| region         | String | Frågesträng                | **Valfritt.** Lokal inställning som tillämpas under bearbetning (t.ex. `sv-SE`). Detta kan påverka tolkningen av region-specifik formelsyntax eller hänvisningar. |
| password       | String | Frågesträng                | **Valfritt.** Lösenord krävs för att öppna en krypterad kalkylfil. Utelämna om filen inte är lösenordsskyddad.                                             |

**Exempel på cURL-förfrågan**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Quarterly_Report.xlsx/search/broken-links?worksheet=Sheet1&cellArea=C5:J50" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Svar**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

**Exempel på JSON-svar**

```json
{
  "BrokenLinks": [
    {
      "Worksheet": "Sheet1",
      "CellName": "D12",
      "Link": "https://example.com/data/source.xlsx",
      "IsValid": false,
      "ErrorMessage": "Filen hittades inte"
    },
    {
      "Worksheet": "Sheet1",
      "CellName": "F30",
      "Link": "C:\\LocalFolder\\data.xlsx",
      "IsValid": false,
      "ErrorMessage": "Externa hänvisningar stöds inte i moln-läge"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Felkoder

- **400 Bad Request** – Ogiltig URI för Aspose.Cells Cloud API.  
- **401 Unauthorized** – Ogiltig åtkomsttoken, klient-ID eller klienthemlighet.  
- **404 Not Found** – Kalkylbladsfilen är inte tillgänglig.  
- **500 Server Error** – Ett fel uppstod vid hämtning av beräkningsdata.

## Var bör vi använda sökfunktionen för trasiga länkar i kalkylblads-API:et?

- **Regelbunden granskning av stora finansiella modeller** – Innan månads- eller kvartalsrapporter publiceras, skanna automatiskt nyckelberäkningsområden (t.ex. `Dashboard!B5:K50`) som innehåller många externa datahänvisningar för att säkerställa att alla länkar pekar på giltiga källfiler.  
- **Dataintegration vid fusioner och övertaganden** – När flera kalkylblad som representerar verksamhetsenheter sammanfogas, skanna “Overview”-arket efter integrationen för att identifiera länkar som blivit ogiltiga på grund av ändrade filsökvägar eller behörighetsproblem.  
- **Förberedelse av investerardatapaket** – Innan presentationsmaterial med diagram och tabeller länkade till externa databaser eller marknadsdatakällor färdigställs, verifiera giltigheten för alla länkar.

## Varför bör du använda sökfunktionen för trasiga länkar i kalkylblads-API:et?

- **Utvecklarvänligt** – Aspose.Cells Cloud tillhandahåller SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling med omfattande dokumentation. Jämfört med att bygga en egen lösning minskas utvecklingsinsatsen markant.  
- **Lägre arbetskostnad** – Automatiserar länkvalidering, vilket eliminerar behovet av personer som manuellt sammanställer dokument.  
- **Betala per användning** – Inga förhandsutgiftskostnader; du betalar endast för de API-anrop du faktiskt använder.  
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen programvaruuppdatering och inga kompatibilitetsproblem.

## Hur man använder sökfunktionen för trasiga länkar i kalkylblads-API:et med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och tillåter dig att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det mest effektiva sättet att påskynda utvecklingen. SDK:et abstraher bort de underliggande HTTP-detaljerna och gör att du kan implementera upptäckt av trasiga länkar med minimal kod. Se [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du interagerar med Aspose.Cells webbtjänster med diverse SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}