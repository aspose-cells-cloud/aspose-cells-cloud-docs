---
title: "Aspose.Cells Cloud API – Fil- och mapphantering (uppladdning, nedladdning, kopiering, flyttning)"
second_title: "Dokument"
ArticleTitle: "Molnfilhantering för Excel – En effektiv och säker lösning för lagring och intelligent organisering av Excel-filer"
linktitle: "Filer och lagring"
type: docs
url: /sv/files-and-storage/
aliases: [  /sv/working-with-files-and-storage-using-aspose-cells-cloud/ ]
keywords: "Aspose.Cells Cloud, fillagrings-API, ladda upp Excel-fil, ladda ned Excel-fil, kopiera fil, flytta fil, ta bort fil, mapphantering, REST API, cURL-exempel"
description: "Omfattande guide för hantering av Excel-filer och mappar i Aspose.Cells Cloud-lagring. Innehåller uppladdning, nedladdning, kopiering, flyttning, borttagning och mappåtgärder med cURL-exempel, nödvändiga parametrar och autentiseringsnoteringar."
weight: 100
---

Aspose.Cells Cloud tillhandahåller en omfattande uppsättning hjälpfunktioner för arbete med filer lagrade i Aspose.Cells Cloud-lagring eller valfri tredjepartsmolnlagring enligt ditt val. För hjälp med konfiguration av tredjepartsmolnlagring, se [Aspose Cloud UI-hjälpämnen](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud erbjuder ett utbud av API:er för fil-, mapp- och lagringsåtgärder.**

> **Obs:** Alla API-anrop måste använda **HTTPS**. Se [Autentiseringsguide](/sv/cells/authentication/) för detaljer om hur du hämtar en JWT-token.

**Förutsättningar:** För att använda dessa API:er behöver du ett giltigt Aspose Cloud-konto, en JWT-åtkomsttoken samt en konfigurerad lagringsplats (antingen Aspose Cloud-lagring eller en ansluten tredjepartsmolnlagring).

**Senast uppdaterad:** 2024-12-01

## **Hur man laddar upp en fil**

### Information om API för filuppladdning

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Följande begärandeparametrar finns:

| Parameternamn   | Typ   | Plats  | Beskrivning |
|----------------|-------|--------|-------------|
| path           | string| path   | Sökväg för uppladdning av filen, inklusive filnamn och filtillägg (t.ex. `/mapp1/Rapport.xlsx`). |
| file           | file  | formData | Filen som ska laddas upp. |
| storageName    | string| query  | Namn på lagring som ska användas. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Filen har laddats upp.                   |
| 400 | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401 | Autentisering krävs – ogiltig eller saknad JWT-token. |
| 404 | Lagringen hittades inte.                 |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/File/UploadFile) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filuppladdning

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du laddar upp en fil med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MinMapp/Rapport.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "File=@Rapport.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MinMapp/Rapport.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Maximal filstorlek för uppladdning är 100 MB. Begränsningar kan gälla.*

## **Hur man laddar ned en fil**

