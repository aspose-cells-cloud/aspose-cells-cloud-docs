---
title: "Aspose.Cells Cloud-mappkopierings-API – Snabb kopiering av mappar i molnet"
second_title: "Dokument"
ArticleTitle: "Molnbaserad Excel-filhanteringslösning – Detaljerad förklaring av Aspose.Cells Copy Folder API:s batchkopieringsfunktion"
linktitle: "Kopiera mapp"
type: docs
url: /copy-folder/
keywords: "Kopiera mapp, Aspose.Cells Cloud, REST API, Molnlagring, Kalkylarkshantering"
description: "Lär dig hur du kopierar mappar i Aspose.Cells Cloud-lagring med ett enda REST-anrop. Inkluderar slutpunkt, parametrar, exempel på förfrågningar, felkoder och SDK-exempel."
weight: 100
---

**CopyFolder**-API:et duplicerar en befintlig mapp i Aspose.Cells Cloud-lagring. Detta är användbart för att skapa säkerhetskopior, omorganisera data eller förbereda en mappstruktur för vidare bearbetning utan manuella filflyttningar.

## **Excel-API: Kopiera mapp**

### Web-API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### CopyFolder API:et tar emot följande parametrar

| Parameter namn    | Krävs  | Typ    | Plats (Sökväg/Fråga) | Beskrivning                                                           |
| ----------------- | ------ | ------ | -------------------- | --------------------------------------------------------------------- |
| `srcPath`         | Ja     | Sträng | Sökväg               | Sökvägen till källmappen som ska kopieras.                           |
| `destPath`        | Ja     | Sträng | Fråga                | Sökvägen dit den nya mappen ska skapas.                               |
| `srcStorageName`  | Nej    | Sträng | Fråga                | Namnet på lagringen som innehåller källmappen.                       |
| `destStorageName` | Nej    | Sträng | Fråga                | Namnet på mållagringen dit mappen ska kopieras.                      |

### Exempel på svar

Ett lyckat anrop returnerar **HTTP 200** med en tom JSON-kropp:

```json
{}
```

**Exempel på cURL-förfrågan**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filtrering lyckades; svaret innehåller åtgärdens detaljer.       |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401 | Oauktoriserad         | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

Att använda ett SDK är det bästa sättet att snabba upp utvecklingen. Ett SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}