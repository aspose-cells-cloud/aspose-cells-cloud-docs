---
title: "Ändra lösenordsskydd för en Excel-arbetsbok"
second_title: "Dokument"
linktitle: "Ändra lösenord för en Excel-fil"
type: docs
url: /sv/workbook/password/modify/
aliases:
  - /set-modify-password-of-excel-workbooks/
  - /workbook/modify-password/
keywords: "Excel-lösenord, Aspose.Cells Cloud, skrivskydd, REST API, ändra arbetsbokslösenord"
description: "Ändra skrivskyddslösenordet för en Excel-arbetsbok med Aspose.Cells Cloud REST API (v3.0). Innehåller exempel med cURL och SDK."
weight: 100
ArticleTitle: "Ändra lösenordsskydd för en Excel-arbetsbok – Aspose.Cells Cloud"
---

Denna REST API **ändrar skrivskyddslösenordet** för en befintlig Excel-arbetsbok.

Att uppdatera skrivskyddslösenordet programmatically möjliggör lösenordsbyte eller ersättning utan att behöva ladda ner filen. Det är särskilt praktiskt vid hantering av säkerhetsförsegelade arbetsböcker lagrade i Aspose.Cells Cloud-lagring.


## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Begärparametrar

| Parameternamn   | Typ    | Position    | Beskrivning                                       |
| --------------- | ------ | ----------- | ------------------------------------------------- |
| **name**        | string | path        | Namn på Excel-arbetsboken (obligatoriskt).         |
| **password**    | string | body (JSON) | Nytt skrivskyddslösenord att ange (obligatoriskt). |
| **folder**      | string | query       | Valfri mapp där arbetsboken är lagrad.             |
| **storageName** | string | query       | Valfritt namn på lagringstjänsten.                 |

### Svar

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP-statuskoder**

| Kod | Betyder                     | Beskrivning                                        |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknas eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Ej auktoriserad             | Ogiltigt eller saknat JWT-token. |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500 | Internt serverfel           | Oväntat serverfel. |
## Hur du använder PutDocumentProtectFromChanges API med SDK:er

### PutDocumentProtectFromChanges API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PutDocumentProtectFromChanges) definierar det offentligt tillgängliga programmeringsgränssnittet som låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. cURL-kommandot nedan visar hur man anropar Cloud API:et.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/writeProtection?folder=Samples&storageName=Default" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{ "Password": "aspose" }'
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

Att använda ett SDK är det snabbaste sättet att utveckla. Ett SDK hanterar detaljer på låg nivå och låter dig fokusera på din affärslogik. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutDocumentProtectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutDocumentProtectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutDocumentProtectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutDocumentProtectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutDocumentProtectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutDocumentProtectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutDocumentProtectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutDocumentProtectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
---