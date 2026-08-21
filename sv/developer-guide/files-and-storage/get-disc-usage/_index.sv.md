---
title: "Aspose.Cells Cloud API – Hämta diskutrymme | Realtidsmätvärden för lagring"
second_title: "Dokument"
ArticleTitle: "Lösning för molnbaserad hantering av Excel-filer – Gränssnitt för att snabbt hämta diskutrymme i molnet."
linktitle: "Hämta diskutrymme"
type: docs
url: /sv/get-disk-usage/
keywords: "Aspose Cells, moln-API, diskutrymme, lagringsmätvärden, Excel, REST"
description: "Hämta realtidsdiskutrymme för Aspose.Cells Cloud. Lär dig GET /v4.0/cells/storage/disk-slutpunkten, nödvändig autentisering och exempel på svar."
weight: 100
---

**Hämta diskutrymme**-åtgärden returnerar realtidslagringsmätvärden för ditt Aspose.Cells Cloud-konto. Använd denna slutpunkt för att övervaka förbrukat och totalt diskutrymme.

- Hämtar nuvarande diskutrymme för Excel-API:et i Aspose Cloud-miljön.
- Låter utvecklare övervaka hur mycket lagringsutrymme deras program har förbrukat.
- Möjliggör proaktiv hantering av lagringsbegränsningar och kostnadsstyrning.

## Excel-API: GetDiskUsage

### Webb-API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn | Typ   | Plats  | Beskrivning                                             | Nödvändig |
| ------------- | ----- | ------ | ------------------------------------------------------- | --------- |
| storageName   | String | Fråga | Namnet på det lagringsutrymme som utrymmet ska hämtas för. | Valfri     |

### **Svar**

```json
{
  "Name": "DiskUsage",
  "Description": ["Klass för information om diskutrymme."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Mängd diskutrymme som används av programmet."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Totalt tillgängligt diskutrymme."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                        |
| --- | --------------------- | ------------------------------------------------------------------ |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).   |
| 401 | Inte auktoriserad     | Ogiltig eller saknad JWT-token.                                    |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                  |
| 500 | Internt serverfel     | Oväntat serverfel.                                                 |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer DITT_TILLGÅNGSTOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:n

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:n.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:n:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}