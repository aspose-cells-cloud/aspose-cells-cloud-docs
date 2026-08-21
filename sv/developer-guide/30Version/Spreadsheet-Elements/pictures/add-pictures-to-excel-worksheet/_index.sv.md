---
title: "Lägg till en bild i en Excel-fil"
second_title: "Dokument"
linktitle: "Lägg till"
type: docs
url: /sv/pictures/add/
aliases: [/sv/add-pictures-to-excel-worksheet/]
keywords: "Aspose.Cells, Excel, lägg till bild, REST API"
description: "Använd Aspose.Cells Cloud REST API för att lägga till en bild i ett Excel-arbetsblad. SDK:er för Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift förenklar integration över plattformar."
weight: 20
ArticleTitle: "Lägg till en bild i ett Excel-arbetsblad – Aspose.Cells Cloud API"
---

Denna REST API lägger till en ny bild i ett Excel-arbetsblad.  
**Förutsättningar:** Du måste ha en giltig Aspose Cloud-autentiseringstoken, en befintlig arbetsbok lagrad i ett stödjt lagringssystem samt tillräckliga behörigheter för att ändra arbetsbladet.

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärandeparametrar

| Parameternamn    | Typ     | Plats  | Beskrivning                                                                                   |
| ---------------- | ------- | ------ | --------------------------------------------------------------------------------------------- |
| name             | string  | path   | Namnet på arbetsboken.                                                                        |
| sheetName        | string  | path   | Namnet på arbetsbladet.                                                                       |
| picture          | object  | body   | Bildobjekt (binär data).                                                                      |
| upperLeftRow     | integer | query  | Nollbaserat index för den övre vänstra raden där bilden ska placeras.                         |
| upperLeftColumn  | integer | query  | Nollbaserat index för den övre vänstra kolumnen där bilden ska placeras.                      |
| lowerRightRow    | integer | query  | Nollbaserat index för den nedre högra raden i bildområdet.                                    |
| lowerRightColumn | integer | query  | Nollbaserat index för den nedre högra kolumnen i bildområdet.                                 |
| picturePath      | string  | query  | Sökvägen till bildfilen; om utelämnad måste bilddatat skickas i begärandetexten.             |
| folder           | string  | query  | Mappen som innehåller arbetsboken.                                                            |
| storageName      | string  | query  | Namnet på lagringstjänsten.                                                                   |

**OBS! Begärandetext:** När `picturePath` utelämnas, skicka den binära bilddata i begärandetexten med `multipart/form-data`.

### HTTP-statuskoder

| Kod | Beteende                    | Beskrivning                                              |
|-----|-----------------------------|----------------------------------------------------------|
| 200 | OK                          | Filter applicerades framgångsrikt; svaren innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad           | Ogiltig eller saknad JWT-token.                          |
| 413 | För stor nyttolast          | Den uppladdade filen överskrider storleksgränsen.        |
| 500 | Internt serverfel           | Oväntat serverfel.                                       |

**Exempel 200-svarschema**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**OBS!** Den maximala bildstorleken är 10 MB; större filer kommer att avvisas med ett `400 Bad Request`-svar.

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## SDK-familj för molnet

Att använda en SDK är det bästa sättet att snabba upp utvecklingen. En SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Se [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells-webbtjänster med hjälp av olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**OBS!** Stödda bildformat inkluderar PNG, JPEG, BMP och GIF. Den maximala bildstorleken är 10 MB; större filer kommer att avvisas med ett `400 Bad Request`-svar.