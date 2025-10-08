---
title: Filer och lagring
second_title: Documen
type: docs
url: /sv/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Omfattande guide om hur man använder Aspose Cells Cloud för fillagring, inklusive uppladdning, nedladdning och hantering av filer. SDK-stöd för olika programmeringsspråk som Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 100
kwords: Aspose Cells, Molnlagring, REST API, Filhantering, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud erbjuder omfattande hjälpfunktioner för att arbeta med filer som laddats upp till Aspose.Cells Cloud Storage eller annan molnlagring som du väljer. För hjälp med att konfigurera tredjepartslagring, vänligen se[Aspose Hjälpämnen för molngränssnitt](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud erbjuder en rad API:er för fil-, mapp- och lagringsdrift.**

## **Hur man laddar upp en fil**

### Ladda upp fil API Information

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg|Sökväg för att ladda upp filen inklusive filnamn och filändelse (t.ex. /file.ext eller /Folder 1/file.ext). Om innehållet är flerdelat och sökvägen inte innehåller filnamnet, försöker den hämta det från filename-parametern i Content-Disposition-rubriken.|
| fil| Fil| formulärData| Fil att ladda upp|
| lagringsnamn| sträng| fråga| Lagringsnamn|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/UploadFile) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på uppladdningsfil

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>" \
-d {"File":{}}
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man laddar ner en fil**

### Ladda ner fil API Information

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Filsökväg (t.ex. '/mapp/fil.ext')|
| lagringsnamn| sträng| fråga| Lagringsnamn|
| versions-ID| sträng| fråga| Filversions-ID att ladda ner|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Ladda ner filexempel

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="13" tabName13="Request" tabName14="Response" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```bash
{
    Stream
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man tar bort en fil**

### Ta bort fil API Information

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Filsökväg (t.ex. '/mapp/fil.ext')|
| lagringsnamn| sträng| fråga| Lagringsnamn|
| versions-ID| sträng| fråga| Filversions-ID att radera|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/DeleteFile) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="15" tabName15="Request" tabName16="Response" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/book12.xlsx" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="16" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man kopierar en fil**

### Kopiera fil API Information

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| srcPath| sträng| väg| Sökväg till källfil (t.ex. '/mapp/fil.ext')|
|destPath| sträng| fråga| Sökväg till målfilen|
| srcLagringsnamn| sträng| fråga| Källlagringsnamn|
| destStorageName| sträng| fråga| Namn på destinationslagring|
| versions-ID| sträng| fråga| Filversions-ID att kopiera|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/CopyFile) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på kopieringsfil

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="17" tabName17="Request" tabName18="Response" >}}

{{< tab tabNum="17" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="18" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man flyttar en fil**

### Flytta fil API Information

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| srcPath| sträng| väg| Sökväg till källfil (t.ex. '/src.ext')|
|destPath| sträng| fråga| Sökväg till målfil (t.ex. '/dest.ext')|
| srcLagringsnamn| sträng| fråga| Källlagringsnamn|
| destStorageName| sträng| fråga| Namn på destinationslagring|
| versions-ID| sträng| fråga| Filversions-ID som ska flyttas|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/File/MoveFile) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Flytta fil exempel

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man skapar en mapp**

### Skapa mapp API Information

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg|Mappsökväg att skapa (t.ex. 'mapp_1/mapp_2/') |
| lagringsnamn| sträng| fråga| Lagringsnamn|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på skapa mapp

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="3" tabName3="Request" tabName4="Response" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
-X PUT \
-H "accept: application/json" \
-H "Content-Type: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```bash
{
  "Uploaded": [
    "string"
  ],
  "Errors": [
    {
      "Code": "string",
      "Message": "string",
      "Description": "string",
      "InnerError": {
        "RequestId": "string",
        "Date": "2021-12-02T03:21:11.704Z"
      }
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man får filer i en mapp**

### Hämta filer API Information

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Mappsökväg (t.ex. '/mapp')|
| lagringsnamn| sträng| fråga| Lagringsnamn|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Hämta filer exempel

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="5" tabName5="Request" tabName6="Response" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 0,
      "Path": "string"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man tar bort en mapp**

### Ta bort mapp API Information

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Mappsökväg (t.ex. '/mapp')|
| lagringsnamn| sträng| fråga| Lagringsnamn|
| rekursiv| boolesk| fråga|Falsk|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på radering av mapp

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="7" tabName7="Request" tabName8="Response" >}}

{{< tab tabNum="7" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="8" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man kopierar en mapp**

### Kopieringsmapp API Information

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| srcPath| sträng| väg| Sökväg till källmappen (t.ex. '/src')|
|destPath| sträng| fråga| Sökväg till målmapp (t.ex. '/dst')|
| srcLagringsnamn| sträng| fråga| Källlagringsnamn|
| destStorageName| sträng| fråga| Namn på destinationslagring|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på kopieringsmapp

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="21" tabName21="Request" tabName22="Response" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="22" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man flyttar en mapp**

### Flytta mapp API Information

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| srcPath| sträng| väg| Mappsökväg att flytta (t.ex. '/mapp')|
|destPath| sträng| fråga| Sökväg till målmapp att flytta till (t.ex. '/dst')|
| srcLagringsnamn| sträng| fråga| Källlagringsnamn|
| destStorageName| sträng| fråga| Namn på destinationslagring|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på att flytta mapp

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="23" tabName23="Request" tabName24="Response" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="24" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man kontrollerar om det finns lagringsutrymme**

### Lagring finns API Information

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| lagringsnamn| sträng| väg| Lagringsnamn|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på lagring finns

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="33" tabName33="Request" tabName34="Response" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="34" >}}

```bash
{
  "Exists": true
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man kontrollerar om en fil eller mapp finns**

### Objektet finns API Information

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Sökväg till fil eller mapp (t.ex. '/file.ext' eller '/mapp')|
| lagringsnamn| sträng| fråga| Lagringsnamn|
| versions-ID| sträng| fråga| Filversions-ID|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Exempel på objekt finns

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="37" tabName37="Request" tabName38="Response" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="38" >}}

```bash
{
  "Exists": true,
  "IsFolder": false
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man får reda på diskanvändning**

### Hämta information om diskanvändning API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| lagringsnamn| sträng| fråga| Lagringsnamn|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Hämta exempel på diskanvändning

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="40" tabName40="Request" tabName41="Response" >}}

{{< tab tabNum="40" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="41" >}}

```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
```

{{< /tab >}}
{{< /tabs >}}

## **Hur man hämtar filversioner**

### Hämta information om filversioner API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

Begäranparametrarna är:

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-kropp|Beskrivning|
|:- |:- |:- |:- |
| väg| sträng| väg| Filsökväg (t.ex. '/file.ext')|
| lagringsnamn| sträng| fråga| Lagringsnamn|

 De[OpenAPI-specifikation](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definierar ett offentligt tillgängligt programmeringsgränssnitt som möjliggör REST-interaktioner direkt från en webbläsare.

### Hämta exempel på filversioner

Du kan använda kommandoradsverktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man ringer till molnet API med cURL.

{{< tabs tabTotal="2" tabID="46" tabName46="Request" tabName47="Response" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/storage/cellsstorage/exist" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabnum="47" >}}

```bash
{
  "Value": [
    {
      "Name": "string",
      "IsFolder": true,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 0,
      "Path": "string",
      "VersionId": "string",
      "IsLatest": true
    }
  ]
} 
```

{{< /tab >}}
{{< /tabs >}}
