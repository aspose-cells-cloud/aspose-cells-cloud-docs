---
title: "Avskydda Excel-arbetsbok – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Avskydda Excel-fil"
type: docs
url: /excel-file-unprotect/
aliases:
  - /unprotect-excel-workbooks/
  - /workbook/unprotect/
keywords: "Aspose Cells, API för att avskydda Excel, ta bort skydd av arbetsbok, REST API, moln kalkylark"
description: "Lär dig hur du tar bort skydd från en Excel-arbetsbok med Aspose.Cells Cloud REST API. Innehåller begärsyntax, parametrar, cURL-exempel och SDK-kod i flera språk."
weight: 60
ArticleTitle: "Avskydda Excel-arbetsbok – Aspose.Cells Cloud API"
---

Använd detta REST API för att avskydda en Excel-arbetsbok.

## DeleteUnProtectWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Sökvägparametrar

| Parameter | Typ    | Beskrivning                                       | Krävs |
| --------- | ------ | ------------------------------------------------- | ----- |
| **name**  | string | Namn på arbetsboksfilen (inklusive filtillägg).   | Ja    |

### Frågeparametrar

| Parameternamn | Typ   | Beskrivning                                             |
| ------------- | ----- | ------------------------------------------------------- |
| folder        | string | Sökväg till mappen som innehåller den ursprungliga arbetsboken. |
| storageName   | string | Namn på lagringstjänsten där arbetsboken finns.        |

### Begärandetextparametrar

| Parameternamn | Typ                       | Beskrivning                                             |
| ------------- | ------------------------- | ------------------------------------------------------- |
| protection    | WorkbookProtectionRequest | Objekt som anger vilka skyddinställningar som ska tas bort. |

#### WorkbookProtectionRequest

| Parameternamn   | Typ    | Beskrivning                                                                                              |
| --------------- | ------ | -------------------------------------------------------------------------------------------------------- |
| ProtectionType  | string | Typ av skydd som ska tas bort (`ALL`, `CONTENTS`, `NONE`, `OBJECTS`, `SCENARIOS`, `STRUCTURE`, `WINDOWS`). |
| Password        | string | Lösenord som krävs för att ta bort skyddet (valfritt).                                                   |

#### cURL-exempel

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -d '{ "ProtectionType": "ALL", "Password": "aspose"}'
```

#### Svar (Lyckades)

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### HTTPS-statusfelresponser

| HTTP-status | Kod                 | Beskrivning                                                 |
| ----------- | ------------------- | ----------------------------------------------------------- |
| 400         | BadRequest          | Saknade eller ogiltiga parametrar.                          |
| 401         | Unauthorized        | Ogiltig eller saknad åtkomsttoken.                          |
| 404         | NotFound            | Den angivna arbetsboken hittades inte i den angivna mappen/lagringen. |
| 500         | InternalServerError | Oväntat serverfel.                                          |

## Hur du använder DeleteUnProtectWorkbook API med SDK:er

### DeleteUnProtectWorkbook API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Protection/DeleteUnProtectWorkbook) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK förenklar integrationen och minskar mängden repetitiv kod. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteUnProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteUnProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteUnProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteUnProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteUnProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteUnProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteUnProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteUnProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---