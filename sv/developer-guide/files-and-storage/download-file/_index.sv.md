---
title: "Aspose.Cells Cloud Download File API – Gränssnitt för snabb filhämtning i molnet"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud Download File API – Gränssnitt för snabb filhämtning i molnet"
linktitle: "Download File API"
type: docs
url: /sv/download-file/
keywords: "Aspose.Cells, Download File API, Excel-molnlagring, REST API, filhämtning, PDF, CSV, SDK"
description: "Hämta Excel-filer, PDF-filer, CSV-filer och andra format från Aspose.Cells Cloud-lagring med Download File API (v4.0). Inkluderar slutpunkt, parametrar, autentiseringsinformation och kodexempel."
weight: 100
---

**DownloadFile**-API:t låter dig hämta filer som lagras i Aspose.Cells Cloud-lagring. Download File API är avgörande för att komma åt Excel-kalkylblad, PDF-filer, CSV-filer och andra format som stöds direkt från molnet.

## **Excel API: Hämta fil**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begäranparametrar för **DownloadFile**-API:t är

| Parameter_name | Typ    | Plats (Sökväg / Fråga) | Beskrivning                                                   |
| -------------- | ------ | ---------------------- | ------------------------------------------------------------- |
| path           | String | Sökväg                 | Den virtuella sökvägen till den fil du vill hämta.            |
| storageName    | String | Fråga                  | Namnet på lagringen från vilken filen ska hämtas.             |
| versionId      | String | Fråga                  | Filens versionsidentifierare, om tillämpligt.                |

### **Svar**

API:et returnerar en **binär filström**. `Content-Type`-huvudet matchar filformatet (t.ex. `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` för XLSX). Inget JSON-svar returneras.

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                     |
| --- | --------------------- | --------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad     | Ogiltig eller saknad JWT-token.                                |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.              |
| 500 | Internt serverfel     | Oväntat serverfel.                                              |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FileController/DownloadFile) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till moln-API:t med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/Example.xlsx?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/octet-stream" \
     -o Example.xlsx
```

{{< /tab >}}

{{< tab tabNum="12" >}}

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-repositoriet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DownloadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DownloadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DownloadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DownloadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DownloadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DownloadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DownloadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DownloadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

---