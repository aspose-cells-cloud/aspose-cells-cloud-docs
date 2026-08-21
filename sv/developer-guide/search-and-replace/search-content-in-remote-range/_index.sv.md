---
title: "Aspose Cells Cloud Excel-textsöknings-API – Sök text i fjärranslutna kalkylbladsintervall"
second_title: "Dokument"
ArticleTitle: "Sök text i fjärranslutna Excel-kalkylark – Hitta data i specifika intervall"
linktitle: "Sök i fjärrintegritetsinnehåll"
type: docs
url: /sv/search-content-in-remote-range/
keywords: "Aspose.Cells, Excel-API, sök text, fjärrintervall, molnkalkylark, REST-API, datadisposition"
description: "Sök efter text, siffror eller formler i ett specifikt intervall av en Excel-arbetsbok som lagras i Aspose Cloud."
weight: 100
---

## **Sök i innehåll i fjärrintervall**

Sök systematiskt efter specifik text i valfritt intervall av Excel-kalkylblad med Aspose.Cells Cloud API. Hitta text, siffror eller formler i filer som finns lagrade i molnlagring. RESTful API för automatiserad datadisposition, innehållsanalys och arbetsflöden för kalkylarksgranskning.


### **Webb-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/content
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


**cURL-exempel**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Orders_2024/ranges/B2:H100/search/content?searchText=Report&ignoreCase=true" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json"
```

### Begäranparametrar

| Parameternamn  | Typ     | Sökväg/Fråga/Streng/HTTPBody | Beskrivning                                                                                                                                         |
| :------------- | :------ | :------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String  | Sökväg                     | **Obligatoriskt**. Filnamnet (inklusive tillägg) för den Excel-arbetsbok som ska genomsökas, t.ex. `customer_data.xlsx`.                          |
| worksheet      | String  | Sökväg                     | **Obligatoriskt**. Det exakta namnet på kalkylbladet inom arbetsboken där sökning ska ske, t.ex. `Orders_2024`.                                   |
| cellArea       | String  | Sökväg                     | **Obligatoriskt**. Målintervallet för sökningen, specificerat i A1-notation (t.ex. `B2:H100`). Sökningen begränsas till detta område.               |
| searchText     | String  | Fråga                      | **Obligatoriskt**. Den specifika textsträngen, siffran eller del av innehåll som ska hittas i det definierade cellområdet.                          |
| ignoreCase     | Boolean | Fråga                      | **Valfritt**. När inställt på `true` ignorerar sökningen skiftlägesskillnader (t.ex. matchar "Report" även "report"). Standardvärde är `false` (skiftlägeskänsligt). |
| folder         | String  | Fråga                      | **Valfritt**. Sökvägen till katalogen i molnlagringen där arbetsboken finns. Om utelämnad används rotkatalogen.                                   |
| storageName    | String  | Fråga                      | **Valfritt**. Identifikator för en anpassad molnlagringskonfiguration. Om ej angiven används standardlagringen för kontot.                       |
| region         | String  | Fråga                      | **Valfritt**. Kultur-/regioninställning (t.ex. `sv-SE`) som kan påverka tolkningen av regionspecifika tecken eller format under sökningen.         |
| password       | String  | Fråga                      | **Valfritt**. Lösenordet för att dekryptera och komma åt en lösenordsskyddad kalkylarkfil. Utelämna om filen inte är krypterad.                   |

### Svar

```json
{
  "Code": 200,
  "Status": "OK",
  "TextItems": [
    {
      "Filename": "string",
      "Worksheet": "string",
      "Position": "string",
      "Content": "string"
    }
  ]
}
```

### Felkoder

- **400 Bad Request** – Ogiltig URI för Aspose.Cells Cloud API.  
- **401 Unauthorized** – Ogiltig åtkomsttoken, klient-ID eller klienthemlighet.  
- **404 Not Found** – Kalkylarkfilen är inte tillgänglig.  
- **500 Server Error** – Ett oväntat tillstånd förhindrade servern från att uppfylla begäran.

## Var bör vi använda sökning i innehåll i ett intervall av kalkylarks-API:t?

- **Storskalig datakvalitetskontroll** – Under acceptansfasen i ETL-processen för datalagring söks efter saknade fältbeskrivningar, odefinierade förkortningar eller platshållartext (t.ex. `"TBD"` eller `"NULL"`) i datamappningstabellen (`DataDictionary!B2:F1000`) för att identifiera ofärdiga datadefinitioner.  
- **Dynamisk rapportgenerering och innehållsextraktion** – I automatiserade rapporteringssystem söks och extraheras aktuella periodsdatablock markerade med specifika identifierare (t.ex. `"[KPI]"`) från mallkalkylblad med blandat innehåll (`Monthly_Metrics!C10:G50`) för att sammanställa slutgiltiga rapporter.  
- **Kontrakt- och juridisk dokumentanalys** – Vid granskning av kalkylarksbilagor med många klausuler lokaliseras effektivt specifika juridiska termer (t.ex. `"ansvarsbegränsning"`), parters namn eller datum inom ett definierat intervall (`Contract_Terms!A:A`) för att påskynda granskningsprocessen.

## Varför bör du använda sökning i innehåll i ett intervall av kalkylarks-API:t?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och omfattande dokumentation, vilket avsevärt minskar utvecklingsarbetet jämfört med att bygga egna lösningar.  
- **Lägre arbetskostnader** – Eliminerar behovet av dedikerade roller för hantering av dokumentkonsolidering.  
- **Betala per användning** – Inga förhandsinvesteringar; du betalar endast för de API-anrop som faktiskt används.  
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen programvaruuppdatering och inga kompatibilitetsproblem.

## Hur använder man sökning i innehåll i ett intervall av kalkylarks-API:t med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchContentInRemoteRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och möjliggör REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar de underliggande detaljerna, så att du enkelt kan implementera sökning i innehåll i ett intervall av kalkylblad med minimal kod. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}