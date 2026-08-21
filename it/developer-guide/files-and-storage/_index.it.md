---
title: "Aspose.Cells Cloud API – Gestione di file e cartelle (Caricamento, Scaricamento, Copia, Spostamento)"
second_title: "Documento"
ArticleTitle: "Gestione cloud dei file per Excel – Una soluzione efficiente e sicura per l’archiviazione e l’organizzazione intelligente dei file Excel"
linktype: "docs"
url: /it/files-and-storage/
aliases: [  /it/working-with-files-and-storage-using-aspose-cells-cloud/ ]
keywords: "Aspose.Cells Cloud, API per l’archiviazione file, caricamento file Excel, scaricamento file Excel, copia file, spostamento file, eliminazione file, gestione cartelle, API REST, esempi cURL"
description: "Guida completa alla gestione di file Excel e cartelle nello storage di Aspose.Cells Cloud. Include operazioni di caricamento, scaricamento, copia, spostamento, eliminazione e gestione delle cartelle, con esempi in cURL, parametri obbligatori e note sull’autenticazione."
weight: 100
---

Aspose.Cells Cloud fornisce un insieme completo di funzioni di supporto per la gestione dei file archiviati nello storage di Aspose.Cells Cloud o in qualsiasi servizio di archiviazione cloud di terze parti a tua scelta. Per assistenza nella configurazione di uno storage di terze parti, consulta gli [Argomenti della Guida dell’interfaccia utente di Aspose Cloud](https://docs.aspose.cloud/display/totalcloud/Aspose+Cloud+UI+Help+Topics).

**Aspose.Cells Cloud offre una serie di API per operazioni su file, cartelle e storage.**

> **Nota:** Tutte le chiamate API devono utilizzare **HTTPS**. Per maggiori dettagli su come ottenere un token JWT, consulta la [Guida all’autenticazione](/it/authentication/).

**Prerequisiti:** Per utilizzare queste API devi disporre di un account Aspose Cloud valido, aver ottenuto un token di accesso JWT e aver configurato una posizione di storage (sia lo storage di Aspose Cloud che uno storage di terze parti connesso).

**Ultimo aggiornamento:** 2024-12-01

## **Come caricare un file**

### Informazioni sull’API per il caricamento di file

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso di destinazione per il file da caricare, incluso nome e estensione (es. `/cartella1/Report.xlsx`). |
| file           | file   | formData  | File da caricare. |
| storageName    | string | query     | Nome dello storage da utilizzare. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | File caricato correttamente.              |
| 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401    | Non autorizzato – token JWT non valido o mancante. |
| 404    | Storage non trovato.                      |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/File/UploadFile) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di caricamento file

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come caricare un file con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}
{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F "File=@Report.xlsx"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```json
{
  "Uploaded": [
    "MyFolder/Report.xlsx"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La dimensione massima del file caricabile è di 100 MB. Possono essere applicati limiti di frequenza.*

## **Come scaricare un file**

### Informazioni sull’API per lo scaricamento di file

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso del file (es. `/cartella/Report.xlsx`). |
| storageName    | string | query     | Nome dello storage da utilizzare. |
| versionId      | string | query     | Identificatore della versione del file da scaricare (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | File scaricato; viene restituito uno stream binario. |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | File non trovato.                         |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/File/DownloadFile) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di scaricamento file

{{< tabs tabTotal="2" tabID="13" tabName13="Richiesta" tabName14="Risposta" >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/Report.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="14" >}}

```json
{
  "Stream": "<dati binari>"
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La risposta contiene lo stream binario del file. Quando utilizzi cURL, salva l’output in un file (`-o filename.xlsx`).*

## **Come eliminare un file**

### Informazioni sull’API per l’eliminazione di file

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/file/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso del file (es. `/cartella/Report.xlsx`). |
| storageName    | string | query     | Nome dello storage da utilizzare. |
| versionId      | string | query     | Identificatore della versione del file da eliminare (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | File eliminato correttamente.             |
| 400    | Richiesta non valida – parametri mancanti o non validi. |
| 401    | Non autorizzato – token JWT non valido.   |
| 404    | File non trovato.                         |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/File/DeleteFile) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di eliminazione file

{{< tabs tabTotal="2" tabID="15" tabName15="Richiesta" tabName16="Risposta" >}}
{{< tab tabNum="15" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/MyFolder/OldReport.xlsx" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

*Nota: L’eliminazione di un file è irreversibile; assicurati di disporre di un backup qualora necessario.*

## **Come copiare un file**

### Informazioni sull’API per la copia di file

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
```

I parametri della richiesta sono i seguenti:

| Nome parametro   | Tipo   | Posizione | Descrizione |
|------------------|--------|-----------|-------------|
| srcPath          | string | path      | Percorso del file sorgente (es. `/cartella/Sorgente.xlsx`). |
| destPath         | string | query     | Percorso di destinazione del file (es. `/cartella/Destinazione.xlsx`). |
| srcStorageName   | string | query     | Nome dello storage sorgente (opzionale). |
| destStorageName  | string | query     | Nome dello storage di destinazione (opzionale). |
| versionId        | string | query     | ID della versione del file da copiare (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | File copiato correttamente.               |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | File sorgente non trovato.                |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/File/CopyFile) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di copia file

{{< tabs tabTotal="2" tabID="17" tabName17="Richiesta" tabName18="Risposta" >}}
{{< tab tabNum="17" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/copy/MyFolder/Report.xlsx?destPath=MyFolder/ReportCopy.xlsx" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

*Nota: L’operazione di copia non rimuove il file sorgente.*

## **Come spostare un file**

### Informazioni sull’API per lo spostamento di file

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
```

I parametri della richiesta sono i seguenti:

| Nome parametro   | Tipo   | Posizione | Descrizione |
|------------------|--------|-----------|-------------|
| srcPath          | string | path      | Percorso del file sorgente (es. `/cartella/Sorgente.xlsx`). |
| destPath         | string | query     | Percorso di destinazione del file (es. `/cartella/Destinazione.xlsx`). |
| srcStorageName   | string | query     | Nome dello storage sorgente (opzionale). |
| destStorageName  | string | query     | Nome dello storage di destinazione (opzionale). |
| versionId        | string | query     | ID della versione del file da spostare (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | File spostato correttamente.              |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | File sorgente non trovato.                |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/File/MoveFile) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di spostamento file

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}
{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/file/move/MyFolder/Report.xlsx?destPath=MyFolder/ReportMoved.xlsx" \
  -X PUT \
  -H "accept: application/json" \
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

*Nota: Lo spostamento di un file conserva la cronologia delle versioni del file.*

## **Come creare una cartella**

### Informazioni sull’API per la creazione di cartelle

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso della cartella da creare (es. `cartella1/cartella2/`). |
| storageName    | string | query     | Nome dello storage da utilizzare. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Cartella creata correttamente.            |
| 400    | Richiesta non valida – percorso o parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CreateFolder) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di creazione cartella

{{< tabs tabTotal="2" tabID="3" tabName3="Richiesta" tabName4="Risposta" >}}
{{< tab tabNum="3" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/newfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="4" >}}

```json
{
  "Uploaded": [
    "newfolder"
  ],
  "Errors": []
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: I percorsi delle cartelle sono sensibili alle maiuscole.*

## **Come ottenere l’elenco dei file in una cartella**

### Informazioni sull’API per l’elenco dei file

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso della cartella (es. `/cartella`). |
| storageName    | string | query     | Nome dello storage da utilizzare. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Elenco di file e sottocartelle restituito. |
| 400    | Richiesta non valida – percorso non valido. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | Cartella non trovata.                     |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/GetFilesList) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di elenco dei file

{{< tabs tabTotal="2" tabID="5" tabName5="Richiesta" tabName6="Risposta" >}}
{{< tab tabNum="5" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="6" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T12:38:45.739Z",
      "Size": 102400,
      "Path": "/desfolder/Report.xlsx"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

*Nota: La risposta elenca sia i file che le sottocartelle presenti nel percorso specificato.*

## **Come eliminare una cartella**

### Informazioni sull’API per l’eliminazione di cartelle

```bash
DELETE https://api.aspose.cloud/v3.0/cells/storage/folder/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo    | Posizione | Descrizione |
|----------------|---------|-----------|-------------|
| path           | string  | path      | Percorso della cartella (es. `/cartella`). |
| storageName    | string  | query     | Nome dello storage da utilizzare. |
| recursive      | boolean | query     | Impostare su `true` per eliminare la cartella in modo ricorsivo. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Cartella eliminata correttamente.         |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | Cartella non trovata.                     |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di eliminazione cartella

{{< tabs tabTotal="2" tabID="7" tabName7="Richiesta" tabName8="Risposta" >}}
{{< tab tabNum="7" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
  -X DELETE \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

*Nota: L’eliminazione di una cartella con `recursive=true` rimuove permanentemente tutto il suo contenuto.*

## **Come copiare una cartella**

### Informazioni sull’API per la copia di cartelle

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
```

I parametri della richiesta sono i seguenti:

| Nome parametro   | Tipo   | Posizione | Descrizione |
|------------------|--------|-----------|-------------|
| srcPath          | string | path      | Percorso della cartella sorgente (es. `/src`). |
| destPath         | string | query     | Percorso della cartella di destinazione (es. `/dst`). |
| srcStorageName   | string | query     | Nome dello storage sorgente (opzionale). |
| destStorageName  | string | query     | Nome dello storage di destinazione (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Cartella copiata correttamente.           |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | Cartella sorgente non trovata.            |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di copia cartella

{{< tabs tabTotal="2" tabID="21" tabName21="Richiesta" tabName22="Risposta" >}}
{{< tab tabNum="21" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

*Nota: L’operazione di copia crea una nuova cartella con lo stesso contenuto della sorgente.*

## **Come spostare una cartella**

### Informazioni sull’API per lo spostamento di cartelle

```bash
PUT https://api.aspose.cloud/v3.0/cells/storage/folder/move/{srcPath}
```

I parametri della richiesta sono i seguenti:

| Nome parametro   | Tipo   | Posizione | Descrizione |
|------------------|--------|-----------|-------------|
| srcPath          | string | path      | Percorso della cartella sorgente (es. `/cartella`). |
| destPath         | string | query     | Percorso della cartella di destinazione (es. `/dst`). |
| srcStorageName   | string | query     | Nome dello storage sorgente (opzionale). |
| destStorageName  | string | query     | Nome dello storage di destinazione (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Cartella spostata correttamente.          |
| 400    | Richiesta non valida – parametri non validi. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | Cartella sorgente non trovata.            |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Folder/MoveFolder) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di spostamento cartella

{{< tabs tabTotal="2" tabID="23" tabName23="Richiesta" tabName24="Risposta" >}}
{{< tab tabNum="23" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/folder/move/desfolder?destPath=destfolder" \
  -X PUT \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

*Nota: Lo spostamento di una cartella ne conserva la struttura interna e le versioni dei file.*

## **Come verificare se lo storage esiste**

### Informazioni sull’API per la verifica dell’esistenza dello storage

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/{storageName}/exist
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| storageName    | string | path      | Nome dello storage da verificare. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Viene restituita l’esistenza dello storage (`true` o `false`). |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | Storage non trovato.                      |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/StorageExists) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di verifica dell’esistenza dello storage

{{< tabs tabTotal="2" tabID="33" tabName33="Richiesta" tabName34="Risposta" >}}
{{< tab tabNum="33" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/MyStorage/exist" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## **Come verificare se un file o una cartella esiste**

### Informazioni sull’API per la verifica dell’esistenza di oggetti

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/exist/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso del file o della cartella (es. `/file.xlsx` o `/cartella`). |
| storageName    | string | query     | Nome dello storage da verificare. |
| versionId      | string | query     | Identificatore della versione del file (opzionale). |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Vengono restituite informazioni sull’esistenza. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | File o cartella non trovato.              |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/ObjectExists) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di verifica dell’esistenza di un oggetto

{{< tabs tabTotal="2" tabID="37" tabName37="Richiesta" tabName38="Risposta" >}}
{{< tab tabNum="37" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/exist/Book1.xlsx" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## **Come ottenere l’utilizzo dello spazio disco**

### Informazioni sull’API per l’utilizzo dello spazio disco

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/disc
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| storageName    | string | query     | Nome dello storage da interrogare. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Vengono restituite informazioni sull’utilizzo dello spazio disco. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di utilizzo dello spazio disco

{{< tabs tabTotal="2" tabID="40" tabName40="Richiesta" tabName41="Risposta" >}}
{{< tab tabNum="40" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/disc?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

## **Come ottenere le versioni di un file**

### Informazioni sull’API per le versioni di un file

```bash
GET https://api.aspose.cloud/v3.0/cells/storage/version/{path}
```

I parametri della richiesta sono i seguenti:

| Nome parametro | Tipo   | Posizione | Descrizione |
|----------------|--------|-----------|-------------|
| path           | string | path      | Percorso del file (es. `/file.xlsx`). |
| storageName    | string | query     | Nome dello storage da interrogare. |

**Risposte HTTP**

| Codice | Descrizione                               |
|--------|-------------------------------------------|
| 200    | Viene restituito l’elenco delle versioni del file. |
| 401    | Non autorizzato – token JWT mancante o non valido. |
| 404    | File non trovato.                         |
| 500    | Errore interno del server.                |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Storage/GetFileVersions) definisce un’interfaccia di programmazione pubblicamente accessibile, che consente interazioni REST direttamente da un browser web.

### Esempio di versioni di un file

{{< tabs tabTotal="2" tabID="46" tabName46="Richiesta" tabName47="Risposta" >}}
{{< tab tabNum="46" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/storage/version/Report.xlsx?storageName=MyStorage" \
  -X GET \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="47" >}}

```json
{
  "Value": [
    {
      "Name": "Report.xlsx",
      "IsFolder": false,
      "ModifiedDate": "2021-12-08T18:57:46.128Z",
      "Size": 102400,
      "Path": "/Report.xlsx",
      "VersionId": "1",
      "IsLatest": true
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}