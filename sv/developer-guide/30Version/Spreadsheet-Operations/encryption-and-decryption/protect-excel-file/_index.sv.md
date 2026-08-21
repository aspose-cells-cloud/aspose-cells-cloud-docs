---
title: "Säkerhetskopiera en Excel-arbetsbok med Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Säkerhetskopiera en Excel-fil"
type: docs
url: /sv/protect-excel-file/
aliases: [  /sv/protect-excel-workbooks/ , /sv/workbook/protect/ ]
keywords: "Aspose.Cells, Excel-säkerhet, API, REST, SDK"
description: "Lär dig hur du säkerhetskopierar en Excel-arbetsbok via Aspose.Cells Cloud REST API. Innehåller autentiseringssteg, fråge- och brödparametrar, cURL-förfrågan och SDK-kodexempel för C#, Java, PHP, Ruby, Node.js, Python, Perl och Go."
weight: 30
ArticleTitle: "Säkerhetskopiera en Excel-arbetsbok med Aspose.Cells Cloud API"
---

Denna REST API **säkerhetskopierar** en Excel-arbetsbok, vilket möjliggör säkerhetskopiering av en Excel-arbetsbok med lösenord och skyddsalternativ med Aspose.Cells Cloud.

## PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Frågeparametrar

| Parametername   | Typ    | Beskrivning                                                  |
| --------------- | ------ | ------------------------------------------------------------ |
| folder          | string | Mapp som innehåller källarbetsboken. _(valfritt)_            |
| storageName     | string | Namn på lagringsplatsen. _(valfritt; standard = "Default")_ |

### Brödparametrar för förfrågan

| Parametername | Typ                       | Beskrivning                                                   |
| ------------- | ------------------------- | ------------------------------------------------------------- |
| protection    | WorkbookProtectionRequest | Objekt som definierar skyddsalternativen för arbetsboken.    |

#### WorkbookProtectionRequest

| Parametername   | Typ    | Beskrivning                                                                                                                                                   |
| --------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType  | string | Typ av skydd att tillämpa. Tillåtna värden (skiftlägesokänsliga): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password        | string | Valfritt lösenord att ange för skyddet.                                                                                                                       |

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                                 |
|-----|-----------------------------|------------------------------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller detaljer om åtgärden.   |
| 400 | Bad Request                 | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).            |
| 401 | Unauthorized                | Ogiltig eller saknad JWT-token.                                              |
| 413 | Payload Too Large           | Den uppladdade filen överskrider storleksgränsen.                           |
| 500 | Internal Server Error       | Oväntat serverfel.                                                           |

## Hur du använder PostProtectDocument API med SDK:er

### Krav

Innan du anropar API:et, se till att du har slutfört följande steg:

- **Skaffa en JWT-åtkomsttoken** enligt autentiseringsflödet som beskrivs i säkerhetssektionen.  
- **Ladda upp arbetsboken** till din Aspose Cloud-lagring eller bekräfta att den redan finns i målmappen.  
- **Känna till lagringsnamnet** (standard är `"Default"` om inte angivet) och det exakta filnamnet du vill skydda.

### PostProtectDocument API-specifikation

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Exempel: Skydda en arbetsbok med cURL

1. Skaffa en åtkomsttoken enligt beskrivningen i **Krav / Autentisering**.  
2. Kör förfrågan:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   Svaret kommer att innehålla ett statusobjekt som bekräftar att skyddet lyckades.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla mot Aspose.Cells Cloud. En SDK abstraherar lågnivådetaljer, så att du kan fokusera på din affärslogik. Se <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Exempel på fullständigt svar

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```