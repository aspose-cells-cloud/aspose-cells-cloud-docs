---
title: "Aspose.Cells Cloud – Byt kolumner, rader och intervall (v4.0)"
second_title: "Dokument"
ArticleTitle: "Byt/utväxla data mellan kolumner, rader och celler i Excel"
linktype: "Swap Range"
type: docs
url: /swap-range/
keywords: "Aspose Cells, Excel API, Byt intervall, moln kalkylark"
description: "Byt kolumner, rader eller intervall i Excel-filer med Aspose.Cells Cloud API. Bevara formatering, formler och cellreferenser i en enda begäran."
weight: 100
---

Utväxla automatiskt data mellan valfria två kolumner, rader, intervall eller celler i Excel-filer med Aspose.Cells Cloud API. Swap Range API:t möjliggör exakt datautväxling med bevarande av all formatering, formler och cellreferenser. Det stöder komplex dataomorganisering, batchbearbetning och sömlös molnintegration för företagsarbetsflöden.

## **Swap Range API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begäranparametrar**

| Parameter Name     | Typ    | Plats      | Beskrivning                                                                                                                                   |
| ------------------ | ------ | ---------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Fil    | FormData   | **Obligatorisk.** Käll-Excel-arbetsboksfilen (`.xlsx`, `.xls`).                                                                               |
| **worksheet1**     | Sträng | Fråga      | **Obligatorisk.** Namnet på det kalkylblad som innehåller det första dataområdet.                                                            |
| **range1**         | Sträng | Fråga      | **Obligatorisk.** Cellintervall (t.ex. `A1:D10`) i `worksheet1` som ska bytas.                                                                |
| **worksheet2**     | Sträng | Fråga      | **Obligatorisk.** Namnet på det kalkylblad som innehåller det andra dataområdet (kan vara samma som `worksheet1`).                            |
| **range2**         | Sträng | Fråga      | **Obligatorisk.** Cellintervall (t.ex. `F1:I10`) i `worksheet2` som ska bytas. **Viktigt:** `range1` och `range2` måste ha identiska dimensioner. |
| **outPath**        | Sträng | Fråga      | **Valfri.** Mapp i molnlagring där den ändrade arbetsboken kommer att sparas.                                                                |
| **outStorageName** | Sträng | Fråga      | **Obligatorisk.** Namn på den konfigurerade molnlagringstjänsten (t.ex. `MyCompanyStorage`).                                                 |
| **region**         | Sträng | Fråga      | **Valfri.** Lokal inställning (t.ex. `sv-SE`, `en-US`, `ja-JP`) som kan påverka formatering.                                                 |
| **password**       | Sträng | Fråga      | **Valfri.** Lösenord för att dekryptera ett skyddat kalkylark. Utelämna om det inte är krypterat.                                              |

**Exempel på begäran (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

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

**Anteckningar:**  
- API:t returnerar den ändrade arbetsboken som en filström. Om `outPath` anges sparas filen även på den angivna platsen i molnlagringen.  
- Om intervallens dimensioner inte matchar får du ett **400 Bad Request**-fel.

### Felkoder

| Kod                  | Beskrivning                                                        |
| -------------------- | ------------------------------------------------------------------ |
| **400 Bad Request**  | Ogiltig begärans-URI eller icke matchande intervalldimensioner.   |
| **401 Unauthorized** | Ogiltig eller utgången åtkomsttoken; client-id eller hemlighet är felaktiga. |
| **404 Not Found**    | Den angivna kalkylarksfilen kan inte nås.                         |
| **500 Server Error** | Ett internt fel uppstod vid bearbetning av arbetsboken.            |

## Var bör vi använda Swap Range API?

- **Omräkning av finansiella modeller** – Omorganisera datablock (t.ex. flytta Q3-prognosen till Q4) med bevarande av formler och villkorlig formatering.
- **Dataflöden och ETL-proceser** – Byt ut rådataintervall mot rensade intervall i ett mellanlager-kalkylblad innan slutgiltig utdata skapas.
- **Felkorrigering och dataåterställning** – Snabbt korrigera felplacerad data utan manuell kopiering och klistra in.

## Varför använda Swap Range API?

- **Utvecklarvänligt** – SDK:er finns för flera programmeringsspråk, vilket minskar utvecklingsarbetet jämfört med att bygga egna lösningar.
- **Sänker arbetskostnader** – Automatiserar dataomfördelning, vilket minskar behovet av manuell sammanställning.
- **Betala per användning** – Du betalar bara för de API-anrop som du faktiskt gör.
- **Ingen underhållsbehov** – Inga servrar att hantera, ingen programvaruuppdatering och inga kompatibilitetsproblem.

## Hur man använder Swap Range API med SDK:er

### Swap Range API-specifikation

[Swap Range API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och gör att du kan byta intervall med kort kod. Se [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---