---
title: "Aspose.Cells Cloud Web API – Ta bort tomma/blanka rader automatiskt"
second_title: "Dokument"
ArticleTitle: "Så här tar du bort alla tomma/blanka rader i Excel – En komplett vägledning för datarensning"
linktype: "Ta bort tomma rader"
type: docs
url: /sv/delete-spreadsheet-blank-rows/
keywords: "Aspose.Cells, Excel, tomma rader, ta bort rader, rensa kalkylark, API"
description: "Ta bort alla tomma rader från Excel-filer via Aspose.Cells Cloud API. Snabbt, redo för batchbehandling och helt programmerbart – se kodexempel i C#, Java, Python och mer."
weight: 100
---

Ta automatiskt bort alla tomma rader från Excel-kalkylark med Aspose.Cells Cloud API. Vårt intelligenta API upptäcker och tar bort rader som inte innehåller någon data, formler, kommentarer eller objekt, samtidigt som all annat innehåll bevaras. Det stöder batchbehandling, molnautomation och sömlös integration för företagsdatarensingsarbetsflöden.

## DeleteSpreadsheetBlankRows API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


### Begäranparametrar

| Parameternamn    | Typ    | Plats     | Beskrivning                                                                                                                                         |
| ---------------- | ------ | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Fil    | FormData  | Excel-filen (`.xlsx`, `.xls`, `.ods` etc.) som ska bearbetas.                                                                                      |
| outPath          | Sträng | Query     | (Valfritt) Målmapp i din molnlagring för den rensade arbetsboken. Om den utelämnas sparas filen bredvid källfilen.                                   |
| outStorageName   | Sträng | Query     | Namn på den konfigurerade molnlagringen (t.ex. `MyDropbox`, `CorporateOneDrive`). Krävs om du vill att utdata ska lagras i en specifik lagring.     |
| region           | Sträng | Query     | Lokala inställningar (t.ex. `sv-SE`, `fr-FR`) som tillämpas under bearbetning.                                                                     |
| password         | Sträng | Query     | Lösenord för att öppna ett krypterat kalkylark. Utelämna om filen inte är skyddad.                                                                  |

**Autentisering**  
Alla anrop måste inkludera `Authorization: Bearer <access_token>`-headern. Skaffa åtkomsttoken via Aspose Cloud OAuth2-flödet som beskrivs i autentiseringshandboken.

**Förutsättningar och anteckningar**  
- Se till att din Aspose Cloud-lagring är konfigurerad och att arbetsboken har laddats upp innan du anropar API:et.  
- Filformat som stöds inkluderar `.xlsx`, `.xls`, `.ods` och andra vanliga kalkylarksformat.  
- Maximal filstorlek är 150 MB för en enskild begäran; större filer bör bearbetas i bitar.  

### Respons

API:et returnerar en JSON-ARRAY som innehåller en referens till den bearbetade filen.

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

- **400 Bad Request** – Ogiltig URI för Aspose.Cells Cloud API.
- **401 Unauthorized** – Ogiltig åtkomsttoken eller klientuppgifter.
- **404 Not Found** – Kalkylarkfilen kan inte nås.
- **500 Server Error** – Ett oväntat fel uppstod under bearbetning av filen.

## Var bör man använda Delete Spreadsheet Blank Rows API?

- **Dataimport- och datarensingsarbetsflöden** – Rensa efterföljande eller strukturella tomma rader direkt efter import av data från CSV, databaser eller webb-API:er.
- **Generering av rapporter och instrumentpaneler** – Säkerställ en professionell layout genom att ta bort onödiga tomma rader innan finans-, försäljnings- eller driftrapporter fastställs.
- **Förberedelse av data för analys (ETL)** – Förbearbeta Excel-data i ETL-pipelines innan de laddas till datalagringar (Snowflake, BigQuery) eller BI-verktyg (Tableau, Power BI).
- **Systemintegration och API-strömmar** – Normalisera Excel-filer som tas emot från partnersystem, CRM- och ERP-system genom att ta bort oanvända rader.
- **Dokumentautomation och batchbehandling** – Ta bort platshållarrader som genereras av mallmotorer innan distribution.
- **Bearbetning av användargenererat innehåll** – Standardisera Excel-uppladdningar från webbportaler eller applikationer innan vidare bearbetning eller lagring.
- **Migrering av äldre data** – Effektivisera gamla kalkylarksarkiv genom att ta bort historiskt tomma eller platshållar-rader.

## Varför bör du använda Delete Spreadsheet Blank Rows API?

- **Utvecklarvänligt** – SDK:er finns för flera språk, vilket minskar utvecklingsarbetet jämfört med att bygga egna lösningar.
- **Lägre arbetskostnader** – Eliminerar behovet av manuell kalkylarksrensning eller dedikerat personal.
- **Betala per användning** – Du betalar endast för de API-anrop som du faktiskt gör.
- **Inga underhållskostnader** – Inga servrar att hantera, inga programuppdateringar och inga kompatibilitetsproblem.

## Hur man använder Delete Spreadsheet Blank Rows API med SDK:er

### Specifikation för Delete Spreadsheet Blank Rows API

[Delete Spreadsheet Blank Rows API Specification](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på lägre nivå och tillåter dig att ta bort tomma rader i kalkylark med kort kod.  
Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}  
{{</tab>}}  
{{< /tabs >}}