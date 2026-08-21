---
title: "Lägg till en pivot-tabell i ett Excel-ark"
second_title: "Dokument"
linktitle: Lägg till
type: docs
url: /sv/pivot-tables/add/
aliases: [  /sv/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Lägg till pivot-tabell, Excel-ark, Aspose.Cells Cloud, REST API, SDK, Excel-pivot-tabell"
description: "Använd Aspose.Cells Cloud REST API för att lägga till en pivot-tabell i ett Excel-ark. Tillgängligt via SDK:er för C#, Java, PHP, Python, Node.js, Android, Swift, Perl och Go."
weight: 30
ArticleTitle: "Hur man lägger till en pivot-tabell i ett Excel-ark med Aspose.Cells Cloud"
---

Denna REST API lägger till en pivot-tabell i ett ark.

**Förutsättningar:**  
- Ett Aspose.Cells Cloud-konto med en giltig JWT-access-token.  
- Den mål-fil som ska lagras i ett stödd lagringsplats (standardlagring eller en användarspecifik lagring).  
- Arket som anges av `sheetName` måste finnas i arbetsboken.  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token-baserad autentisering</a>.

### **Begäringsparametrar**

| Parameternamn   | Typ     | Plats  | Beskrivning                                                                                                                         |
| --------------- | ------- | ------ | ----------------------------------------------------------------------------------------------------------------------------------- |
| name            | string  | path   | Namnet på Excel-dokumentet.                                                                                                         |
| sheetName       | string  | path   | Namnet på arket där pivot-tabellen ska skapas.                                                                                     |
| request         | object  | body   | `CreatePivotTableRequest` DTO som innehåller definitionen för pivot-tabellen.                                                      |
| folder          | string  | query  | Mappen som innehåller dokumentet.                                                                                                  |
| storageName     | string  | query  | Namnet på lagringsplatsen där dokumentet finns.                                                                                    |
| sourceData      | string  | query  | Det interval som tillhandahåller källdata för den nya pivot-tabellens cache (t.ex. `A5:E10`).                                       |
| destCellName    | string  | query  | Adressen till den övre vänstra cellen i målintervallet för pivot-tabellrapporten.                                                  |
| tableName       | string  | query  | Namnet som tilldelas den nya pivot-tabellen.                                                                                        |
| useSameSource   | boolean | query  | När `true` återanvänder den nya pivot-tabellen en befintlig källdatakälla, vilket sparar minne om en annan pivot-tabell redan använt den här källan. |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud API:et med cURL.

**Säkerhetsnotering:** Använd alltid `https://` när du anropar API:et och håll din JWT-token hemlig; vid överföring via vanlig HTTP kan token exponeras för avlyssning.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                    |
|-----|-----------------------------|----------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad               | Ogiltig eller saknad JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksbegränsningen. |
| 500 | Internt serverfel           | Oväntat serverfel. |

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

För fler åtgärder, se relaterade API-sidor: **[Hämta en pivot-tabell](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Ta bort en pivot-tabell](https://docs.aspose.cloud/cells/pivot-tables/delete/)** och **[Uppdatera en pivot-tabell](https://docs.aspose.cloud/cells/pivot-tables/update/)**.