---
title: "Lägg till ett Excel-ark"
ArticleTitle: "Lägg till ett Excel-ark - Aspose.Cells Cloud API-guide"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /worksheets/add/
aliases: [/add-a-new-excel-worksheet/]
keywords: "Lägg till Excel-ark, Aspose.Cells Cloud, REST API, PUT-ark, Excel-arbetsbok, API-förfrågan"
description: "Steg-för-steg-guide för att lägga till ett nytt ark i en Excel-arbetsbok med Aspose.Cells Cloud REST API, inklusive förfrågningsdetaljer, ett cURL-exempel och SDK-kodfragment för flera språk."
weight: 20
---

Denna REST API lägger till ett nytt ark i en befintlig arbetsbok.

**Förutsättningar**: För att anropa denna slutpunkt måste du ha en giltig Aspose Cloud-autentiseringstoken, målarbetsboken måste vara uppladdad till Aspose Cloud-lagring och du bör känna till lagringsnamnet (om du använder en anpassad lagring).

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Förfrågningsparametrar**

| Parameternamn | Typ     | Plats  | Beskrivning                                            |
| ------------- | ------- | ------ | ------------------------------------------------------ |
| name          | string  | path   | Namn på arbetsboksfilen.                               |
| sheetName     | string  | path   | Namn på det nya ark som ska skapas.                    |
| position      | integer | query  | Position (nollbaserad) där arket ska infogas.         |
| sheettype     | string  | query  | Typ av det nya arket (t.ex. **Chart**, **Dialog**).   |
| folder        | string  | query  | Mapp som innehåller arbetsboken.                       |
| storageName   | string  | query  | Namn på Aspose Cloud-lagringen.                        |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Worksheets/PutAddNewWorksheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör en anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks" \
-X PUT \
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

**Möjliga svarsstatuskoder**

| Statuskod | Beskrivning                                         |
|-----------|-----------------------------------------------------|
| 200       | Arket lades framgångsrikt till.                    |
| 400       | Felaktig förfrågan – ogiltiga parametrar.          |
| 401       | Otillåten – autentiseringstoken saknas eller är ogiltig. |
| 404       | Hittades inte – arbetsboken eller mappen finns inte. |
| 500       | Internt serverfel – oväntat tillstånd.             |

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på ditt projekt. Kolla in [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostPutAddNewWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPutAddNewWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPutAddNewWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPutAddNewWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPutAddNewWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPutAddNewWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPutAddNewWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPutAddNewWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}