---
title: "Ottenere il numero di pagine da un file Excel"
second_title: "Documento"
linktype: "Pagine"
type: docs
url: /get-page-count-from-an-excel-file/
aliases: [/workbook/page-count/, /workbook/get/page-count/]
keywords: "Aspose.Cells, API cloud, numero di pagine Excel, paginazione cartella di lavoro"
description: "Recupera il numero totale di pagine stampabili in una cartella di lavoro Excel tramite l'API REST di Aspose.Cells Cloud (v3.0). Include il formato della richiesta, i parametri obbligatori, un esempio cURL, lo schema di risposta, la gestione degli errori e frammenti SDK per diversi linguaggi."
weight: 10
version: "v3.0"
ArticleTitle: "Ottenere il numero di pagine da un file Excel utilizzando l'API Aspose.Cells Cloud"
---

Questa REST API restituisce il **numero di pagine** per una cartella di lavoro.

## Sicurezza e autenticazione
Le API Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione tramite token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## API REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### I parametri della richiesta

| Nome Parametro | Tipo   | Posizione | Obbligatorio | Descrizione                              |
| -------------- | ------ | --------- | ------------ | ---------------------------------------- |
| name           | string | path      | Sì           | Il nome del documento Excel.             |
| folder         | string | query     | No           | La cartella contenente il documento.     |
| storageName    | string | query     | No           | Il nome dello storage da utilizzare.     |

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente all'API REST di Aspose.Cells. L'esempio seguente mostra come chiamare l'endpoint con cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/IlTuoFile.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <token jwt>"
```

*Sostituisci `IlTuoFile.xlsx` con il nome effettivo della cartella di lavoro che desideri interrogare.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Schema di risposta

| Stato HTTP | Tipo dati | Descrizione                                                         |
| ---------- | --------- | ------------------------------------------------------------------- |
| 200        | integer   | Il numero totale di pagine stampabili nella cartella di lavoro (es. `13`). |
| 4xx‑5xx    | JSON      | Oggetto errore (vedere la sezione _Gestione errori_).                |

## Famiglia di SDK cloud

Utilizzare un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK si occupa dei dettagli a basso livello e ti permette di concentrarti sulle attività del tuo progetto.Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Gestione errori

| Stato HTTP | Descrizione                                  | Corpo JSON di esempio                                                                          |
| ---------- | -------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| 401        | Token JWT non valido o mancante.             | `{ "Code": "InvalidAuthenticationToken", "Message": "Il token di accesso è mancante o non valido." }` |
| 404        | La cartella di lavoro specificata non è stata trovata. | `{ "Code": "FileNotFound", "Message": "Il file richiesto non esiste." }`                |
| 400        | Richiesta non valida – parametri obbligatori mancanti. | `{ "Code": "BadRequest", "Message": "Parametro obbligatorio 'name' mancante." }`               |
| 500        | Errore interno del server.                   | `{ "Code": "InternalError", "Message": "Si è verificato un errore imprevisto." }`             |
---