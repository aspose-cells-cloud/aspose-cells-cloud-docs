---
title: "Säkerhetskopiera Excel-filer"
second_title: "Dokument"
linktype: "Kryptera Excel-filer"
type: docs
url: /sv/protect-excel-files/
aliases:
  [
    "/protect/without-storage/",
    "/protect/without-using-storage/",
    "/protect/without-using-storage/",
  ]
keywords: "Aspose.Cells, API för Excel-skydd, kryptera Excel-arbetsbok, molnbaserad kalkylarkssäkerhet, REST API"
description: "Använd Aspose.Cells Cloud REST API för att skydda Excel-filer. Denna guide visar hur du krypterar arbetsböcker via HTTP POST, cURL och SDK:er för flera programmeringsspråk, såsom 2026."
weight: 40
---

Denna REST API skyddar Excel-filer.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/protect
```

### Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Begäranparametrar

| Parameternamn | Typ   | Plats                     | Beskrivning                            |
| -------------- | ------ | ------------------------- | -------------------------------------- |
| file           | fil   | formData (body)           | Fil som ska laddas upp                 |
| password       | sträng | frågesträng (`password`) | Lösenord som används för att skydda arbetsboken |

### Svar


```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename": "skyddat filnamn: smaple1.xlsx",
      "FileSize": storlek,
      "FileContent": "-----Base64-sträng för sample1-----"
    },
    {
      "Filename": "skyddat filnamn: sample2.xlsx",
      "FileSize": storlek,
      "FileContent": "-----Base64-sträng för sample2-----"
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK                          | Filter tillämpades framgångsrikt; svaret innehåller detaljer om åtgärden. |
| 400  | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401  | Oautentiserad               | Ogiltig eller saknad JWT-token. |
| 413  | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen. |
| 500  | Internt serverfel           | Oväntat serverfel. |
## Hur man använder PostProtect-API:et med SDK:er

### PostProtect API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostProtect) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du anropar Cloud API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/protect?password=MySecretPwd" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@sample1.xlsx' \
  -F 'file2=@sample2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "sample1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng för sample1-----"
    },
    {
      "Filename": "sample2.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng för sample2-----"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### **Felhantering**

– API:et kan returnera följande statuskoder:

| HTTP-kod | Betydelse                               | Exempel på JSON-felmeddelande                        |
| -------- | --------------------------------------- | ---------------------------------------------------- |
| 400      | Felaktig begäran (t.ex. saknad fil)     | `{"Code":400,"Message":"Fil krävs."}`               |
| 401      | Oautentiserad (ogiltig eller saknad token) | `{"Code":401,"Message":"Ogiltig åtkomsttoken."}`    |
| 403      | Förbjuden (otillräckliga rättigheter)   | `{"Code":403,"Message":"Åtkomst nekad."}`           |
| 500      | Internt serverfel                       | `{"Code":500,"Message":"Oväntat serverfel."}`       |

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}