---
title: "Creare API Foglio di Lavoro – Aspose.Cells Cloud (v5.0) | Generare File Excel"
second_title: "Documento"
ArticleTitle: "Come creare nuovi fogli di calcolo Excel – Generare file vuoti o basati su modelli"
linktitle: "Creare Foglio di Lavoro"
type: docs
url: /it/create-spreadsheet/
keywords: "Aspose.Cells, API foglio di lavoro, creare Excel, cloud, XLSX, ODS, CSV, modello, SDK, automazione"
description: "Scopri come creare cartelle di lavoro Excel vuote o basate su modelli usando l'API Aspose.Cells Cloud (v5.0). Include endpoint, parametri, codici di errore, fasi di autenticazione ed esempi di SDK."
weight: 100
---

Crea programmaticamente nuovi fogli di calcolo Excel usando l'API Aspose.Cells Cloud. Genera cartelle di lavoro vuote o istanzia file a partire da modelli personalizzati. L’API REST permette la creazione automatizzata di file Excel, ideale per la generazione di report, l’automazione di documenti e i flussi di lavoro di elaborazione dati.

## **API Creare Foglio di Lavoro**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/create
```

### **Sicurezza e Autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della Richiesta

| Nome Parametro     | Tipo   | Posizione | Descrizione                                                                                                                                       |
| ------------------ | ------ | --------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **format**         | String | Query     | **Obbligatorio**. Formato del file per il nuovo foglio di lavoro (ad esempio, `XLSX`, `XLS`, `ODS`, `CSV`).                                      |
| **template**       | String | Query     | **Facoltativo**. Nome di un file modello memorizzato nel tuo archivio cloud (ad esempio, `invoice_template.xlsx`). Se omesso, viene creata una cartella di lavoro vuota. |
| **outPath**        | String | Query     | **Facoltativo**. Percorso della cartella di destinazione nell'archivio cloud per il file generato. Se `null` o omesso, il foglio di lavoro viene salvato nella posizione predefinita. |
| **outStorageName** | String | Query     | **Obbligatorio**. Identificatore dell’archivio cloud configurato (ad esempio, `MyDrive`).                                                        |
| **region**         | String | Query     | **Facoltativo**. Impostazione locale (ad esempio, `fr-FR`) che determina i formati predefiniti per date, numeri e valute.                        |
| **password**       | String | Query     | **Facoltativo**. Password per un file modello crittografato. Lasciare vuoto se il modello non è protetto.                                         |

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

**Codici di Stato HTTP**

| Codice | Significato            | Descrizione                                                      |
| ------ | ---------------------- | ---------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non valida   | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT non valido o mancante.                                 |
| 413    | Payload Troppo Grande  | Il file caricato supera il limite di dimensione.                |
| 500    | Errore Interno Server  | Errore imprevisto del server.                                    |

## Dove utilizzare l’API Creare Foglio di Lavoro?

- **Inizializzazione del Sistema di Report Automatizzato** – Crea una nuova cartella di lavoro vuota o genera un file di report a partire da un modello standard all’inizio di ogni ciclo di automazione quotidiano/settimanale.
- **Portale Self‑service per gli Utenti** – Consenti ai clienti di selezionare un modello (preventivo, piano di progetto, ecc.) e scaricare istantaneamente un file Excel personalizzato.
- **Esportazione e Distribuzione in Batch dei Dati** – Produci cartelle di lavoro separate con un formato uniforme per ciascun insieme di dati esportati, semplificando la distribuzione e l’elaborazione successiva.

Per operazioni successive, come l’aggiunta di fogli di calcolo o la compilazione delle celle, consulta le API **Aggiungi Foglio di Lavoro**, **Aggiorna Cella** e **Esporta Cartella di Lavoro**.

## Perché utilizzare l’API Creare Foglio di Lavoro?

- **Facile da Usare per gli Sviluppatori** – Fornisce librerie SDK per molteplici linguaggi e una documentazione approfondita, semplificando l’integrazione rispetto alla creazione di soluzioni personalizzate.
- **Efficienza Lavorativa** – Permette l’automazione della consolidazione dei documenti, riducendo lo sforzo manuale.
- **Prezzo basato sull’uso** – I costi sono basati sull’utilizzo dell’API, senza oneri di licenza iniziale.
- **Servizio Gestito** – L’API è completamente ospitata, eliminando la necessità di manutenzione di server on‑premises o aggiornamenti software.

## Come Usare l’API Creare Foglio di Lavoro con gli SDK

### Specifica dell’API Creare Foglio di Lavoro

La [Specifica dell’API Creare Foglio di Lavoro](https://reference.aspose.cloud/cells/#/ManagementController/CreateSpreadsheet) definisce un’interfaccia di programmazione pubblicamente accessibile e consente interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/create?format=XLSX&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}"
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

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per lo sviluppo, poiché astrae i dettagli di basso livello e consente di creare il foglio di lavoro con codice conciso. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come richiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CreateSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CreateSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CreateSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CreateSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CreateSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CreateSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CreateSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CreateSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}