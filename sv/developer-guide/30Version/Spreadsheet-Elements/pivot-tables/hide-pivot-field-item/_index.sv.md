---
title: "Dölj pivotfältelement i en pivot tabell"
second_title: "Document"
linktitle: Dölj
type: docs
url: /sv/pivot-tables/hide-pivot-field-item/
aliases: [  /sv/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, dölj pivotfältelement, PivotTable API, REST API, moln SDK"
description: "Lär dig hur du döljer ett pivotfältelement i en pivot tabell med Aspose.Cells Cloud REST API. Innehåller begärandedetaljer, cURL-exempel och SDK-kodsnuttar för flera språk."
weight: 110
ArticleTitle: "Dölj pivotfältelement i en pivot tabell – Aspose.Cells Cloud API-guide"
---

Innan du anropar API:et, se till att du har:

* En giltig **JWT-åtkomsttoken** (tillgänglig via Aspose Cloud:s autentiseringsflöde).  
* Målarboksdokumentet uppladdat till ditt Aspose Cloud-lager.  
* Kalkylbladet och pivot tabellen redan skapade.

Dessa förutsättningar förhindrar autentiseringsfel och "resursen hittades inte"-svar. Följande steg beskriver den nödvändiga konfigurationen innan API:et anropas.

Detta REST API döljer ett pivotfältelement i en pivot tabell.

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärandeparametrar**

| Parameternamn   | Typ     | Plats   | Beskrivning                                                                                       |
| --------------- | ------- | ------- | ------------------------------------------------------------------------------------------------- |
| name            | string  | path    | Namn på Excel-filen.                                                                              |
| sheetName       | string  | path    | Kalkylbladet som innehåller pivot tabellen.                                                       |
| pivotTableIndex | integer | path    | Index för pivot tabellen inom kalkylbladet.                                                       |
| pivotFieldType  | string  | query   | Typ av pivotfält (Rad, Kolumn, Sida, Data etc.).                                                  |
| fieldIndex      | integer | query   | Nullbaserat index för pivotfältet som ska ändras.                                                 |
| itemIndex       | integer | query   | Index för det specifika elementet i fältet som ska döljas.                                        |
| isHide          | boolean | query   | Ställ in på **true** för att dölja elementet; **false** för att visa det.                         |
| needReCalculate | boolean | query   | Indikerar om pivot tabellen ska omberäknas efter ändringen. Standard är **false**.                |
| folder          | string  | query   | Mappväg där arbetsboken lagras.                                                                   |
| storageName     | string  | query   | Namn på lagringstjänsten.                                                                         |

**Snabbreferens för nödvändiga frågeparametrar**

- **pivotFieldType** – fältets typ (t.ex. `Row`).  
- **fieldIndex** – nullbaserat index för fältet som ska ändras.  
- **itemIndex** – nullbaserat index för elementet som ska döljas/visas.  
- **isHide** – `true` för att dölja, `false` för att visa.  
- **needReCalculate** – valfri, standardvärdet är `false`.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Exemplet nedan visar hur du anropar API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

**Svardetaljer**

| Statuskod | Beskrivning                                                           |
| --------- | --------------------------------------------------------------------- |
| 200       | Elementet döljdes framgångsrikt.                                     |
| 400       | Felaktig begäran – saknade eller ogiltiga parametrar.                |
| 401       | Otillåten begäran – ogiltig eller saknad JWT-token.                  |
| 500       | Serverfel – åtgärden kunde inte slutföras.                           |

**Obs:** Om angivet `fieldIndex` eller `itemIndex` ligger utanför giltigt intervall returnerar API:et ett **400 Bad Request**-svar.

## Moln SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla mot API:et. SDK:er hanterar detaljer på låg nivå så att du kan fokusera på din affärslogik. Se [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man döljer ett pivotfältelement med olika SDK:er.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Förbered arbetsboken och kalkylbladet
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Ladda upp arbetsboken
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Skapa kalkylbladet som ska innehålla pivot tabellen
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Skapa ett andra kalkylblad med exempeldatapunkter
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Importera exempeldatapunkter till Sheet2
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Avkortad för tydlighet
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Lägg till en pivot tabell till PivotSheet
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Dölj ett specifikt radfältselement
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Obs:** Kodexemplen förutsätter att du redan har konfigurerat autentisering (JWT-token) och att arbetsboken finns i den angivna lagringsmappen. Justera `folder`- och `storageName`-parametrarna enligt ditt miljöbehov.