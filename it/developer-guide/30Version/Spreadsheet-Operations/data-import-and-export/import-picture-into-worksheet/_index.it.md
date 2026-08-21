---
title: "Importa immagine in un foglio di lavoro Excel"
ArticleTitle: "Importa immagine in un foglio di lavoro Excel – Guida all'API Aspose.Cells Cloud"
second_title: "Documento"
linktype: "docs"
url: /it/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "Importa immagine, Excel, Aspose.Cells Cloud, API REST, v3.0"
description: "Scopri come importare immagini nei fogli di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud v3.0. Include esempi di richieste multipart, codice di esempio per gli SDK e indicazioni sulla gestione degli errori. Inizia subito con passaggi chiari."
weight: 19
---

Importare un’immagine in un foglio di lavoro Excel consente di arricchire i fogli elettronici con contenuti visivi come loghi, grafici o diagrammi. Questa guida mostra come utilizzare l’operazione **ImportPicture** di Aspose.Cells Cloud, il formato richiesto per la richiesta e come gestire le risposte.

**Prerequisiti:** Prima di invocare l’operazione di importazione, è necessario disporre di un token di autenticazione JWT valido e di un workbook esistente memorizzato in Aspose Cloud Storage.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

La richiesta è una **POST** HTTP con contenuto **multipart/related** (vedere [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- La **prima parte** contiene un oggetto JSON denominato **ImportPictureOption** che descrive dove e come l’immagine deve essere posizionata.
- La **seconda parte** trasporta il file immagine (o i suoi dati codificati in Base64).

### ImportPictureOption – definizione

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` è un **booleano** – `true` inserisce una nuova immagine, `false` ne sostituisce una esistente._

### Parametri importanti

**ImportPictureOption**

| Nome parametro      | Tipo        | Descrizione                                                                                                                                                                                                 |
| ------------------- | ----------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UpperLeftRow        | int         | Indice di riga dell’angolo in alto a sinistra in cui l’immagine verrà posizionata.                                                                                                                         |
| UpperLeftColumn     | int         | Indice di colonna dell’angolo in alto a sinistra in cui l’immagine verrà posizionata.                                                                                                                      |
| LowerRightRow       | int         | Indice di riga dell’angolo in basso a destra che definisce i limiti dell’immagine.                                                                                                                         |
| LowerRightColumn    | int         | Indice di colonna dell’angolo in basso a destra che definisce i limiti dell’immagine.                                                                                                                      |
| Filename            | string      | Nome del file immagine.                                                                                                                    |
| Data                | string      | Dati binari dell’immagine codificati in Base64 (opzionale se il file viene inviato come seconda parte).                                                                                                   |
| DestinationWorksheet| string      | Nome del foglio di lavoro in cui l’immagine verrà inserita.                                                                                |
| **IsInsert**        | **boolean** | `true` per inserire una nuova immagine; `false` per sostituire un’immagine esistente.                                                                                                                     |
| ImportDataType      | string      | Tipo di dati da importare (ad esempio, `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`).       |
| Source              | FileSource  | Indica la posizione del file di dati quando il parametro `BatchData` è null.                                                               |

### Risposta

Una richiesta riuscita restituisce **HTTP 200** con un payload JSON simile al seguente:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codici di stato possibili:

| Codice | Significato                                 |
| ------ | ------------------------------------------- |
| 200    | Importazione riuscita                       |
| 400    | Richiesta non valida – dati mancanti o errati |
| 401    | Non autorizzato – token non valido o mancante |
| 500    | Errore interno del server                   |


## Come utilizzare l’API PostImportData con gli SDK

### Specifica dell’API PostImportData

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L’uso di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

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
{{< /tab >}}

{{< /tabs >}}
---