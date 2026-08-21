---
title: "Aspose.Cells Cloud – identifiera trasiga länkar i Excel-område (API)"
second_title: "Dokument"
ArticleTitle: "Hitta och fixa trasiga länkar i fjärr-Excel-område – moln-baserad länkkontroll för kalkylark"
linktype: "Sök trasiga länkar i fjärr-område"
type: docs
url: /search-broken-links-in-remote-range/
keywords: "Aspose, Cells, trasiga länkar, API, Excel-område, validering, moln, kalkylark, extern referens, kontroll"
description: "Använd Aspose.Cells Cloud API för att skanna ett specifikt Excel-område efter trasiga externa länkar, ogiltiga formler eller saknade datakällor. Säkert, snabbt och moln-baserat."
weight: 100
---

## **Sök trasiga länkar i fjärr-område API**

Upptäck automatiskt trasiga länkar i områdesdata för Excel-filer som lagras i molnlagring. Vårt API skannar angivna områden efter trasiga externa referenser, ogiltiga formler och saknade datakällor. Stödjer fjärrkontroll av kalkylark, automatiserad kvalitetskontroll och integration med molnlagringsleverantörer. RESTful API för affärsprocessautomation.

### **Webb-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäranparametrar

| Parametername | Typ    | Plats  | Beskrivning                                                                                                                                                          |
| ------------- | ------ | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | Sträng | Sökväg | **Obligatorisk.** Namnet på Excel-arbetsbokensfil (t.ex. `financial_report.xlsx`) som finns i molnlagringen och som du vill skanna efter trasiga länkar.              |
| worksheet     | Sträng | Sökväg | **Obligatorisk.** Namnet på det specifika kalkylbladet (t.ex. `Sheet1`, `Q4_Data`) i arbetsboken där sökning efter trasiga länkar ska utföras.                        |
| cellArea      | Sträng | Sökväg | **Obligatorisk.** Adressen till det målområde (t.ex. `A1:F100`) i det angivna kalkylbladet som ska skannas efter trasiga externa referenser, formler eller länkar.    |
| folder        | Sträng | Fråga  | **Valfri.** Sökvägen till katalogen i din molnlagring där målarbetsboken finns. Om utelämnad antas rotkatalogen gälla.                                               |
| storageName   | Sträng | Fråga  | **Valfri.** Namnet på din konfigurerade molnlagringstjänst (t.ex. `DropboxBusiness`, `S3Bucket`). Om inte angiven använder API:et kontots standardlagring.       |
| region        | Sträng | Fråga  | **Valfri.** Det lokala inställningsvärdet (t.ex. `sv-SE`, `de-DE`) som ska tillämpas vid regional tolkning av data under skanningen.                                |
| password      | Sträng | Fråga  | **Valfri.** Lösenordet som krävs för att dekryptera en lösenordsskyddad arbetsbok. Lämna tomt om filen inte är krypterad.                                            |

**Exempel på begäran_innehåll**

```json
{
  "name": "financial_report.xlsx",
  "worksheet": "Sheet1",
  "cellArea": "A1:F100",
  "folder": "reports/2024",
  "storageName": "MyDropbox",
  "region": "en-US",
  "password": ""
}
```

### Svar

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

Samlingen `BrokenLinks` innehåller objekt av typen **BrokenLink**. Varje objekt tillhandahåller följande egenskaper:

- **CellName** – Adressen till cellen som innehåller den trasiga referensen (t.ex. `B12`).
- **LinkType** – Typen av länk som är trasig (t.ex. `ExternalReference`, `Formula`).
- **ErrorMessage** – En beskrivning av varför länken anses vara trasig.

**Obs!** API:et är föremål för hastighetsbegränsningar. Se [Prissättning och hastighetsbegränsningar](https://www.aspose.cloud/pricing) för detaljer.

### Felkoder

- **400 Bad Request** – Ogiltig Aspose.Cells Cloud API-URI.
- **401 Unauthorized** – Ogiltig åtkomsttoken, klient-ID eller klienthemlighet.
- **404 Not Found** – Kalkylarkfilen är inte tillgänglig.
- **500 Server Error** – Kalkylarket stötte på ett fel vid hämtning av beräkningsdata.

## Var bör vi använda sökning efter trasiga länkar i kalkylarksområdet API?

- **Regelbunden granskning av stora finansmodeller** – Innan månads- eller kvartalsrapporter publiceras, skanna automatiskt nyckelberäkningsområden (t.ex. `Dashboard!B5:K50`) som innehåller många externa datareferenser för att säkerställa att alla länkar pekar på giltiga källfiler.
- **Dataintegration vid fusioner och övertaganden** – Vid sammanslagning av flera kalkylarkfil som representerar affärsenheter, skanna "Översikt"-kalkylbladet efter integrationen för att identifiera länkar som blivit ogiltiga på grund av ändrade filsökvägar eller behörighetsproblem.
- **Förberedelse av investorrapporter** – Innan presentationsmaterial som innehåller diagram och tabeller kopplade till externa databaser eller marknadsdatakällor slutförs, verifiera giltigheten av alla länkar.

## Varför bör du använda sökning efter trasiga länkar i kalkylarksområdet API?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling med omfattande dokumentation. Jämfört med att bygga en egen lösning minskas utvecklingsinsatsen betydligt.
- **Lägre arbetskostnader** – Eliminerar behovet av dedikerad personal för manuell dokumentkonsolidering.
- **Betala per användning** – Inga förstakostnader; du betalar endast för de API-anrop du faktiskt gör.
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.
- **Bevarar avancerat Excel-formatering** – Resultaten kan exporteras till PDF-format utan att förlora formatering.

## Hur använder man sökning efter trasiga länkar i kalkylarksområdet API med SDK:er

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Användning av SDK är det bästa sättet att påskynda utvecklingen. SDK:et hanterar underliggande detaljer och låter dig implementera "sök trasiga länkar i ett område" med minimal kod. Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}