---
title: "Dekryptera en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Dekryptera en Excel-fil"
type: docs
url: /excel-file-decrypt/
aliases: [/decrypt-excel-workbooks/, /workbook/decrypt/]
keywords: "Aspose.Cells, Excel-dekryptering, REST API, moln-SDK"
description: "Lär dig hur du dekrypterar en Excel-arbetsbok med Aspose.Cells Cloud REST API. Innehåller nödvändiga parametrar, cURL-exempel, SDK-kodexempel och detaljerad felhantering."
ArticleTitle: "Så här dekrypterar du en Excel-arbetsbok med Aspose.Cells Cloud API"
weight: 50
---

**Förutsättningar**

- En giltig JWT-åtkomsttoken.
- Arbetsboken måste vara uppladdad till Aspose Cloud-lagring och dess sökväg anges i frågeparametern `folder`.

## DeleteDecryptWorkbook API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Frågeparametrar

| Parameternamn   | Typ    | Beskrivning                                      |
| --------------- | ------ | ------------------------------------------------ |
| folder          | string | Sökvägen till mappen med den ursprungliga arbetsboken. |
| storageName     | string | Namnet på lagringen där arbetsboken finns.      |

### Request Body Parameter

| Parameternamn | Typ                      | Beskrivning                                   |
| ------------- | ------------------------ | --------------------------------------------- |
| encryption    | WorkbookEncryptionRequest | Krypteringsinställningar som krävs för dekryptering. |

### WorkbookEncryptionRequest

| Parameternamn | Typ     | Beskrivning                                                                                                   |
| ------------- | ------- | ------------------------------------------------------------------------------------------------------------- |
| EncryptionType | string  | Krypteringsalgoritm (`XOR`, `Compatible`, `EnhancedCryptographicProviderV1`, `StrongCryptographicProvider`). |
| KeyLength      | integer | Längden på krypteringsnyckeln i bitar.                                                                        |
| Password       | string  | Lösenord som används för dekryptering.                                                                        |

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**Exempel på felaktiga svar**

```json
{
  "Code": "400",
  "Message": "Ogiltiga begärparametrar."
}
```

```json
{
  "Code": "401",
  "Message": "Autentisering misslyckades. Ogiltig eller saknad JWT-token."
}
```

```json
{
  "Code": "413",
  "Message": "Nyttolast för stor. Den uppladdade filen överskrider den tillåtna storleken."
}
```

```json
{
  "Code": "500",
  "Message": "Internt serverfel. Försök igen senare."
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                       |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Ogiltig begäran             | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad              | Ogiltig eller saknad JWT-token.                  |
| 413 | Payload för stor            | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel            | Oväntat serverfel.                               |

## Hur du använder DeleteDecryptWorkbook API med SDK:er

### DeleteDecryptWorkbook API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDecryptWorkbook) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 1280, "Password": "aspose"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projekts uppgifter. Ta en titt på [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDecryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDecryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDecryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDecryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteDecryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDecryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDecryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDecryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}