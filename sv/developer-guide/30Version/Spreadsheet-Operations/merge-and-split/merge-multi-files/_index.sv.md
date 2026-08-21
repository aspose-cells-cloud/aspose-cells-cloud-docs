---
title: "Sammanfoga flera Excel-filer till en enda arbetsbok"
second_title: "Dokument"
linktitle: "Sammanfoga flera Excel-filer"
type: docs
url: /merge-multi-files-into-excel/
aliases: [/merge/multi-files/]
keywords: "Aspose.Cells Cloud, sammanfoga flera Excel-filer, REST API, kalkylarkssammanfogning, molntjänst SDK"
description: "Lär dig hur du sammanfogar flera Excel-arbetsböcker till en enda fil med Aspose.Cells Cloud REST API (v3.0). Innehåller HTTPS-slutpunkt, cURL-kommando, SDK-exempel, obligatoriska parametrar och detaljerad felhantering."
weight: 32
---

## REST API

Denna REST API sammanfogar flera Excel-filer till en enda Excel-arbetsbok.

```bash
POST https://api.aspose.cloud/v3.0/cells/merge
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.


### Begärparametrar

| Parameter_name  | Typ     | Plats     | Beskrivning                                                                                      | Obligatoriskt |
| --------------- | ------- | --------- | ------------------------------------------------------------------------------------------------ | ------------- |
| files[]         | fil     | formData  | En eller flera Excel-arbetsböcker som ska sammanfogas. Använd `file1`, `file2`, … i begäran.     | Ja            |
| format          | sträng  | query     | Önskat utdataformat (t.ex. `xlsx`).                                                              | Ja            |
| mergeToOneSheet | boolean | query     | Sätt till `true` för att kombinera alla kalkylblad till ett enda kalkylblad; standard är `false`. | Nej           |

### **Svar**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[sammanfogat filnamn]",
    "Filesize" : [filstorlek],
    "FileContent" : "[Base64-sträng]"
}
```

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                                      |
|-----|-----------------------------|------------------------------------------------------------------|
| 200 | OK                          | Sammanfogningen lyckades; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad               | Ogiltig eller saknad JWT-token.                                  |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.                |
| 500 | Internt serverfel           | Oväntat serverfel.                                               |

## Hur du använder PostMerge-API:et med SDK:er

### PostMerge API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostMerge) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/merge?format=xlsx" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file1=@file1.xlsx" \
  -F "file2=@file2.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  {
    "Filename": "file1.xlsx",
    "FileSize": 274022,
    "FileContent": "-----Base64-sträng--------"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-förvaret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example-Merge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example-Merge.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-LightCells-Merge.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "LightCellsMerge.py" >}}
{{< /tab >}}

{{< /tabs >}}

---