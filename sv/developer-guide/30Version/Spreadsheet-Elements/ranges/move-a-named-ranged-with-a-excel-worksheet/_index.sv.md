---
title: "Flytta ett namngivet intervall med ett Excel-arbetsblad"
second_title: "Document"
linktitle: "Flytta"
type: docs
url: /sv/ranges/move/
aliases: [  /sv/move-a-named-range-with-an-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, flytta namngivet intervall, Excel-arbetsblad, REST API, intervallflyttning, SDK-exempel"
description: "Lär dig hur du flyttar ett namngivet intervall inom ett Excel-arbetsblad med Aspose.Cells Cloud REST API v3.0, inklusive detaljerad endpoint-info, autentisering, exempel och SDK-kodexempel."
weight: 20
ArticleTitle: "Flytta ett namngivet intervall med ett Excel-arbetsblad med Aspose.Cells Cloud API"
---

Att flytta ett namngivet intervall är en vanlig uppgift när du behöver omorganisera data programmässigt. Detta avsnitt förklarar hur du flyttar ett definierat intervall till en ny position på samma arbetsblad med Aspose.Cells Cloud REST API.

Detta REST API flyttar ett angivet intervall till ett målintervall på ett Excel-arbetsblad.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/moveto
```

### Autentisering
API:t kräver ett **Bearer JWT-token** som erhålls via Aspose Cloud OAuth-flödet. Inkludera token i `Authorization`-huvudet:

```
Authorization: Bearer <jwt token>
```

Token:t måste ha scope:et **Cells**.

### Förutsättningar
- Arbetsboken måste lagras i Aspose Cloud-lagring.  
- Angiv `storageName` och mappvägen (`folder`) om filen inte finns i rotkatalogen.  
- Använd den senaste Aspose.Cells Cloud SDK-versionen som stöder API-version **v3.0**.

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärans parametrar

| Namn           | Typ    | Plats  | Beskrivning |
|----------------|--------|--------|-------------|
| **name**       | string | path   | Namn på arbetsboksfilen |
| **sheetName**  | string | path   | Namn på arbetsbladet |
| **destRow**    | integer| query  | Startradindex för målintervall (0-baserat) |
| **destColumn**| integer| query  | Startkolumnindex för målintervall (0-baserat) |
| **range**      | object | body   | Definition av källintervall som ska flyttas |
| **folder**     | string | query  | Mappväg där arbetsboken lagras |
| **storageName**| string | query  | Namn på Aspose Cloud-lagringen |

### Begäran kropp (Request Body)

| Fält           | Typ    | Obligatoriskt | Beskrivning |
|----------------|--------|---------------|-------------|
| **ColumnCount**| integer| Nej | Antal kolumner i källintervall |
| **ColumnWidth**| integer| Nej | Bredd på varje kolumn (i punkter) |
| **FirstColumn**| integer| Nej | 0-baserat index för första kolumnen i källintervall |
| **FirstRow**   | integer| Nej | 0-baserat index för första raden i källintervall |
| **Name**       | string | Nej | Namn på intervallet (om det är ett namngivet intervall) |
| **RefersTo**   | string | Nej | A1-stilreferens som definierar intervallet |
| **RowCount**   | integer| Nej | Antal rader i källintervall |
| **RowHeight**  | integer| Nej | Höjd på varje rad (i punkter) |
| **Worksheet**  | string | Nej | Arbetsblad som innehåller källintervall |

### Arbetsflöde

1. **Ladda upp** arbetsboken till Aspose Cloud-lagring (om den inte redan finns).  
2. **Generera** en JWT-token med OAuth-endpointen.  
3. **Bygg** JSON-payload som beskriver källintervall.  
4. **Anropa** `moveto`-endpointen med nödvändiga path, query-parametrar och JSON-body.  
5. **Verifiera** svaret; en lyckad anrop returnerar status `200 OK`.

### Exempel på begäran/svar

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/moveto?destRow=20&destColumn=20" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{ 
  "ColumnCount": 7,
  "ColumnWidth": 19,
  "FirstColumn": 0,
  "FirstRow": 9,
  "Name": "MyRange",
  "RefersTo": "A10:G10",
  "RowCount": 1,
  "RowHeight": 15,
  "Worksheet": "Sheet1"
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

När ett fel inträffar innehåller svaret ett valfritt fält `ErrorMessage` som ger ytterligare information om felet.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |

**Svarschema**

| Fält | Typ | Beskrivning |
|------|-----|-------------|
| **Code** | integer | HTTP-liknande statuskod returnerad av API:t (t.ex. 200) |
| **Status** | string | Textuell beskrivning av resultatet (t.ex. "OK") |
| **ErrorMessage** | string (valfritt) | Mänsklig läsbara felinformation när anropet misslyckas |

## Moln SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektoppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med diverse SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMoveTo.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMoveTo.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMoveTo.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMoveTo.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMoveTo.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMoveTo.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMoveTo.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMoveTo.go" >}}

{{< /tab >}}

{{< /tabs >}}