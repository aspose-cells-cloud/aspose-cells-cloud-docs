---
title: "Sök efter trasiga länkar i kalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Hitta och åtgärda trasiga länkar i Excel – Moln-baserat länkverktyg för kalkylark"
linktype: "Search Spreadsheet Broken Links"
type: docs
url: /search-spreadsheet-broken-links/
keywords: "Aspose Cells, trasiga länkar, granskning av kalkylark, Excel API, molnkalkylark, länkverifierare"
description: "Upptäck och åtgärda trasiga länkar i Excel-arbetsböcker via Aspose.Cells Cloud API. Skanna intervall, få detaljerade JSON-resultat och integrera med SDK för valfritt programmeringsspråk."
weight: 100
---

## **Sök efter trasiga länkar i kalkylark – API**

Identifiera automatiskt trasiga länkar i Excel-filer. Vårt API skannar angivna intervall efter trasiga externa referenser, ogiltiga formler och saknade datakällor. Stödjer fjärrgranskning av kalkylark, automatiska kvalitetskontroller och integration med molnlagringsleverantörer. RESTful API för företagsworkflowautomation.

**Sammanfattning:** Använd denna endpoint för snabbt att identifiera och reparera ogiltiga länkar i arbetsböcker, vilket säkerställer datointegritet i finansiella modeller, M&A-dataset och investerarredovisningsmaterial.

### **Webb-API**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Blad1" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@exempel.xlsx"
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begärandeparametrar**

| Parameter_name | Typ    | Plats                | Beskrivning                                                                                                            |
| -------------- | ------ | -------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | FormData (multipart) | **Obligatoriskt.** Excel-arbetsboken (`.xlsx`, `.xls` etc.) som ska analyseras.                                        |
| worksheet      | Sträng | Frågeparameter       | **Valfritt.** Namnet på det kalkylblad som ska analyseras. Om utelämnas används det första kalkylbladet.               |
| cellArea       | Sträng | Frågeparameter       | **Valfritt.** Målcellintervall i A1-notation (t.ex. `B2:D10`). Om utelämnas analyseras hela det använda intervallet.   |
| region         | Sträng | Frågeparameter       | **Valfritt.** Lokalinställning (t.ex. `sv-SE`) som kan påverka tolkning av datum, tal eller valuta.                     |
| password       | Sträng | Frågeparameter       | **Valfritt.** Lösenord för krypterade arbetsböcker. Lämna tomt om filen inte är skyddad.                                |

### **Svar**

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "Filen hittades inte",
      "Status": "Trasig"
    },
    {
      "CellName": "C12",
      "Link": "http://example.com/data.csv",
      "ErrorMessage": "404 Not Found",
      "Status": "Trasig"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### **Felkoder**

| Kod  | Beskrivning |
|------|-------------|
| **400 Bad Request** | Ogiltig URI för Aspose.Cells Cloud API. |
| **401 Unauthorized** | Ogiltig åtkomsttoken, klient-ID eller klienthemlighet. |
| **404 Not Found** | Kalkylarkfilen är inte tillgänglig. |
| **429 Too Many Requests** | Gräns för förfrågningsfrekvens överskriden (60 anrop/minute). |
| **500 Server Error** | Kalkylarket stötte på ett fel vid hämtning av beräkningsdata. |


## Var bör vi använda Sök trasiga länkar i Kalkylark API?

- **Regelbunden granskning av stora finansiella modeller**: Innan månads- eller kvartalsrapporter publiceras, skanna automatiskt nyckelberäkningsområden (t.ex. `Dashboard!B5:K50`) som innehåller många externa datareferenser för att säkerställa att alla länkar pekar på giltiga källfiler.  
- **Dataintegration för fusioner och överlåtelser**: Vid sammanslagning av flera kalkylark som representerar affärsenheter, skanna "Översikt"-kalkylbladet efter integration för att upptäcka länkar som blivit ogiltiga på grund av ändrade filsökvägar eller behörighetsproblem.  
- **Förberedelse av investerardatapaket**: Innan slutgiltiga presentationsmaterial med diagram och tabeller som länkar till externa databaser eller marknadsdatakällor publiceras, verifiera giltigheten för alla länkar.

## Varför bör du använda Sök trasiga länkar i Kalkylark API?

- **Utvecklarvänligt** – Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och omfattande dokumentation. Jämfört med byggande av anpassade lösningar minskas utvecklingsarbete betydligt.  
- **Lägre arbetskostnader** – Upphäver behovet av personaltid för manuell kontroll av dokumentlänkar.  
- **Betala per användning** – Inget förstainvestering; du betalar endast för de API-anrop du faktiskt använder.  
- **Inga underhållskostnader** – Inga servrar att underhålla, ingen mjukvaruuppdatering och inga kompatibilitetsproblem.  
- **Bevarar avancerat Excel-formatering** – Resultaten returneras i ett universellt tillgängligt JSON-format medan originalarbetsbokens layout bibehålls.

## Hur använder man Sök trasiga länkar i Kalkylark API med SDK:er

### **OpenAPI-specifikation**

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### **Använd Aspose.Cells Cloud SDK:er**

Att använda SDK är det bästa sättet att accelerera utvecklingen. SDK hanterar underliggande detaljer, vilket gör att du enkelt kan implementera söktrasiga-länkar-funktionen med minimal kod. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}