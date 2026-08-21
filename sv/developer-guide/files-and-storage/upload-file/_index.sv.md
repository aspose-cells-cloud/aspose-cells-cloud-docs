---
title: "Aspose.Cells Cloud-filuppladdnings-API – ett gränssnitt för snabb uppladdning av filer i molnet"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud-filuppladdnings-API – ett gränssnitt för snabb uppladdning av filer i molnet"
linktype: "Upload File"
type: docs
url: /sv/upload-file/
keywords: "Aspose.Cells, filuppladdning, Excel-API, molnlagring, REST-API"
description: "Guide för filuppladdning med Aspose.Cells Cloud-API, inklusive begärparametrar, HTTP-statuskoder, felhantering och kodexempel."
weight: 100
---

**uploadFile**-API:t gör det möjligt för utvecklare att ladda upp filer direkt till molnlagring för bearbetning med Aspose Cells.

## **Aspose Cells API: Filuppladdning**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Begärparametrarna för **uploadFile**-API:t är

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-kropp | Beskrivning                                                                                   |
| :------------ | :---- | :---------------------------- | :-------------------------------------------------------------------------------------------- |
| UploadFiles   | Fil   | FormData                      | Ladda upp filer till molnlagring.                                                             |
| path          | Sträng | Sökväg                        | Målsökvägen i molnlagringen. Ange den sökväg där filen ska laddas upp.                       |
| storageName   | Sträng | Frågesträng                   | Namnet på den lagring där filen ska laddas upp.                                               |

### **Svar**

```json
{
  "Name": "FilesUploadResult",
  "Description": ["Resultat för filuppladdning"],
  "Type": "Klass",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Uploaded",
      "Description": ["Lista över uppladdade filnamn"],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "String",
        "ElementDataType": {
          "Identifier": "String",
          "Name": "string"
        },
        "Name": "container"
      }
    },
    {
      "Name": "Errors",
      "Description": ["Lista över fel."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Container",
        "Reference": "Error",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "Error",
          "Name": "class:error"
        },
        "Name": "container"
      }
    }
  ]
}
```

API:et returnerar följande HTTP-statuskoder:

| Statuskod                     | Beskrivning                                           |
| ----------------------------- | ----------------------------------------------------- |
| **200 OK**                    | Filen har laddats upp utan problem.                   |
| **400 Bad Request**           | Ogiltiga parametrar eller felaktigt formaterad förfrågan. |
| **401 Unauthorized**          | Saknar eller har ogiltig autentiseringstoken.         |
| **403 Forbidden**             | Otillräckliga rättigheter för den angivna lagringen.  |
| **500 Internal Server Error** | Oväntat serverfel.                                    |

## Hur använder man filuppladdnings-API:t med SDK:er?

### OpenAPI-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/FileController/UploadFile) innehåller en detaljerad beskrivning av API:t och gör det möjligt för utvecklare att interagera med det direkt via en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud-API:t med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/Folder/Book1.xlsx" \
  -H "Authorization: Bearer {access_token}" \
  -F "UploadFiles=@/path/to/Book1.xlsx" \
  -F "path=Folder/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Uploaded": ["Book1.xlsx"],
  "Errors": []
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK förbättrar utvecklingseffektiviteten genom att hantera detaljer på låg nivå, så att utvecklare kan fokusera på projektuppgifter. Besök [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur Aspose.Cells webbtjänster anropas med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UploadFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UploadFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UploadFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UploadFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UploadFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UploadFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UploadFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UploadFile.go" >}}
{{</tab>}}
{{< /tabs >}}

**Se även**

- [Filnedladdnings-API](/download-file/) – Hämta en fil från molnlagring.
- [Kopiera fil-API](/copy-file/) – duplicera en fil inom molnlagring.
- [Ta bort fil-API](/delete-file/) – ta bort en fil från molnlagring.