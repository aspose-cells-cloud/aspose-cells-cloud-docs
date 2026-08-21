---
title: "Aspose.Cells Cloud Excel Compression Web API – Ridurre la dimensione dei file di foglio di calcolo in modo programmatico"
second_title: "Documento"
ArticleTitle: "Come comprimere file Excel – Ridurre le dimensioni dei fogli di calcolo e ottimizzare le prestazioni"
linktitle: "Comprimi foglio di calcolo"
type: docs
url: /it/compress-spreadsheet/
keywords: "Compressione Excel, Aspose.Cells Cloud, riduzione dimensione foglio di calcolo, API, ottimizzazione cartella di lavoro"
description: "Scopri come comprimere cartelle di lavoro Excel con l'API Aspose.Cells Cloud. Ottieni esempi passo-passo, parametri, autenticazione e best practice."
weight: 100
---

Comprimi in modo programmatico fogli di calcolo Excel e riduci la dimensione dei file con l'API Aspose.Cells Cloud. Ottimizza le prestazioni della cartella di lavoro rimuovendo dati non utilizzati, comprimendo oggetti incorporati e pulendo la formattazione. Questa API RESTful consente di automatizzare i flussi di lavoro di compressione e ottimizzazione dei file Excel.

## **API per la compressione del foglio di calcolo**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parametri della richiesta

| Nome parametro | Tipo    | Percorso/Query/Stringa/Corpo HTTP | Descrizione                                                                                                                     |
| -------------- | ------- | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File    | FormData                          | **Obbligatorio.** Il file della cartella di lavoro Excel sorgente (`.xlsx`, `.xls`, ecc.) da comprimere.                        |
| level          | Integer | Query                             | **Opzionale.** Intensità della compressione (0 = più veloce/meno intensa, 9 = più lenta/massima). Se omesso, viene applicato un valore predefinito bilanciato (5). |
| outPath        | String  | Query                             | **Opzionale.** Percorso della cartella di destinazione nel tuo archivio cloud. Se omesso, il file viene salvato nella stessa cartella della cartella di lavoro sorgente. |
| outStorageName | String  | Query                             | **Obbligatorio.** Identificatore del servizio di archivio cloud configurato (es. `CorporateDrive`).                            |
| region         | String  | Query                             | **Opzionale.** Impostazione locale (es. `de-DE`) che potrebbe influenzare la gestione dei dati specifici per regione.           |
| password       | String  | Query                             | **Opzionale.** Password per decrittografare un foglio di calcolo protetto. Lasciare vuoto se il file non è crittografato.       |

### Risposta

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Codici di stato HTTP**

| Codice | Significato         | Descrizione                                                    |
| ------ | ------------------- | -------------------------------------------------------------- |
| 200    | OK                  | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato     | Token JWT non valido o mancante.                               |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.              |
| 500    | Errore interno del server | Errore imprevisto del server.                                 |

## Dove dovresti utilizzare l’API per la compressione del foglio di calcolo?

- **Distribuzione automatica di report** – Comprimi i bilanci mensili prima di inviarli via email per garantire la riuscita della consegna e migliorare l’esperienza del destinatario.
- **Ottimizzazione del caricamento dei file da parte degli utenti** – Comprimi i file Excel caricati in background per risparmiare spazio di archiviazione cloud e ridurre i costi di archiviazione.
- **Elaborazione e migrazione di pipeline dati** – Comprimi i file Excel intermedi generati durante i processi ETL per velocizzare il trasferimento in rete e ridurre il carico di archiviazione temporanea.

## Perché dovresti utilizzare l’API per la compressione del foglio di calcolo?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido con una documentazione completa.
- **Riduzione dei costi del personale** – Elimina la necessità di personale dedicato per la consolidazione manuale dei documenti.
- **Prezzi basati sull’uso** – Nessun investimento iniziale; paghi solo per le chiamate API effettivamente eseguite.
- **Nessuna manutenzione del server richiesta** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l’API per la compressione del foglio di calcolo con gli SDK

### Specifica dell’API per la compressione del foglio di calcolo

La [Specifica dell’API per la compressione del foglio di calcolo](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) fornisce un’interfaccia accessibile pubblicamente per le interazioni REST, consentendo chiamate dirette all’API da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK è il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello e ti permette di comprimere un foglio di calcolo con poche righe di codice. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells Cloud utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}