---
title: "Esporta Tabella – API Aspose.Cells Cloud | Converti Excel in PDF, PNG, CSV"
secondoTitolo: "Documentazione"
TitoloArticolo: "Come esportare una tabella di un foglio di calcolo remoto in un altro formato: Guida passo-passo"
linktitle: "Esporta tabella nel formato specificato"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, Esporta Tabella, Excel in PDF, API Cloud, REST"
description: "Esporta una tabella Excel memorizzata nel cloud in PDF, PNG, CSV, JSON o altri formati tramite Aspose.Cells Cloud API. Endpoint HTTPS sicuro con autenticazione JWT ed esempi di SDK."
weight: 100
---

Esporta una tabella di un foglio di calcolo (Excel) memorizzato nel cloud in un file in un altro formato.

## **API Esporta Tabella in un Formato**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Sicurezza e Autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della Richiesta:**

| Nome Parametro | Tipo   | Percorso/Query String/Corpo HTTP | Descrizione                                                                                                                                         |
| :------------- | :----- | :------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | Stringa | Percorso                         | **Obbligatorio.** Nome del file del foglio di calcolo da recuperare.                                                                               |
| worksheet      | Stringa | Percorso                         | Nome del foglio di calcolo.                                                                                                                         |
| tableName      | Stringa | Percorso                         | Nome della tabella.                                                                                                                                 |
| format         | Stringa | Query                            | **Obbligatorio.** Formato di output desiderato (ad esempio, “png”, “pdf”, “svg”).                                                                  |
| folder         | Stringa | Query                            | Opzionale. Percorso della cartella in cui è memorizzato il foglio di calcolo. Default: `null`.                                                     |
| storageName    | Stringa | Query                            | Opzionale. Nome dello storage personalizzato. Usa lo storage predefinito se omesso.                                                                |
| outPath        | Stringa | Query                            | Opzionale. Percorso della cartella di output. Default: `null`.                                                                                     |
| outStorageName | Stringa | Query                            | Opzionale. Nome dello storage per il file di output.                                                                                               |
| fontsLocation  | Stringa | Query                            | Opzionale. Percorso per i caratteri personalizzati.                                                                                                |
| region         | Stringa | Query                            | Opzionale. Impostazione regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione numerica, l'analisi delle date e il comportamento specifico della localizzazione. |
| password       | Stringa | Query                            | Opzionale. Password per aprire il file del foglio di calcolo.                                                                                      |

### **Risposta**

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

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non Valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non Autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload Troppo Grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore Interno del Server | Errore imprevisto sul server.                                     |

## **Dove Dovresti Utilizzare l’API Esporta Tabella in un Altro Formato?**

- **Migrazione di Sistemi Obsoleti**: Converti migliaia di file legacy XLS in XLSX per sistemi moderni.
- **Standardizzazione per Archiviazione**: Normalizza vari formati di fogli di calcolo (XLS, XLSM, ODS, CSV) in un unico formato per l’archiviazione.
- **Interoperabilità con Suite Office**: Converti file Excel in formati compatibili con LibreOffice, Google Sheets o Apple Numbers.
- **Normalizzazione Fonti Dati**: Converti vari formati di fogli di calcolo in CSV o JSON per l’ingestione nei database.
- **Pubblicazione Web**: Converti modelli finanziari in HTML per la visualizzazione sul web.

## Perché Dovresti Utilizzare l’API Esporta Tabella in un Altro Formato?

- **Facile da Usare per gli Sviluppatori**: Aspose.Cells Cloud offre librerie SDK in molteplici linguaggi, consentendo uno sviluppo rapido e accompagnato da una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, riduce notevolmente il carico di lavoro di sviluppo.
- **Riduzione dei Costi del Personale**: Diminuisce la necessità di assegnare risorse specifiche alla consolidazione dei documenti.
- **Pagamento a Utilizzo**: Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Costi di Manutenzione Nulli**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.
- **L’API restituisce solo i dati grezzi della tabella, senza alcuno stile del foglio di calcolo.**

## Come Utilizzare l’API Esporta Tabella di Foglio di Calcolo in un Formato con gli SDK?

### Specifica dell’API Esporta Tabella in un Formato

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">Specifiche dell’API Esporta Tabella in un Formato</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
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
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzo degli SDK di Aspose.Cells Cloud

L’utilizzo di un SDK rappresenta il modo più veloce per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di esportare una tabella di foglio di calcolo in un file in formato specifico con pochissime righe di codice. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}