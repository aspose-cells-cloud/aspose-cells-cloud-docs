---
title: "Skapa mapp – Aspose.Cells Cloud API | Excel-lagerhantering"
second_title: "Dokument"
ArticleTitle: "Skapa mapp – Aspose.Cells Cloud API"
linktype: "Skapa mapp"
type: docs
url: /sv/create-folder/
keywords: "Aspose.Cells, Cloud API, Skapa mapp, Lagerhantering, Excel"
description: "Skapa en ny mapp i Aspose.Cells Cloud-lagring via en enkel PUT-begäran. Se begärans format, parametrar, svar och felhantering."
weight: 100
---

**createFolder**-åtgärden skapar en ny mapp på den angivna platsen i lagerutrymmet som används av Excel API:et i molnet. Detta är avgörande för att organisera filer och underhålla en strukturerad kataloghierarki.

## **Excel API: Skapa mapp**

### Webb-API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärans parametrar för **createFolder**-API:et är

| Parameternamn   | Typ    | Plats  | Obligatorisk | Standard | Beskrivning                                                         |
| --------------- | ------ | ------ | ------------ | -------- | ------------------------------------------------------------------- |
| `path`          | String | Path   | Ja           | –        | Mappsökvägen som ska skapas (t.ex. `minMapp/underMapp`).           |
| `storageName`   | String | Query  | Nej          | –        | Namnet på det lagring som ska användas. Om utelämnas används standardlagring. |

### Svarsbeskrivning

```json
{}
```

Åtgärden returnerar inget innehåll vid lyckad åtgärd. Vanliga HTTP-statuskoder är:

**HTTP-statuskoder**

| HTTP-kod | HTTP-status          | Beskrivning                                                             |
| -------- | -------------------- | ----------------------------------------------------------------------- |
| 200      | OK                   | Web-API:et anropades utan problem; svaret innehåller åtgärdens detaljer. |
| 400      | Bad Request          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).       |
| 401      | Unauthorized         | Ogiltig eller saknad JWT-token.                                        |
| 413      | Payload Too Large    | Den uppladdade filen överskrider storleksgränsen.                      |
| 500      | Internal Server Error| Oväntat serverfel.                                                     |

## OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FolderController/CreateFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL kommandoradsverktyget för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/minMapp/underMapp" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateFolder.go" >}}
{{</tab>}}
{{< /tabs >}}