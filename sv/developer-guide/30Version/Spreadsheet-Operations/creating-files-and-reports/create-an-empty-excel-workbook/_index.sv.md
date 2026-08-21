---
title: "Skapa en tom Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Tom arbetsbok"
type: docs
url: /sv/create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, moln, Excel, tom arbetsbok, REST API, SDK"
description: "Lär dig hur du skapar en tom Excel-arbetsbok med Aspose.Cells Cloud REST API. Innehåller cURL- och SDK-exempel."
weight: 20
ArticleTitle: "Skapa en tom Excel-arbetsbok med Aspose.Cells Cloud API"
---

Denna REST API skapar en **tom arbetsbok**.

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Frågeparametrar

| Parameternamn  | Typ    | Beskrivning                                                  |
| -------------- | ------ | ------------------------------------------------------------ |
| templateFile   | string | Sökväg till en mallarbetsbok som ska användas som bas (valfritt). |
| dataFile       | string | Sökväg till en datafil för att fylla i arbetsboken (valfritt). |
| isWriteOver    | boolean | `true` för att skriva över en befintlig fil; `false` annars. |
| folder         | string | Målmapp för den skapade arbetsboken (valfritt).              |
| storageName    | string | Namn på den lagringstjänst som ska användas.                 |

### Begäranhållningsparameter

| Parameternamn | Typ | Beskrivning                                   |
| ------------- | --- | --------------------------------------------- |
| data          | file | Binärt innehåll i den arbetsboksfil som ska skapas. |

### **Svar**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | När den returneras                        |
|-----|-----------------------------|-------------------------------------------|
| 200 OK | Arbetsboken skapades lyckades | Normalt flöde                             |
| 201 Created | Arbetsboken skapades (alternativt svar) | När API:et returnerar en "created"-status |
| 400 Bad Request | Ogiltiga parametrar | Klientsidigt fel                           |
| 401 Unauthorized | Saknas eller ogiltig token | Autentiseringsfel                         |
| 409 Conflict | Filen finns och `isWriteOver=false` | Konflikt med befintlig fil                |

## Hur du använder PutWorkbookCreate API med SDK:er

### PutWorkbookCreate API-specificering

[OpenAPI-specificeringen](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för att komma åt Aspose.Cells-webbtjänster. Inkludera `Authorization`-huvudet med en giltig OAuth2/JWT-åtkomsttoken. För en tom arbetsbok är begäranhållningen valfri; om du behöver ladda upp en fil lägger du till `--data-binary @empty.xlsx` enligt nedan.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Skapa en tom arbetsbok med namnet newworkbook.xlsx
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Uteslut denna rad för en helt tom arbetsbok
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

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---