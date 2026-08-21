---
title: "Aspose.Cells Cloud – Excel API för upptäckt av trasiga länkar – Skanna & validera kalkylarkslänkar i fjärrarbetsblad"
second_title: "Dokument"
ArticleTitle: "Hitta & fixa trasiga länkar i fjärr-Excel-arbetsblad – Molnbaserat länkverifieringsverktyg"
linktitle: "Sök efter trasiga länkar i fjärrarbetsblad"
type: docs
url: /sv/search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, trasiga länkar, Excel-API, molnbaserat kalkylark, länkvalidering"
description: "Upptäck och fixa trasiga externa länkar i Excel-arbetsblad som lagras i molnlagring. Använd Aspose.Cells Cloud API för att skanna intervall, returnera länkuppgifter och automatisera kvalitetskontroller."
weight: 100
---

## **Sök efter trasiga länkar i fjärrarbetsblad – API**

Upptäck automatiskt trasiga länkar i ett Excel-arbetsblad som lagras i molnlagring. Vårt API skannar angivna intervall för att hitta trasiga externa referenser, ogiltiga formler och saknade datakällor. Stödjer fjärrgranskning av kalkylark, automatiserade kvalitetskontroller och integration med molnlagringsleverantörer. RESTful API för företagsworkflowautomatisering.

### **Webb-API**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:en är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Förfrågningsparametrar:**

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning                                                                                                                                                                                                                                |
| :------------ | :---- | :---------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name          | Sträng | Sökväg                        | **Obligatoriskt.** Filnamnet (med tillägg) för den Excel-arbetsbok där trasiga länkar ska sökas (t.ex. `Årsrapport.xlsx`).                                                                                                                 |
| worksheet     | Sträng | Sökväg                        | **Obligatoriskt.** Det exakta namnet på det arbetsblad där länkskanningen ska utföras (t.ex. `DataBlad1`).                                                                                                                              |
| folder        | Sträng | Frågesträng                   | **Valfritt.** Sökvägen till katalogen i din molnlagring där den aktuella arbetsboken finns. Om utelämnas används rotmappen.                                                                                                      |
| storageName   | Sträng | Frågesträng                   | **Valfritt.** Identifieraren för din anpassade konfigurerade molnlagring. Om inte angiven används kontots standardlagring.                                                                                                         |
| region        | Sträng | Frågesträng                   | **Valfritt.** Den språkinställning som ska tillämpas vid sökningen (t.ex. `sv-SE`). Detta kan påverka tolkningen av vissa formler eller regionella dataformat. _Stödda språkkoder inkluderar `en-US`, `fr-FR`, `de-DE`, `es-ES`, `sv-SE` etc._ |
| password      | Sträng | Frågesträng                   | **Valfritt.** Lösenordet för dekryptering av ett lösenordsskyddat kalkylark. Utelämna om filen inte är krypterad.                                                                                                                             |

**Exempel på cURL-förfrågan**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Årsrapport.xlsx/worksheets/DataBlad1/search/broken-links?folder=Rapporter&storageName=MinLagring" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Källa.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Källfil hittades inte"
    }
  ]
}
```

Svarsobjektet är av typen **BrokenLinksResponse** och innehåller:

- **BrokenLinks** – en samling `BrokenLink`-objekt, var och en beskriver den problematiska referensen (adress, felkod och meddelande).
- **Code** – numerisk statuskod som returneras av tjänsten.
- **Status** – textuell beskrivning av resultatet.

**Anteckningar**: API:et paginerar inte resultat. Upp till 10 000 trasiga länkar kan returneras per förfrågan. Rate limit är 100 förfrågningar per minut per konto.

### Felkoder

- **400 Bad Request** – Ogiltig URI för Aspose.Cells Cloud API.
- **401 Unauthorized** – Ogiltig eller saknad åtkomsttoken.
- **404 Not Found** – Kalkylarkfilen är inte tillgänglig.
- **500 Server Error** – Ett fel uppstod vid hämtning av beräkningsdata.

## Var bör vi använda sökfunktionen efter trasiga länkar i ett kalkylarks arbetsblad?

- **Regelbunden granskning av stora finansiella modeller**: Innan månads- eller kvartalsrapporter publiceras, skanna automatiskt viktiga beräkningsområden (t.ex. `Dashboard!B5:K50`) som innehåller stora mängder externa datareferenser, för att säkerställa att alla länkar pekar på giltiga källfiler.
- **Dataintegration vid fusioner och akkvisationer**: När flera kalkylark som representerar affärsenheter sammanfogas, skanna "Översikt"-arbetsbladet efter integrationsprocessen för att identifiera länkar som blivit ogiltiga på grund av ändrade sökvägar till källfiler eller behörighetsproblem.
- **Förberedelse av investerardatapaket**: Innan presentationsmaterial med diagram och tabeller kopplade till externa databaser eller marknadsdatakällor färdigställs, verifiera giltigheten av alla länkar.

## Varför bör du använda sökfunktionen efter trasiga länkar i ett kalkylarks arbetsblad?

- **Utvecklarvänlig**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och kommer med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskas utvecklingsarbetet avsevärt.
- **Sänker arbetskostnader**: Minskar behovet av personal som tilldelas manuell dokumentkonsolidering och länkverifiering.
- **Betala per användning**: Inget förstainvestering krävs; du betalar endast för de API-anrop som du faktiskt använder.
- **Inga underhållskostnader**: Inga servrar att underhålla, ingen programvaruuppdatering och inga kompatibilitetsproblem att hantera.
- **Bevarar kompleks Excel-formatering** i universellt tillgängligt PDF-format.

## Hur används sökfunktionen efter trasiga länkar i ett kalkylarks arbetsblad med SDK:er?

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det bästa sättet att påskynda utvecklingen. SDK hanterar underliggande detaljer, så att du enkelt kan implementera sökning efter trasiga länkar i kalkylarkarbetsblad med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur anrop görs till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}