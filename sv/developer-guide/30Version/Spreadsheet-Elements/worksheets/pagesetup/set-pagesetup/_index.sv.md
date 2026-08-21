---
title: "Ställa in sidinställning för ett kalkylblad"
second_title: "Dokument"
linktype: "Ställa in sidinställning"
type: docs
url: /sv/set-page-setup/
keywords: "Aspose.Cells, Excel, sidinställning, REST API, kalkylblad, molntjänst"
description: "Lär dig hur du ställer in sidinställningen för ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Inkluderar begärandedetaljer, ett säkert HTTPS cURL-exempel, svarsstatuskoder och SDK-kodsnuttar för flera programmeringsspråk."
weight: 20
ArticleTitle: "Ställa in sidinställning för ett kalkylblad – Aspose.Cells Cloud API-guide"
---

Förutsättningar: För att kunna anropa denna API måste du ha en giltig JWT-token (OAuth) och arbetsboken måste finnas i en Aspose Cloud-lagringsplats där du har läs- och skrivbehörighet. Se till att token inkluderas i **Authorization**-headern och att ditt konto har nödvändig API-kvot.

Denna REST API ställer in sidinställningen för ett Excel-kalkylblad.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parameternamn | Typ    | Plats  | Beskrivning             |
| ------------- | ------ | ------ | ----------------------- |
| name          | string | path   | Dokumentets namn.       |
| sheetName     | string | path   | Kalkylbladets namn.     |
| pageSetup     | object | body   | Beskrivning av sidinställning. |
| folder        | string | query  | Dokumentmapp.           |
| storageName   | string | query  | Lagringsnamn.           |

**Exempel på JSON-svar för objektet `pageSetup`**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

<a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

API:et returnerar ett JSON-objekt som anger resultatet av operationen:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Möjliga svarsstatuskoder**

| Kod | Betydelse                   | När                                                        |
|-----|-----------------------------|------------------------------------------------------------|
| 200 | OK                          | Lyckad uppdatering av sidinställning                       |
| 400 | Felaktig begäran            | Ogiltig JSON-payload eller saknade obligatoriska fält     |
| 401 | Autentisering krävs         | Saknas eller ogiltig JWT-token                             |
| 404 | Hittades inte               | Arbetsboken eller kalkylbladets namn finns inte           |
| 500 | Internt serverfel           | Oväntat serverfel                                           |

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se i <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-arkivet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}
---