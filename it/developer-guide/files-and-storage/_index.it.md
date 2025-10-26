---
title: File e archiviazione
second_title: Documen
type: docs
url: /it/files-and-storage/
aliases: [/working-with-files-and-storage-using-aspose-cells-cloud/]
keywords: Aspose Cells Cloud file storage, upload, download, delete, move, copy file
description: Guida completa all'utilizzo di Aspose Cells Cloud per operazioni di archiviazione file, inclusi caricamento, download e gestione dei file. Supporto SDK per vari linguaggi di programmazione come Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e Swift.
weight: 100
kwords: Aspose Cells, Archiviazione cloud, REST API, Gestione file, Excel, PDF, CSV, JSON, Markdow
---
 Aspose.Cells Cloud offre funzioni di supporto complete per lavorare con i file caricati su Aspose.Cells Cloud Storage o su qualsiasi altro cloud storage di tua scelta. Per assistenza nella configurazione di un archivio di terze parti, consulta[Aspose Argomenti della guida dell'interfaccia utente cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud offre una gamma di API per la gestione di file, cartelle e archivi.**

## **Come caricare un file**

### Carica file API Informazioni

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero|Percorso per caricare il file, inclusi nome ed estensione (ad esempio, /file.ext o /Cartella 1/file.ext). Se il contenuto è multiparte e il percorso non contiene il nome del file, il programma tenta di recuperarlo dal parametro filename nell'intestazione Content-Disposition.|
| file| File| formData| File da caricare|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di caricamento file

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come scaricare un file**

### Scarica il file API Informazioni

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso del file (ad esempio, '/cartella/file.ext')|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|
| ID versione| corda| domanda| ID versione file da scaricare|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Scarica file di esempio

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come eliminare un file**

### Elimina file API Informazioni

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso del file (ad esempio, '/cartella/file.ext')|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|
| ID versione| corda| domanda| ID versione file da eliminare|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come copiare un file**

### Copia file API Informazioni

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| Percorso src| corda| sentiero| Percorso del file sorgente (ad esempio, '/cartella/file.ext')|
|Percorso di destinazione| corda| domanda| Percorso del file di destinazione|
| NomeArchiviazioneSorgente| corda| domanda| Nome dell'archivio di origine|
| NomeArchiviazioneDest| corda| domanda| Nome dell'archiviazione di destinazione|
| ID versione| corda| domanda| ID versione file da copiare|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di copia file

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come spostare un file**

### Sposta file API Informazioni

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| Percorso src| corda| sentiero| Percorso del file sorgente (ad esempio, '/src.ext')|
|Percorso di destinazione| corda| domanda| Percorso del file di destinazione (ad esempio, '/dest.ext')|
| NomeArchiviazioneSorgente| corda| domanda| Nome dell'archivio di origine|
| NomeArchiviazioneDest| corda| domanda| Nome dell'archiviazione di destinazione|
| ID versione| corda| domanda| ID versione file da spostare|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di spostamento del file

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come creare una cartella**

### Crea cartella API Informazioni

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero|Percorso della cartella da creare (ad esempio, 'cartella_1/cartella_2/') |
| Nome di archiviazione| corda| domanda| Nome dell'archivio|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Crea esempio di cartella

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come ottenere file in una cartella**

### Ottieni informazioni sui file API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso della cartella (ad esempio, '/cartella')|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Ottieni file Esempio

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come eliminare una cartella**

### Elimina cartella API Informazioni

```bash
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso della cartella (ad esempio, '/cartella')|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|
| ricorsivo| booleano| domanda|Falso|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di eliminazione della cartella

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come copiare una cartella**

### Copia cartella API Informazioni

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| Percorso src| corda| sentiero| Percorso della cartella di origine (ad esempio, '/src')|
|Percorso di destinazione| corda| domanda| Percorso della cartella di destinazione (ad esempio, '/dst')|
| NomeArchiviazioneSorgente| corda| domanda| Nome dell'archivio di origine|
| NomeArchiviazioneDest| corda| domanda| Nome dell'archiviazione di destinazione|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di copia della cartella

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come spostare una cartella**

### Sposta cartella API Informazioni

```bash
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| Percorso src| corda| sentiero| Percorso della cartella da spostare (ad esempio, '/cartella')|
|Percorso di destinazione| corda| domanda| Percorso della cartella di destinazione in cui spostarsi (ad esempio, '/dst')|
| NomeArchiviazioneSorgente| corda| domanda| Nome dell'archivio di origine|
| NomeArchiviazioneDest| corda| domanda| Nome dell'archiviazione di destinazione|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di spostamento della cartella

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come verificare se esiste spazio di archiviazione**

### Esiste un deposito API Informazioni

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| Nome di archiviazione| corda| sentiero| Nome dell'archivio|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di archiviazione esistente

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come verificare se un file o una cartella esiste**

### L'oggetto esiste API Informazioni

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso del file o della cartella (ad esempio, '/file.ext' o '/folder')|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|
| ID versione| corda| domanda| ID versione file|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Esempio di oggetto esistente

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come ottenere l'utilizzo del disco**

### Ottieni informazioni sull'utilizzo del disco API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/disc
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| Nome di archiviazione| corda| domanda| Nome dell'archivio|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Ottieni un esempio di utilizzo del disco

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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

## **Come ottenere le versioni dei file**

### Ottieni informazioni sulle versioni dei file API

```bash
GET http://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

I parametri della richiesta sono:

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|:- |:- |:- |:- |
| sentiero| corda| sentiero| Percorso del file (ad esempio, '/file.ext')|
| Nome di archiviazione| corda| domanda| Nome dell'archivio|

 IL[Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definisce un'interfaccia di programmazione accessibile al pubblico, consentendo interazioni REST direttamente da un browser web.

### Ottieni esempio di versioni di file

È possibile utilizzare lo strumento da riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate al Cloud API con cURL.

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
