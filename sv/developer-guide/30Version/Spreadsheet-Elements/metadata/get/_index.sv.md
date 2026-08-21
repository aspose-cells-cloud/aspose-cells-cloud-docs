---
title: "Hämta metadata från Excel-filer"
second_title: "Dokument"
linktitle: "Hämta utan att använda lagring"
type: docs
url: /sv/metadata/get/
keywords: "Aspose.Cells, Excel, metadata, REST API, molntjänst"
description: "Hämta inbyggda eller anpassade metadata från Excel-arbetsböcker med Aspose.Cells Cloud REST API. Inkluderar begäranformat, parametrar, exempel på SDK-kod och felhantering."
weight: 23
ArticleTitle: "Hämta metadata från Excel-filer - Aspose.Cells Cloud API"
---

Denna REST API hämtar **metadata** från en eller flera Excel-filer.  
Begäran måste inkludera ett `Authorization: Bearer <access_token>`-huvud som erhållits via OAuth 2.0-klientautentisering.

**Förutsättningar**: För att kunna anropa denna slutpunkt måste du ha en giltig åtkomsttoken som erhållits från Aspose Clouds OAuth 2.0-tokenslutpunkt. Exempel på curl-begäran för att erhålla en token:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Frågeparameter

| Parameternamn | Typ    | Beskrivning                                                                 |
| ------------- | ------ | --------------------------------------------------------------------------- |
| type          | string | `ALL` / `BuiltIn` / `Custom` – anger vilka metadatagrupper som ska returneras. |

### Begärans brödtextparameter

| Parameternamn | Typ       | Beskrivning                                                             |
| ------------- | --------- | ----------------------------------------------------------------------- |
| excel file    | datafil   | Excel-filen som skickas som första del i multipart-begäran.            |

### Svar

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| Kod | Betydelse               | När                                |
|-----|-------------------------|------------------------------------|
| 200 | Lyckades                | Metadata har returnerats.          |
| 400 | Ogiltig begäran         | Fil saknas eller ogiltig fråga.    |
| 401 | Obehörig                | Ogiltig eller saknad token.        |
| 404 | Hittades inte           | Angiven fil kunde inte hittas.     |
| 500 | Internt serverfel       | Oväntat serverfel uppstod.         |

API:et returnerar dessa standard-HTTP-statuskoder tillsammans med ett JSON-objekt som beskriver felet, om relevant.

### Molntjänstfamilj

Att använda en SDK accelererar utvecklingen genom att hantera detaljer på låg nivå. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:n:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}
---