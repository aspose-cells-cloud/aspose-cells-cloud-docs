---
title: "Aspose.Cells Cloud Excel-add-in för att lägga till kalkylblad – Infoga nya kalkylblad med typ- och positionskontroll"
second_title: "Dokument"
ArticleTitle: "Hur man lägger till kalkylblad i Excel – Infoga nya kalkylblad på specifika platser"
linktitle: "Lägg till kalkylblad i kalkylark"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "excel, lägg till kalkylblad, aspose cells api, kalkylark, moln-api, kalkylbladstyp, kalkylbladsposition"
description: "Lär dig hur du programmatiskt lägger till ett nytt kalkylblad, diagramkalkylblad eller makrokalkylblad till en Excel-arbetsbok med Aspose.Cells Cloud API. Kontrollera kalkylbladstyp, namn och infogningsposition med ett enda REST-anrop."
weight: 100
---

Lägg programmatiskt till kalkylblad i Excel-filer med full kontroll över kalkylbladstyp och plats. Infoga vanliga kalkylblad, diagramkalkylblad eller makrokalkylblad på valfri plats i arbetsboken. Denna REST-baserade åtgärd möjliggör automatiserad hantering och organisering av Excel-arbetsböcker.

**Förutsättningar**

- Ett aktivt Aspose.Cells Cloud-konto med en giltig JWT-åtkomsttoken.
- Ett konfigurerat molnlagernamn (t.ex. `CompanyOneDrive`) där arbetsboken ska sparas.
- Målarbetsboken måste vara tillgänglig i den angivna lagringen och, om den är skyddad, måste det korrekta lösenordet anges.

| **Kalkylbladstyp**     | Beskrivning                                       |
| :--------------------- | :------------------------------------------------ |
| **VB**                 | Visual Basic-modul                                |
| **Worksheet**          | Vanligt kalkylblad                                |
| **Chart**              | Diagramkalkylblad                                 |
| **BIFF4Macro**         | BIFF4-makrokalkylblad                             |
| **InternationalMacro** | Internationellt makrokalkylblad                   |
| **Other**              | Anpassad eller mindre vanlig kalkylbladstyp som inte listas ovan |
| **Dialog**             | Dialogkalkylblad                                  |

## **Lägg till kalkylblad i kalkylark – API**

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäransparametrar

| Parameter Name     | Typ     | Plats     | Beskrivning                                                                                                                                                                                          |
| :----------------- | :------ | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Fil     | FormData  | **Obligatorisk.** Excel-arbetsboken (.xlsx, .xls, etc.) till vilken ett nytt kalkylblad kommer att läggas till.                                                                                      |
| **sheetType**      | Sträng  | Fråga     | **Valfri.** Typen av kalkylblad som ska skapas. Acceptabla värden är `worksheet` (standard), `chartsheet`, `macrosheet`, `vbmodule` och `dialog`.                                                  |
| **position**       | Heltal | Fråga     | **Valfri.** Nullbaserat index där det nya kalkylbladet ska infogas. `0` infogar före det första kalkylbladet; `2` infogar som tredje kalkylblad. Utelämna för att lägga till kalkylbladet sist.     |
| **sheetName**      | Sträng  | Fråga     | **Valfri.** Namn på det nya kalkylbladet. Måste vara unikt inom arbetsboken. Om utelämnas genereras ett standardnamn som "BladX".                                                                  |
| **outPath**        | Sträng  | Fråga     | **Valfri.** Målmapp i molnlagringen där den ändrade arbetsboken ska sparas. Om `null` eller utelämnad sparas arbetsboken på samma plats som källfilen eller till en standardväg.                     |
| **outStorageName** | Sträng  | Fråga     | **Obligatorisk.** Identifierare för den konfigurerade molnlagringen (t.ex. `CompanyOneDrive`) där utdatafilen ska skrivas.                                                                          |
| **region**         | Sträng  | Fråga     | **Valfri.** Språkinställning (t.ex. `sv-SE`) som kan påverka formatering och regionala regler i det nya kalkylbladet.                                                                              |
| **password**       | Sträng  | Fråga     | **Valfri.** Lösenord för att dekryptera och ändra en lösenordsskyddad arbetsbok. Utelämna om filen inte är krypterad.                                                                               |

### Svar

Vid framgång returnerar API:et **HTTP 200 OK** (eller **201 Created** när en ny fil genereras) med den uppdaterade arbetsboksfilen.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter applicerades framgångsrikt; svaret innehåller åtgärddetaljer. |
| 400  | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401  | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413  | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500  | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör vi använda API:et för att lägga till kalkylblad i kalkylark?

- **Automatiserad rapportgenerering** – Skapa och infoga månadsvisa kalkylblad (t.ex. `2024‑05`) dynamiskt vid generering av rapporter över finansiella tillstånd.
- **Batch-mallinitiering** – Lägg till ett dedikerat analyskalkylblad för varje ny kund eller projekt vid generering av offert- eller förslagssatser i bulk.
- **Dynamisk instrumentpanelutvidgning** – Infoga nya diagramkalkylblad i realtid när nya datadimensioner blir tillgängliga.
- **Kompatibilitet och revisionsarkivering** – Lägg automatiskt till bevisinsamlingskalkylblad under årliga revisioner, med varje inspektionspunkt isolerad.
- För att ta bort ett kalkylblad, se åtgärden **[Ta bort kalkylblad](/delete-worksheet/)**.
- För att flytta ett kalkylblad, se åtgärden **[Flytta kalkylblad](/move-worksheet/)**.

## Varför bör du använda API:et för att lägga till kalkylblad i kalkylark?

- **Utvecklarvänligt** – Aspose.Cells Cloud tillhandahåller SDK:er för flera språk, vilket minskar utvecklingsarbetet och erbjuder omfattande dokumentation.
- **Lägre arbetskostnader** – Eliminerar behovet av manuell skapande av kalkylblad och repetitiva kopiera/klistra-uppgifter.
- **Betala per användning** – Du betalar endast för de API-anrop som du faktiskt gör.
- **Ingen underhållsbelastning** – Inga servrar att hantera, inga programuppdateringar och inga kompatibilitetsproblem.

## Hur man använder API:et för att lägga till kalkylblad i kalkylark med SDK:er

### API-specifikation för att lägga till kalkylblad i kalkylark

[API-specifikationen för att lägga till kalkylblad i kalkylark](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Blad1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/sökväg/till/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK abstraherar lågnivådetaljer, vilket gör att du kan lägga till ett kalkylblad med minimal kod. Se den fullständiga listan över SDK:er i [GitHub-förrådet](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur man anropar tjänsten med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}