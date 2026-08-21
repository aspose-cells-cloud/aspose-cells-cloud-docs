---
title: "Kryptera en Excel-arbetsbok med Aspose.Cells Cloud API – Snabba cURL- och SDK-exempel"
secondtitle: "Dokument"
linktitle: "Kryptera en Excel-fil"
type: docs
url: /excel-file-encrypt/
aliases: [/encrypt-excel-workbooks/, /workbook/encrypt/]
keywords: "Aspose Cells kryptera arbetsbok, Excel-krypterings-API, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Lär dig hur du krypterar en Excel-arbetsbok med Aspose.Cells Cloud REST API (v3.0). Innehåller cURL-kommando, SDK-kodexempel (C#, Java, Python, …), nödvändiga parametrar och felhantering."
weight: 20
ArticleTitle: "Kryptera Excel-arbetsbok med Aspose.Cells Cloud API – cURL- och SDK-exempel"
---

Denna REST API krypterar en Excel-**arbetsbok**.

**Förutsättningar:** Du måste ha ett giltigt JWT-token och arbetsboken redan uppladdad till ett lagringsplats innan du anropar denna slutpunkt.

## PostEncryptDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Frågeparametrar**

| Parameternamn   | Typ    | Obligatorisk | Beskrivning                          |
| --------------- | ------ | ------------ | ------------------------------------ |
| folder          | string | ✗            | Sökvägen till mappen med den ursprungliga arbetsboken. |
| storageName     | string | ✗            | Namnet på den lagring som ska användas. |

### **Parametrar i begärandetexten**

| Parameternamn | Typ                       | Obligatorisk | Beskrivning                        |
| ------------- | ------------------------- | ------------ | ---------------------------------- |
| encryption    | WorkbookEncryptionRequest | ✓            | Krypteringsinställningar för arbetsboken. |

#### **WorkbookEncryptionRequest**

| Parameternamn  | Typ     | Obligatorisk | Beskrivning                                                                              |
| -------------- | ------- | ------------ | ---------------------------------------------------------------------------------------- |
| EncryptionType | string  | ✓            | Krypteringsalgoritm. Se tabellen nedan för stödda värden och deras betydelse.          |
| KeyLength      | integer | ✗            | Längden på krypteringsnyckeln i bitar (ignoreras för `XOR` och `Compatible`).           |
| Password       | string  | ✓            | Lösenord som används för kryptering.                                                     |

#### **Värden för EncryptionType**

| Värde                             | Beskrivning                                          |
| --------------------------------- | ---------------------------------------------------- |
| `XOR`                             | Enkel XOR-algoritm (äldre, låg säkerhet).           |
| `Compatible`                      | Excel 97‑2003-kompatibel kryptering (40‑bitars).    |
| `EnhancedCryptographicProviderV1` | AES‑128 med SHA‑1-hash.                              |
| `StrongCryptographicProvider`     | AES‑256 med SHA‑512-hash (starkaste versionen).      |

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                 |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oauktoriserad               | Ogiltigt eller saknat JWT-token.                            |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.          |
| 500 | Internt serverfel           | Oväntat serverfel.                                          |

## Hur du använder PostEncryptDocument API med SDK:er

### PostEncryptDocument API-specifikation

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör ett anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Kryptera arbetsboken "test.xlsx" med XOR-algoritmen (128‑bitars nyckel) och lösenordet "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Möjliga felaktiga svar**

| HTTP-status | Kod                 | Meddelande                                           |
| ----------- | ------------------- | ---------------------------------------------------- |
| 400         | BadRequest          | Saknade eller ogiltiga parametrar.                  |
| 401         | Unauthorized        | Autentiseringstoken saknas eller är ogiltigt.       |
| 403         | Forbidden           | Otillräckliga behörigheter för att komma åt lagringen. |
| 500         | InternalServerError | Oväntat serverfel.                                   |

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå så att du kan fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}
---