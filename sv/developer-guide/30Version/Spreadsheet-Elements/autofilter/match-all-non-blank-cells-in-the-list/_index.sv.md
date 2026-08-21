---
title: "Matcha alla icke‑tomma celler i ett Excel-ark"
second_title: "Dokument"
linktitle: "Matcha alla icke‑tomma celler"
type: docs
url: /autofilter/match-all-non-blank/
aliases: [/match-all-non-blank-cells-in-the-list/]
keywords: "Aspose.Cells Cloud, matcha icke‑tomma celler, AutoFilter, Excel API"
description: "Lär dig hur du använder Aspose.Cells Cloud REST API för att matcha alla icke‑tomma celler i en AutoFilter-lista på ett Excel-ark. Innehåller endpoint, parametrar, autentisering, svarsschema, felkoder och SDK-exempel."
ArticleTitle: "Matcha alla icke‑tomma celler i ett Excel-ark med Aspose.Cells Cloud API"
weight: 100
---

**Översikt**  
Operationen *Matcha alla icke‑tomma celler* tillämpar en AutoFilter på ett ark och returnerar endast de rader där den angivna kolumnen innehåller data, och ignorerar tomma celler. Detta är användbart för att rensa datamängder, generera rapporter eller förbereda data för vidare analys.

**Förutsättningar**  
- En giltig JWT-token för autentisering hos Aspose.Cells Cloud.  
- Arbetsboken måste vara uppladdad till Aspose Cloud-lagring.  
- Du behöver filnamnet, arkets namn och den nollbaserade kolumnindexpositionen (`fieldIndex`) du vill filtrera.

Detta REST API matchar alla icke‑tomma celler i AutoFilter-listan på ett Excel-ark.

## PostWorksheetMatchNonBlanks API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/matchNonBlanks
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameternamn   | Typ     | Plats  | Beskrivning                                                   |
| --------------- | ------- | ------ | ------------------------------------------------------------- |
| name            | string  | path   | Filnamnet på Excel-filen.                                     |
| sheetName       | string  | path   | Namnet på arket som innehåller AutoFiltern.                   |
| fieldIndex      | integer | query  | Nollbaserat index för den kolumn som filtert ska tillämpas på. |
| folder          | string  | query  | _(Valfritt)_ Mappväg där filen lagras.                         |
| storageName     | string  | query  | _(Valfritt)_ Namn på den lagringstjänst som ska användas.      |

### **Svar**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-statuskoder**

| Kod  | Betydelse                   | Beskrivning                                            |
|------|-----------------------------|--------------------------------------------------------|
| 200  | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens information. |
| 400  | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Ej auktoriserad             | Ogiltig eller saknad JWT-token.                        |
| 413  | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.      |
| 500  | Internt serverfel           | Oväntat serverfel.                                     |

*Exempel på felaktigt svar (400)*  

```json
{
  "Code": 400,
  "Message": "Ogiltig parameter: fieldIndex måste vara ett icke‑negativt heltal."
}
```

## Hur du använder PostWorksheetMatchNonBlanks API med SDK:er

### PostWorksheetMatchNonBlanks API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetMatchNonBlanks) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/matchNonBlanks?fieldIndex=0" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMatchNonBlanks.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMatchNonBlanks.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMatchNonBlanks.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMatchNonBlanks.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMatchNonBlanks.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMatchNonBlanks.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMatchNonBlanks.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMatchNonBlanks.go" >}}

{{< /tab >}}

{{< /tabs >}}