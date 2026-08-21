---
title: "Esporta intervallo Excel in PDF, PNG, CSV – Aspose.Cells Cloud API"
second_title: "Documento"
ArticleTitle: "Come esportare un intervallo di foglio di calcolo remoto in altri formati: guida passo-passo"
linktitle: "Esporta intervallo come formato"
type: docs
url: /export-range-as-format/
keywords: "Aspose Cells, esporta intervallo Excel, PDF, PNG, CSV, API cloud, conversione foglio di calcolo"
description: "Scopri come convertire un intervallo Excel specifico memorizzato in Aspose Cells Cloud in PDF, PNG, CSV o altri formati. Include dettagli sull’endpoint, parametri, richieste di esempio, gestione della risposta e informazioni sugli errori."
weight: 100
---

Esporta un intervallo di foglio di calcolo/Excel in cloud in un file di formato. Il file di formato può essere salvato in cloud o esportato in archiviazione locale.

## API Esporta intervallo come formato

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{range}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome del parametro | Tipo   | Posizione | Descrizione                                                                                                                                              |
| :----------------- | :----- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path      | (Obbligatorio) Nome del file del workbook da recuperare.                                                                                               |
| **worksheet**      | String | Path      | Nome del foglio di calcolo.                                                                                                                            |
| **range**          | String | Path      | Intervallo da convertire (ad esempio, `A1:C12`).                                                                                                       |
| **format**         | String | Query     | (Obbligatorio) Formato di output desiderato (ad esempio, `pdf`, `png`, `svg`).                                                                         |
| **folder**         | String | Query     | (Facoltativo) Percorso della cartella in cui è memorizzato il workbook.                                                                                |
| **storageName**    | String | Query     | (Facoltativo) Nome dell’archivio se si utilizza un archivio cloud personalizzato.                                                                      |
| **outPath**        | String | Query     | (Facoltativo) Percorso del file di output nell’archivio cloud.                                                                                         |
| **outStorageName** | String | Query     | (Facoltativo) Nome dell’archivio per il file di output.                                                                                                |
| **fontsLocation**  | String | Query     | (Facoltativo) Percorso personalizzato dei font.                                                                                                        |
| **region**         | String | Query     | (Facoltativo) Impostazione di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l’analisi delle date e il comportamento specifico della località. |
| **password**       | String | Query     | (Facoltativo) Password necessaria per aprire il file del foglio di calcolo.                                                                            |

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

| Codice | Significato             | Descrizione                                                            |
| ------ | ----------------------- | ---------------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                       |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                      |
| 500    | Errore interno del server | Errore imprevisto sul server.                                          |

## Dove dovresti utilizzare l’API Esporta intervallo in un altro formato?

### Scenari di esportazione e migrazione dati

- **Integrazione con database** – Esporta intervalli Excel specifici direttamente nei sistemi di database.
- **Integrazione con applicazioni** – Fornisci dati selezionati del foglio di calcolo alle applicazioni SaaS.
- **Migrazione di sistemi** – Trasferisci intervalli di dati specifici tra sistemi legacy e moderni.
- **Condivisione cross-platform** – Condividi sottoinsiemi di dati focalizzati tra diverse piattaforme.

### Segnalazione e analisi

- **Segnalazione mirata** – Esporta sezioni specifiche di report in altri formati per un’analisi mirata.
- **Flussi di dati per dashboard** – Fornisci intervalli di dati specifici agli strumenti di dashboard BI.
- **Metriche di performance** – Estrai intervalli di KPI per sistemi di monitoraggio delle performance.
- **Segnalazione finanziaria** – Esporta sezioni di bilanci per audit esterni.

### Sviluppo e test

- **Gestione dei dati di test** – Esporta intervalli di dati specifici per scopi di test.
- **Ambienti di sviluppo** – Condividi intervalli di dati di esempio con i team di sviluppo.
- **Test delle API** – Genera dati di test CSV da sezioni specifiche del foglio di calcolo.
- **Sviluppo di prototipi** – Fornisci set di dati mirati per prototipi di applicazioni.

### Operazioni aziendali

- **Condivisione selettiva dei dati** – Condividi intervalli di dati specifici con partner esterni.
- **Backup parziale dei dati** – Esegui il backup di intervalli di dati critici in un formato scelto.
- **Trasferimento dati tra dipartimenti** – Condividi dati specifici tra dipartimenti.
- **Segnalazione di conformità** – Esporta intervalli di dati normativi per la presentazione di report di conformità.

### Flussi di lavoro automatizzati

- **Esportazioni programmate di intervalli** – Esporta automaticamente intervalli specifici in base a una pianificazione.
- **Estrazione basata su trigger** – Esporta intervalli in base a eventi aziendali o trigger.
- **Integrazione nei flussi di lavoro** – Integra le esportazioni di intervalli nei flussi di processo aziendale.
- **Elaborazione batch di intervalli** – Elabora più intervalli specifici in operazioni in batch.

## Perché dovresti utilizzare l’API Esporta intervallo in un altro formato?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido con documentazione completa. Rispetto alla creazione di soluzioni personalizzate di rendering grafici, riduce notevolmente il carico di lavoro di sviluppo.
- **Riduzione dei costi del personale** – Minor bisogno di personale dedicato alla consolidazione dei documenti.
- **Pay-per-use** – Nessun investimento iniziale: paghi solo per le chiamate API effettivamente utilizzate.
- **Nessuna manutenzione del server** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.
- **Preserva la formattazione complessa di Excel** – I file di output mantengono la formattazione originale del foglio di calcolo.

## Come utilizzare l’API Esporta intervallo foglio di calcolo come formato con gli SDK?

### Specifica dell’API Esporta intervallo come formato

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportRangeAsFormat" rel="noopener noreferrer">Specifica dell’API Esporta intervallo come formato</a> fornisce un’interfaccia di programmazione pubblicamente accessibile, consentendo interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/ranges/A1:C12?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file facoltativo"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L’utilizzo dell’SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di esportare un intervallo di foglio di calcolo in un file di formato con codice conciso. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportRangeAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportRangeAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportRangeAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportRangeAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportRangeAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportRangeAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportRangeAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportRangeAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}