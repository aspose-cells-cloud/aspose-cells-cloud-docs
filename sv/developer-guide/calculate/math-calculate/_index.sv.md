---
title: "Aspose.Cells Cloud – Math Calculate API (Addera, subtrahera, multiplicera, dividera, %)"
second_title: "Dokument"
ArticleTitle: "Addera, subtrahera, multiplicera, dividera och procent i kalkylark/Excel"
linktype: "docs"
url: /sv/math-calculate/
keywords: "Math Calculate API, Aspose.Cells Cloud, Excel-beräkningar, addera, subtrahera, multiplicera, dividera, procent, bulk-Excel-behandling, REST API"
description: "Lär dig hur du använder Aspose.Cells Cloud Math Calculate API för att bulk-tillämpa adderings-, subtraherings-, multiplikations-, divisions- eller procentoperationer på Excel-intervall. Inkluderar begärandeformat, exempelkod och felhantering."
weight: 100
---

## **Introduktion**: Snabbberäkning i kalkylark – Addera, multiplicera, subtrahera, dividera och procentformler i en enda sammanhållen API

_För bulk-beräkningar över hela kolumner, rader eller tabeller utan att skriva en formel._

- **Grundläggande matematik**: addera, subtrahera, multiplicera eller dividera varje cell i ett intervall med ett valfritt tal
- **Procent**: öka/minska med %, eller beräkna % av ett tal (t.ex. +15 %, -8 %, 20 % av…)
- **Bulk**: tillämpa på tusentals celler omedelbart – ingen behov av drag-fyllning, arrayformler eller VBA

| **Beräkningsoperation** | Beskrivning |
| :---------------------- | :---------- |
| **Addera**              | +           |
| **Subtrahera**          | -           |
| **Multiplicera**        | \*          |
| **Dividera**            | /           |
| **Procent**             | %           |

## **Math Calculate API**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:erna är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### **Begärparametrar:**

| Parameter Name | Typ    | Path/Query String/HTTP Body | Beskrivning                                                                 |
| :------------- | :----- | :-------------------------- | :-------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | FormData                    | Ladda upp kalkylarkfilen för bearbetning.                                   |
| operation      | Sträng | Query                       | Den matematiska operation som ska utföras (Addera, Subtrahera, Multiplicera, Dividera och Procent). |
| value          | Sträng | Query                       | Ett värde som ska användas i beräkningen, om tillämpligt.                   |
| worksheet      | Sträng | Query                       | Namnet på det kalkylblad som operationen ska utföras på.                   |
| range          | Sträng | Query                       | Intervallet av celler som ska inkluderas i beräkningen.                     |
| region         | Sträng | Query                       | Inställning för kalkylarksregion.                                           |
| password       | Sträng | Query                       | Lösenordet för att öppna kalkylarkfilen, om den är skyddad.                 |

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

**HTTP-statuskoder**

| Kod | Betydelse              | Beskrivning                                                       |
| --- | ---------------------- | ----------------------------------------------------------------- |
| 200 | OK                     | Filter applicerades framgångsrikt; svaret innehåller detaljerad information om operationen. |
| 400 | Bad Request            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized           | Ogiltig eller saknad JWT-token.                                   |
| 413 | Payload Too Large      | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internal Server Error  | Oväntat serverfel.                                                |

## Var bör vi använda Math Calculate API?

- **Finans**: addera 13 % moms till en hel kolumn med inköpspriser.
- **Inventering**: multiplicera kg-kolumnen med 2,2046 för att bulk-omvandla till pounds.
- **Lön**: addera en fast bonus på 1 000 till bonuskolumnen för alla anställda.
- **Valutakonvertering**: dividera försäljningskolumnen med aktuell växlingskurs för att få belopp i USD.
- **Betygsättning**: subtrahera 5 poäng från varje elevs poäng som straff för närvarande.
- **E-handel**: tillämpa 15 % kampanjrabatt genom att minska produktpriser med ett klick.

## Varför bör du använda Math Calculate API?

- **Snabba Excel-beräkningar** – slutför månadsavslutrapporter på sekunder.
- **Bulk-procentökning i Excel** – uppdatera priser, prognoser, provisioner med ett klick.
- **Addera samma tal till hela kolumnen** – inventering, valutakonvertering, enhetskonvertering.
- **Excel utan formler** – icke-tekniska användare uppskattar enkelheten.
- Utveckling kan snabbt slutföras via befintliga SDK:er.

**Anteckningar**  
Den maximala filstorlek som stöds är 200 MB. Parametern `range` måste vara en giltig Excel-adress (t.ex. A1:B10). Väldigt stora kalkylblad kan kräva extra bearbetningstid.

## Hur man använder Math Calculate API med SDK:er

### Math Calculate API-specifikation

[Math Calculate-specifikationen](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) definierar ett offentligt tillgängligt programmeringsgränssnitt som tillåter utvecklare att interagera direkt med API:et från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljer på låg nivå, så att du kan utföra matematiska beräkningar per cell med endast lite kod.  
Se [Aspose.Cells Cloud SDK:er på GitHub](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}