### Information om API för filnedladdning

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| path         | string | path   | Sökväg till filen (t.ex. `/mapp/Rapport.xlsx`). |
| storageName  | string | query  | Namn på lagring som ska användas. |
| versionId    | string | query  | Identifierare för versionen av filen som ska laddas ned (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Filen har laddats ner; binär ström returneras. |
| 400 | Felaktig begäran – ogiltiga parametrar.  |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Filen hittades inte.                     |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filnedladdning

{{< tabs tabTotal="2" tabID="13" tabName13="Begäran" tabName14="Svar" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MinMapp/Rapport.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<binär data>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Svaret innehåller filens binära ström. Spara utdata till en fil när du använder cURL (`-o filnamn.xlsx`).*

## **Hur man tar bort en fil**

### Information om API för filborttagning

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| path         | string | path   | Sökväg till filen (t.ex. `/mapp/Rapport.xlsx`). |
| storageName  | string | query  | Namn på lagring som ska användas. |
| versionId    | string | query  | Identifierare för versionen av filen som ska tas bort (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Filen har tagits bort.                   |
| 400 | Felaktig begäran – saknade eller ogiltiga parametrar. |
| 401 | Autentisering krävs – ogiltig JWT-token. |
| 404 | Filen hittades inte.                     |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/File/DeleteFile) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filborttagning

{{< tabs tabTotal="2" tabID="15" tabName15="Begäran" tabName16="Svar" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MinMapp/GammalRapport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Filborttagning är permanent; se till att ha en säkerhetskopia om det behövs.*

## **Hur man kopierar en fil**

### Information om API för filkopiering

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Följande begärandeparametrar finns:

| Parameternamn     | Typ    | Plats  | Beskrivning |
|------------------|--------|--------|-------------|
| srcPath          | string | path   | Källfilens sökväg (t.ex. `/mapp/Källfil.xlsx`). |
| destPath         | string | query  | Målfilens sökväg (t.ex. `/mapp/Målfil.xlsx`). |
| srcStorageName   | string | query  | Källlagringens namn (valfritt). |
| destStorageName  | string | query  | Mållagringens namn (valfritt). |
| versionId        | string | query  | Filversionens ID som ska kopieras (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Filen har kopierats.                     |
| 400 | Felaktig begäran – ogiltiga parametrar.  |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Källfilen hittades inte.                 |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/File/CopyFile) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filkopiering

{{< tabs tabTotal="2" tabID="17" tabName17="Begäran" tabName18="Svar" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MinMapp/Rapport.xlsx?destPath=MinMapp/RapportKopia.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Kopieringsåtgärden tar inte bort källfilen.*

## **Hur man flyttar en fil**

### Information om API för filflyttning

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Följande begärandeparametrar finns:

| Parameternamn     | Typ    | Plats  | Beskrivning |
|------------------|--------|--------|-------------|
| srcPath          | string | path   | Källfilens sökväg (t.ex. `/mapp/Källfil.xlsx`). |
| destPath         | string | query  | Målfilens sökväg (t.ex. `/mapp/Målfil.xlsx`). |
| srcStorageName   | string | query  | Källlagringens namn (valfritt). |
| destStorageName  | string | query  | Mållagringens namn (valfritt). |
| versionId        | string | query  | Filversionens ID som ska flyttas (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Filen har flyttats.                      |
| 400 | Felaktig begäran – ogiltiga parametrar.  |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Källfilen hittades inte.                 |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/File/MoveFile) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filflyttning

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MinMapp/Rapport.xlsx?destPath=MinMapp/FlyttadRapport.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
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

*Obs: Vid flyttning bevaras filens versionshistorik.*

## **Hur man skapar en mapp**

### Information om API för mappskapande

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| path         | string | path   | Sökväg till mappen som ska skapas (t.ex. `mapp1/mapp2/`). |
| storageName  | string | query  | Namn på lagring som ska användas. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Mappen har skapats.                      |
| 400 | Felaktig begäran – ogiltig sökväg eller parametrar. |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på mappskapande

{{< tabs tabTotal="2" tabID="3" tabName3="Begäran" tabName4="Svar" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/nymapp" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "nymapp"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Mappsökvägar är skiftlägeskänsliga.*

## **Hur man hämtar filer i en mapp**

### Information om API för filhämtning

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| path         | string | path   | Mappsökväg (t.ex. `/mapp`). |
| storageName  | string | query  | Namn på lagring som ska användas. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Lista med filer och undermappar returneras. |
| 400 | Felaktig begäran – ogiltig sökväg.       |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Mappen hittades inte.                    |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filhämtning

{{< tabs tabTotal="2" tabID="5" tabName5="Begäran" tabName6="Svar" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/malMapp" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Rapport.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/malMapp/Rapport.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Svaret innehåller både filer och undermappar i den angivna sökvägen.*

## **Hur man tar bort en mapp**

### Information om API för mappborttagning

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ     | Plats  | Beskrivning |
|--------------|---------|--------|-------------|
| path         | string  | path   | Mappsökväg (t.ex. `/mapp`). |
| storageName  | string  | query  | Namn på lagring som ska användas. |
| recursive    | boolean | query  | Sätt till `true` för att ta bort mappen rekursivt. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Mappen har tagits bort.                  |
| 400 | Felaktig begäran – ogiltiga parametrar.  |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Mappen hittades inte.                    |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på mappborttagning

{{< tabs tabTotal="2" tabID="7" tabName7="Begäran" tabName8="Svar" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/malMapp" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Om du tar bort en mapp med `recursive=true` tas allt innehåll bort permanent.*

## **Hur man kopierar en mapp**

### Information om API för mappkopiering

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Följande begärandeparametrar finns:

| Parameternamn     | Typ    | Plats  | Beskrivning |
|------------------|--------|--------|-------------|
| srcPath          | string | path   | Källmappens sökväg (t.ex. `/käll`). |
| destPath         | string | query  | Målmappens sökväg (t.ex. `/mål`). |
| srcStorageName   | string | query  | Källlagringens namn (valfritt). |
| destStorageName  | string | query  | Mållagringens namn (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Mappen har kopierats.                    |
| 400 | Felaktig begäran – ogiltiga parametrar.  |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Källmappen hittades inte.                |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på mappkopiering

{{< tabs tabTotal="2" tabID="21" tabName21="Begäran" tabName22="Svar" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/kallmapp?destPath=malmapp" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Kopieringsåtgärden skapar en ny mapp med samma innehåll som källmappen.*

## **Hur man flyttar en mapp**

### Information om API för mappflyttning

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Följande begärandeparametrar finns:

| Parameternamn     | Typ    | Plats  | Beskrivning |
|------------------|--------|--------|-------------|
| srcPath          | string | path   | Källmappens sökväg (t.ex. `/mapp`). |
| destPath         | string | query  | Målmappens sökväg (t.ex. `/mål`). |
| srcStorageName   | string | query  | Källlagringens namn (valfritt). |
| destStorageName  | string | query  | Mållagringens namn (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Mappen har flyttats.                     |
| 400 | Felaktig begäran – ogiltiga parametrar.  |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Källmappen hittades inte.                |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på mappflyttning

{{< tabs tabTotal="2" tabID="23" tabName23="Begäran" tabName24="Svar" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/malmapp?destPath=doelmapp" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="24" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

*Obs: Vid mappflyttning bevaras mappens interna struktur och filversioner.*

## **Hur man kontrollerar om en lagring finns**

### Information om API för lagringsexistenskontroll

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| storageName  | string | path   | Namn på lagringen som ska kontrolleras. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Lagringens existens returneras (`true` eller `false`). |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Lagringen hittades inte.                 |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på lagringsexistenskontroll

{{< tabs tabTotal="2" tabID="33" tabName33="Begäran" tabName34="Svar" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MinLagring/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man kontrollerar om en fil eller mapp finns**

### Information om API för objektexistenskontroll

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| path         | string | path   | Sökväg till fil eller mapp (t.ex. `/fil.xlsx` eller `/mapp`). |
| storageName  | string | query  | Namn på lagring som ska kontrolleras. |
| versionId    | string | query  | Filversionsidentifierare (valfritt). |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Information om existens returneras.      |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Fil eller mapp hittades inte.            |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på objektexistenskontroll

{{< tabs tabTotal="2" tabID="37" tabName37="Begäran" tabName38="Svar" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```json
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man får användningsinformation för diskutrymme**

### Information om API för diskanvändning

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| storageName  | string | query  | Namn på lagring som ska frågas. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Information om diskutrymme returneras.   |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på diskanvändning

{{< tabs tabTotal="2" tabID="40" tabName40="Begäran" tabName41="Svar" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MinLagring" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 987654321
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man får filversioner**

### Information om API för filversioner

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Följande begärandeparametrar finns:

| Parameternamn | Typ    | Plats  | Beskrivning |
|--------------|--------|--------|-------------|
| path         | string | path   | Sökväg till filen (t.ex. `/fil.xlsx`). |
| storageName  | string | query  | Namn på lagring som ska frågas. |

**HTTP-svarskoder**

| Kod | Beskrivning                              |
|-----|------------------------------------------|
| 200 | Lista med filversioner returneras.       |
| 401 | Autentisering krävs – saknad eller ogiltig JWT-token. |
| 404 | Filen hittades inte.                     |
| 500 | Internt serverfel.                       |

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på filversioner

{{< tabs tabTotal="2" tabID="46" tabName46="Begäran" tabName47="Svar" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Rapport.xlsx?storageName=MinLagring" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt-token>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Rapport.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Rapport.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}
---