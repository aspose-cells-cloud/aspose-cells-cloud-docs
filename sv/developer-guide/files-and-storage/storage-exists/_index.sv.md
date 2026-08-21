---
title: "Kontrollera om ett lagringsutrymme finns – Aspose.Cells Cloud API (v4.0)"
second_title: "Dokument"
ArticleTitle: "Webbaserad Excel-filhantering – Kontrollera om lagringsutrymme finns"
linktitle: "Lagringsutrymme finns"
type: docs
url: /sv/storage-exists/
keywords: "Aspose.Cells, lagringsutrymme finns, molnlagrings-API, REST, Excel"
description: "Kontrollera om ett lagringsutrymme finns i Aspose.Cells Cloud. Lär dig om GET /v4.0/cells/storage/{storageName}/exist-slutpunkten, nödvändiga parametrar, svarsformat och se SDK-exempel i C#, Java, Python med mera."
weight: 100
---

`storageExists`-API:et kontrollerar om ett specificerat lagringsutrymme finns i Aspose.Cells-moltjänsten. Denna funktionalitet är avgörande för att säkerställa att alla åtgärder som beror på lagringsutrymmet kan utföras utan fel.

**Sammanfattning** – `storageExists`-slutpunkten låter dig bekräfta att ett specifikt lagringsutrymme finns tillgängligt i Aspose.Cells Cloud. Använd den före filrelaterade åtgärder för att undvika körningsfel.

## Kontrollera om ett lagringsutrymme finns (storageExists)

### Webb-API

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:erna är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameter Name | Typ    | Plats  | Beskrivning                                                |
| -------------- | ------ | ------ | ---------------------------------------------------------- |
| storageName    | String | Path   | Namnet på det lagringsutrymme som ska kontrolleras för närvarande. |

### **Svar**

```json
{
  "Name": "StorageExist",
  "Description": ["Anger om det angivna lagringsutrymmet finns."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Anger om lagringsutrymmet finns.",
        "Detta egenskap returnerar true om lagringsutrymmet finns; annars returneras false."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter applicerades utan fel; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad         | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## Hur använder man storage exists-API:et med SDK:er?

### OpenAPI-specifikation

<a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">OpenAPI-specifikationen</a> definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket tillåter utvecklare att enkelt interagera med REST-API:et direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är den mest effektiva metoden för att påskynda utvecklingen. Ett SDK abstraher bort detaljer i den lågnivåimplementeringen, vilket gör att utvecklare kan fokusera på sina projektuppgifter. För en komplett lista över tillgängliga Aspose.Cells Cloud SDK:er, besök <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">GitHub-förrådet</a>.

Följande kodexempel visar hur man gör API-anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}