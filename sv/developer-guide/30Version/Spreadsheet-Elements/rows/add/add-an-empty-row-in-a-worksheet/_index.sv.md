---
title: "Lägg till en tom rad i ett Excel-ark"
ArticleTitle: "Lägg till en tom rad i ett Excel-ark med Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Rad"
type: docs
url: /rows/add/row/
aliases: [/add-an-empty-row-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, lägg till tom rad, kalkylark, REST API, infoga rad, molnspreadsheets"
description: "Använd Aspose.Cells Cloud REST API för att infoga en tom rad i ett Excel-ark. Stöder flera SDK:er (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) för snabb utveckling."
weight: 20
---

Denna REST API lägger till en ny rad i ett Excel-ark. Den infogar en tom rad vid den angivna nollbaserade indexpositionen.

**Förutsättningar:**  
- Ett giltigt Aspose Cloud-åtkomsttoken (Bearer JWT) måste inkluderas i `Authorization`-headern.  
- Den målarkivfil som ska bearbetas måste ha laddats upp till ditt Aspose Cloud-lagrum, och parametrarna `folder` och `storageName` ska peka på dess plats.

**Anteckningar:**  
- `rowIndex` är nollbaserat; infoga vid index 0 lägger till en rad högst upp i arket.  
- Excel-ark har högst 1 048 576 rader; försök att infoga utanför denna gräns resulterar i

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameternamn | Typ    | Plats | Beskrivning                                            |
| ------------- | ------ | ----- | ------------------------------------------------------ |
| name          | string | path  | Filnamnet på arbetsboken.                              |
| sheetName     | string | path  | Arkets namn.                                           |
| rowIndex      | integer | path | Den nollbaserade indexpositionen där den nya raden ska infogas. |
| folder        | string | query | Mappens sökväg i lagringen där arbetsboken finns.     |
| storageName   | string | query | Namnet på Aspose Cloud-lagringen som ska användas.     |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör det möjligt att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Obs:** Alla Aspose.Cells Cloud-slutpunkter kräver HTTPS. Använd den säkra `https://`-schemat för produktionsanrop.

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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                      |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Unauthorized                | Ogiltigt eller saknat JWT-token. |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internal Server Error       | Oväntat serverfel. |

*Exempel på ett fel svar (t.ex. när radindexet överskrider arkets gräns):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Radindex utanför giltigt intervall. Maximalt antal tillåtna rader: 1048576."
}
```

## Moln-SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lägre nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}