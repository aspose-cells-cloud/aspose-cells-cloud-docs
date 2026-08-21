---
title: "Aspose.Cells Cloud Spreadsheet Splitter Web API - Suddividi il file Excel in più file in oltre 30 formati"
second_title: "Documento"
ArticleTitle: "Suddividi il file Excel nel cloud per separarlo in più file ed esportarlo in oltre 30 formati"
linktitle: "Suddividi foglio di calcolo remoto nel cloud"
type: docs
url: /it/split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, suddividi cartella di lavoro Excel, strumento per la suddivisione di fogli di calcolo, API cloud, esporta in PDF, esporta in CSV, esporta in JSON, esportazione in formati multipli, elaborazione di fogli di calcolo nel cloud"
description: "Utilizza l'API Aspose.Cells Cloud per suddividere una cartella di lavoro Excel memorizzata nell'archivio cloud in singoli fogli di calcolo ed esportare ciascuna parte in oltre 30 formati, tra cui PDF, CSV, JSON, XLSX, HTML, ODS e XPS."
weight: 100
---

Suddividi una grande cartella di lavoro Excel memorizzata nel cloud in file separati per foglio e esporta ciascuno in oltre 30 formati di output, tra cui PDF, CSV, JSON, ODS e XPS, utilizzando Aspose.Cells Cloud.

## **API per la suddivisione di fogli di calcolo remoti**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo    | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                                           |
| :------------- | :------ | :------------------------------ | :------------------------------------------------------------------------------------------------------------------------------------ |
| name           | String  | Percorso                        | Nome del file della cartella di lavoro (ad esempio `data.xlsx`) da suddividere, posizionato nella cartella specificata dell'archivio cloud. |
| folder         | String  | Query                           | Percorso della cartella nell'archivio cloud in cui è memorizzata la cartella di lavoro sorgente.                                    |
| from           | Integer | Query                           | Indice iniziale (0-based) del foglio di calcolo da cui iniziare l'operazione di suddivisione. Ad esempio, `0` indica il primo foglio. |
| to             | Integer | Query                           | Indice finale (0-based) del foglio di calcolo fino al quale procedere con la suddivisione. Ad esempio, `2` suddivide i fogli 0, 1 e 2. |
| outFormat      | String  | Query                           | Format del file di output per i file suddivisi. I formati supportati includono `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` e oltre 30 altri. |
| storageName    | String  | Query                           | _(Opzionale)_ Nome dell'archivio cloud in cui si trova la cartella di lavoro sorgente. Se omesso, viene utilizzato l'archivio cloud predefinito. |
| outPath        | String  | Query                           | _(Opzionale)_ Percorso della cartella di destinazione nell'archivio cloud in cui verranno salvati i file suddivisi. Se omesso, i file verranno salvati nella cartella sorgente. |
| outStorageName | String  | Query                           | Nome dell'archivio cloud in cui verranno salvati i file suddivisi in uscita.                                                        |
| fontsLocation  | String  | Query                           | _(Opzionale)_ Specifica un percorso personalizzato di una cartella cloud contenente i file di font per un corretto rendering del testo in output PDF o immagine. |
| region         | String  | Query                           | _(Opzionale)_ Imposta il locale per la formattazione di numeri, date e valute nei file di output (ad esempio `"it-IT"`, `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password       | String  | Query                           | _(Opzionale)_ Se la cartella di lavoro sorgente è protetta da password, fornire la password per aprirla.                              |

## **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

Il file può essere scaricato direttamente o salvato nella posizione specificata da `outPath`.

**Dettagli della risposta in caso di successo**

| Codice di stato | Content-Type               | Descrizione                                     |
| --------------- | -------------------------- | ----------------------------------------------- |
| 200 OK          | `application/octet-stream` | Flusso binario del file della cartella di lavoro suddivisa. |

**Codici di stato HTTP**

| Codice | Significato            | Descrizione                                                             |
| ------ | ---------------------- | ----------------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida   | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT non valido o mancante.                                        |
| 413    | Payload troppo grande  | Il file caricato supera il limite di dimensione.                       |
| 500    | Errore interno del server | Errore imprevisto del server.                                          |

## Dove utilizzare l'API per la suddivisione di fogli di calcolo remoti?

- **Distribuzione dei dati per reparto**: suddividi una singola cartella di lavoro contenente dati di più reparti in file specifici per reparto.
- **Distribuzione di report regionali**: suddividi i report di vendita nazionali in file separati per regione.
- **Distribuzione mascherata dei dati dei clienti**: suddividi una cartella di lavoro contenente informazioni sensibili in un file dedicato per la visualizzazione da parte dei clienti.
- **Suddivisione periodica dei report**: suddividi automaticamente i report di sintesi in report settimanali o giornalieri su base mensile.
- **Distribuzione in formati multipli**: suddividi un singolo file Excel in più versioni in diversi formati (PDF, CSV, JSON, ecc.) contemporaneamente.
- **Suddivisione basata su modelli**: suddividi i file di dati in file di output standardizzati in base a modelli predefiniti.
- **Pre-elaborazione della fonte dati**: suddividi il file Excel in un file CSV standardizzato prima di caricare i dati nel database.
- **Preparazione dei dati per l'API**: suddividi grandi set di dati in blocchi più piccoli adatti per il trasferimento tramite API.
- **Distribuzione dati in microservizi**: suddividi il file dati centrale in file di dati separati richiesti da ciascun microservizio.

## Perché utilizzare l'API per la suddivisione di fogli di calcolo remoti?

- **Facile da usare per sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido, e include una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering di grafici, riduce notevolmente il carico di lavoro di sviluppo.
- **Riduzione dei costi del personale**: diminuisce la necessità di figure dedicate alla consulenza e alla gestione della documentazione.
- **Pagamento in base all'uso**: nessun investimento iniziale; si paga solo per le chiamate API effettivamente utilizzate.
- **Costi zero di manutenzione**: non è necessario mantenere server, aggiornare software o gestire problemi di compatibilità.
- **Preserva la formattazione complessa di Excel** in un formato PDF universalmente accessibile.

## Come utilizzare l'API per la suddivisione di fogli di calcolo remoti con gli SDK

### Specifica dell'API per la suddivisione di fogli di calcolo remoti

La [Specifica dell'API per la suddivisione di fogli di calcolo remoti](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

L'utilizzo di un SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendoti di suddividere il foglio di calcolo memorizzato nel cloud in file separati con pochissimo codice.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.  
I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}