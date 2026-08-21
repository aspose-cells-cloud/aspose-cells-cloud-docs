---
title: "Aspose.Cells Cloud Split Excel Web API – Dividi Excel localmente in più file ed esporta in oltre 30 formati"
second_title: "Documento"
ArticleTitle: "Strumento di divisione Excel – Dividi foglio di calcolo locale in file in oltre 30 formati"
linktitle: "Dividi foglio di calcolo"
type: docs
url: /it/split-spreadsheet/
keywords: "divisione, excel, aspose cells, API foglio di calcolo, esporta pdf, csv, json"
description: "Dividi un workbook Excel localmente in file separati utilizzando l'API Aspose.Cells Cloud. Esporta in oltre 30 formati (PDF, CSV, JSON, XLSX, HTML) senza caricare i dati su cloud."
weight: 100
---

Dividi un workbook Excel locale in file separati in modo completo — nessuna archiviazione su cloud necessaria. L’output supporta oltre 30 formati, tra cui PDF, CSV, JSON, ODS e XPS.

## **API per la divisione del foglio di calcolo**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/split/spreadsheet
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta:**

| Nome parametro | Tipo    | Percorso/QueryString/Corpo HTTP | Descrizione                                                                                                                                                                       |
| :------------- | :------ | :----------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File    | FormData                       | Il file locale del foglio di calcolo da dividere. I formati supportati includono XLSX, XLS, ODS, CSV, ecc. Il file viene elaborato interamente sul server senza richiedere archiviazione su cloud. |
| from           | Integer | Query                          | Indice iniziale (base zero) dell'intervallo di fogli da dividere (es. `0` per il primo foglio).                                                                                  |
| to             | Integer | Query                          | Indice finale (base zero) dell'intervallo di fogli da dividere (es. `2` dividerà i fogli 0, 1 e 2).                                                                              |
| outFormat      | String  | Query                          | Format di output per i file risultanti. Supporta oltre 30 formati, tra cui `PDF`, `CSV`, `JSON`, `XLSX`, `HTML`.                                                                |
| outPath        | String  | Query                          | _(Opzionale)_ Il percorso della cartella locale dove salvare i file risultanti. Se omesso, i file verranno salvati in una posizione temporanea predefinita.                      |
| outStorageName | String  | Query                          | Identificatore dello storage per organizzare i file di output. In modalità di elaborazione locale, solitamente si riferisce a un'etichetta di storage definita dalla sessione o dall'utente. |
| fontsLocation  | String  | Query                          | _(Opzionale)_ Specifica una directory locale o personalizzata dei font per garantire una corretta resa del testo durante l'esportazione in PDF o formati immagine.             |
| region         | String  | Query                          | _(Opzionale)_ Imposta le impostazioni locali per la formattazione di numeri, date e valute nei file di output (es. `"en-US"`, `"de-DE"`).                                        |
| password       | String  | Query                          | _(Opzionale)_ Se il foglio di calcolo caricato è protetto da password, fornire la password per aprirlo ed elaborarlo.                                                            |

## **Risposta**

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

Il file può essere scaricato direttamente o salvato nella posizione specificata da `outPath`.

**Dettagli della risposta in caso di successo**

| Codice di stato | Content-Type               | Descrizione                                    |
| --------------- | -------------------------- | ---------------------------------------------- |
| 200 OK          | `application/octet-stream` | Stream binario del file workbook unito.        |

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                      |
| ------ | ----------------------- | ---------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato con successo; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                 |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                |
| 500    | Errore interno del server | Errore imprevisto sul server.                                    |

## Dove utilizzare l'API per la divisione del foglio di calcolo?

- **Distribuzione dati per dipartimento**: Dividi un workbook unificato contenente dati di più dipartimenti in file specifici per ciascun dipartimento.
- **Distribuzione report regionali**: Dividi i report nazionali di vendita in file separati per regione.
- **Distribuzione mascheramento dati clienti**: Dividi un workbook contenente informazioni sensibili in un file con dati clienti ridotti e anonimizzati.
- **Divisione periodica dei report**: Dividi automaticamente i report riassuntivi in report settimanali o giornalieri su base mensile.
- **Distribuzione multi-formato**: Dividi un singolo file Excel in più versioni in formati diversi (PDF, CSV, JSON, ecc.) contemporaneamente.
- **Divisione basata su modelli**: Dividi file di dati in file di output standardizzati seguendo modelli predefiniti.
- **Pre-elaborazione delle origini dati**: Dividi il file Excel in un file CSV standardizzato prima del caricamento nel database.
- **Preparazione dati per API**: Dividi dataset di grandi dimensioni in blocchi più piccoli adatti per il trasferimento tramite API.

## Perché utilizzare l'API per la divisione del foglio di calcolo?

- **Facile da usare per sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido e fornendo documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering di grafici, riduce significativamente il carico di lavoro.
- **Riduzione dei costi del personale**: Riduce la necessità di figure dedicate alla consolidazione dei documenti.
- **Pagamento in base all’uso**: Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi di manutenzione nulli**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.
- **Mantiene la formattazione complessa di Excel** nel formato PDF, universalmente accessibile.

## Come utilizzare l'API per la divisione del foglio di calcolo con gli SDK

### Specifica dell'API per la divisione del foglio di calcolo

La [Specifiche dell'API per la divisione del foglio di calcolo](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitSpreadsheet) fornisce un'interfaccia di programmazione accessibile pubblicamente per eseguire interazioni REST direttamente da un browser web.
Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/split/spreadsheet?outFormat=PDF" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o split-spreadsheet.zip
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

L'utilizzo degli SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello e permette di dividere il foglio di calcolo in file separati con codice minimo.  
Controlla il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web di Aspose.Cells utilizzando diversi SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}