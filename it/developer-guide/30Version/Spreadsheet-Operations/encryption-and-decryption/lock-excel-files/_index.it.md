---
title: "Blocca file Excel"
second_title: "Documento"
linktitle: "Blocca file Excel"
type: docs
url: /it/lock-excel-files/
aliases: [  /it/lock/without-storage/ , /it/lock/ , /it/lock/without-using-storage/ ]
keywords: "Blocca, Excel, API, Aspose.Cells, Cloud, REST, Workbook, Spreadsheet, SDK"
description: "Scopri come bloccare cartelle di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include endpoint HTTPS, autenticazione, richiesta cURL, schema di risposta e esempi di codice SDK per C#, Java, Python e altri linguaggi."
ArticleTitle: "Blocca file Excel – Documentazione API Aspose.Cells Cloud"
weight: 70
---

**Versione API:** v3.0 (corrente)

Questa REST API **blocca** le cartelle di lavoro Excel.

## API PostLock

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Prerequisiti** – La richiesta deve essere inviata tramite **HTTPS** e includere un token Bearer OAuth 2.0 valido nell'header `Authorization`.

### I parametri della richiesta sono

| Nome parametro | Tipo   | Posizione                   | Descrizione                                   |
| -------------- | ------ | -------------------------- | --------------------------------------------- |
| file           | file   | form‑data (corpo multipart) | La cartella di lavoro Excel da caricare e bloccare. |
| password       | string | stringa di query               | Password per la cartella di lavoro (opzionale).         |

La <a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come **chiamare** l'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*Puoi scaricare una cartella di lavoro di esempio — [Sample.xlsx](https://example.com/Sample.xlsx) — per testare la richiesta.*

**Nota:** L'API supporta file di dimensioni massime pari a 100 MB; payload più grandi potrebbero generare una risposta 413 (Payload Troppo Grande).

### **Dettagli della risposta**

| Campo       | Tipo            | Descrizione                                          |
| ----------- | --------------- | ---------------------------------------------------- |
| Filename    | string          | Nome della cartella di lavoro bloccata restituita dal servizio. |
| FileSize    | integer         | Dimensione del file bloccato in byte.                    |
| FileContent | string (Base64) | La cartella di lavoro bloccata codificata come stringa Base64.      |

Per recuperare la cartella di lavoro bloccata, decodifica il valore `FileContent` da Base64 e salvala utilizzando il nome `Filename` fornito nella risposta.

### **Gestione degli errori**

– L'API restituisce i codici di stato HTTP standard (ad esempio, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) insieme a un oggetto JSON di errore che contiene i campi `Code` e `Message`.

## Famiglia di SDK Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}
---