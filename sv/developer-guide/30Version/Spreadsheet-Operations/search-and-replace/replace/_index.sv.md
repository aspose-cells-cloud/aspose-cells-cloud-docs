---
title: "Ersätt text i Excel-filer"
second_title: "Dokument"
linktitle: "Ersätt utan att använda lagring"
type: docs
url: /sv/replace/
keywords: "Excel ersätt text, Aspose.Cells Cloud, REST API, kalkylblad ersättning, API, Excel-filtextersättning"
description: "Använd Aspose.Cells Cloud REST API för att ersätta befintlig text med nya värden i Excel-filer. Stöder SDK:er för C#, Java, Python, Node.js, PHP, Ruby, Go och Perl."
weight: 80
---


## REST API

Detta REST API ersätter data i Excel-filer.

```bash
POST https://api.aspose.cloud/v3.0/cells/replace
```

### Säkerhet och autentisering

Aspose.Cells Cloud API:er är säkra och kräver [JWT-tokenbaserad autentisering](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).


### Begäranparameter

| Parameternamn | Typ   | Plats                | Beskrivning                                        |
| ------------- | ----- | -------------------- | -------------------------------------------------- |
| **file**      | fil   | formData (multipart) | Excel-fil som ska bearbetas.                      |
| **text**      | sträng | fråga                | Textsträng som ska ersättas.                       |
| **newtext**   | sträng | fråga                | Ersättningstext.                                   |
| **password**  | sträng | fråga                | Lösenord för ett skyddat kalkylbladsark (valfritt). |
| **sheetname** | sträng | fråga                | Namn på det kalkylblad som ska målras (valfritt).  |

### **Svar**

```json
{
  "Status":"OK",
  "Code":200,
  "Files": [
    {
      "Filename" : "[fil1-namn]",
      "Filesize" : [filstorlek],
      "FileContent" : "[Base64-sträng]"
    },
    {
      "Filename" : "[fil2-namn]",
      "Filesize" : [filstorlek],
      "FileContent" : "[Base64-sträng]"
    },
    {
      "Filename" : "[fil3-namn]",
      "Filesize" : [filstorlek],
      "FileContent" : "[Base64-sträng]"
    }
  ]
}
```

**HTTP-statuskoder**

| Kod | Betydelse                 | Beskrivning                                             |
|-----|---------------------------|---------------------------------------------------------|
| 200 | OK                        | Ersättning lyckades; svaret innehåller åtgärdsdetaljer. |
| 400 | Felaktig begäran          | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktorisering saknas      | Ogiltig eller saknad JWT-token.                         |
| 413 | För stor nyttolast        | Den uppladdade filen överskrider storleksgränsen.       |
| 500 | Internt serverfel         | Oväntat serverfel.                                      |

## Hur du använder PostReplace API med SDK:er

### PostReplace API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/LightCells/PostReplace) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/replace?text=1&newtext=aspose.cells.cloud" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxx1",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    },
    {
      "Filename": "xxxx2",
      "FileSize": 274022,
      "FileContent": "-----Base64-sträng--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Moln SDK-familj

Att använda en SDK är det bästa sättet att påskynda utvecklingen. En SDK hanterar detaljer på lågnivå och låter dig fokusera på dina projektuppgifter. Se [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostReplace.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostReplace.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostReplace.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostReplace.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostReplace.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostReplace.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostReplace.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostReplace.go" >}}

{{< /tab >}}

{{< /tabs >}}

---