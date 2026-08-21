---
title: "Aspose.Cells Cloud Web API - Esporta foglio di calcolo remoto in altri formati - Strumento online gratuito"
second_title: "Documento"
ArticleTitle: "Come esportare un foglio di calcolo remoto in altri formati: Guida passo-passo"
linktype: "Esporta foglio di calcolo come formato"
type: docs
url: /it/export-spreadsheet-as-format/
keywords: "Aspose.Cells, conversione foglio di calcolo, API, esportazione, PDF, CSV, JSON, XLSX"
description: "Converti cartelle di lavoro Excel memorizzate in Aspose Cloud in PDF, XLSX, CSV, JSON o HTML tramite un singolo endpoint REST. Scopri la sintassi della richiesta, i parametri e gli esempi di SDK in C#, Java, Python e altri linguaggi."
weight: 100
---

Esporta un foglio di calcolo cloud (Excel) in un altro formato file.

## **API Esporta foglio di calcolo come formato**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Parametri della richiesta:**

| Nome parametro | Tipo   | Percorso/Query string/Corpo HTTP | Descrizione                                                                                                                                         |
| :------------- | :----- | :-------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Percorso                      | (Obbligatorio) Il nome del file della cartella di lavoro da recuperare.                                                                             |
| format         | String | Query                         | (Obbligatorio) Il formato di output desiderato (ad esempio, “Xlsx”, “PDF”, “CSV”).                                                                  |
| folder         | String | Query                         | (Opzionale) Il percorso della cartella in cui è memorizzata la cartella di lavoro. L’impostazione predefinita è null.                               |
| storageName    | String | Query                         | (Opzionale) Nome dello storage se si utilizza un cloud storage personalizzato. Utilizzare lo storage predefinito se omesso.                         |
| outPath        | String | Query                         | (Opzionale) Il percorso della cartella in cui verrà salvata la cartella di lavoro. L’impostazione predefinita è null.                               |
| outStorageName | String | Query                         | (Opzionale) Nome dello storage per il file di output.                                                                                               |
| fontsLocation  | String | Query                         | (Opzionale) Percorso personalizzato per i caratteri.                                                                                                |
| region         | String | Query                         | (Opzionale) Impostazione di regione/lingua del foglio di calcolo (ad esempio, `it-IT`, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, l'analisi delle date e il comportamento specifico della località. |
| password       | String | Query                         | (Opzionale) La password per aprire il file del foglio di calcolo.                                                                                   |

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

La risposta contiene un singolo oggetto che rappresenta il flusso del file convertito.

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

## Dove dovresti utilizzare l’API Esporta foglio di calcolo come altro formato?

- **Migrazione di sistemi legacy**: Converti migliaia di file XLS legacy in XLSX per sistemi moderni.
- **Standardizzazione per l’archiviazione**: Normalizza vari formati di fogli di calcolo (XLS, XLSM, ODS, CSV) in un singolo formato per l’archiviazione.
- **Interoperabilità con suite office**: Converti file Excel in formati compatibili con LibreOffice, Google Sheets o Apple Numbers.
- **Normalizzazione delle fonti dati**: Converti vari formati di fogli di calcolo in CSV o JSON per l’ingestione nel database.
- **Pubblicazione web**: Converti modelli finanziari in HTML per la visualizzazione su web.

## Perché dovresti utilizzare l’API Esporta foglio di calcolo come altro formato?

- **Facile da usare per sviluppatori**: Aspose.Cells Cloud offre librerie SDK in diversi linguaggi, consentendo uno sviluppo rapido, e dispone di una documentazione completa. Rispetto alla creazione di soluzioni personalizzate per il rendering dei grafici, riduce significativamente il carico di lavoro di sviluppo.
- **Riduzione dei costi del personale**: Riduce la necessità di assegnare ruoli specifici alla gestione della consolidazione dei documenti.
- **Pagamento in base all’uso**: Nessun investimento iniziale; paghi solo per le chiamate API effettivamente utilizzate.
- **Nessuna manutenzione lato server richiesta**: Nessuna necessità di mantenere server, aggiornare software o gestire problemi di compatibilità.
- **Ampio supporto per i formati**: Converti tra oltre 20 formati di fogli di calcolo.
- **Mantiene la fedeltà dei dati e la formattazione originale**: Preserva il layout, le formule e lo stile originali durante la conversione.

## Come utilizzare l’API Esporta foglio di calcolo come formato con gli SDK?

### Specifica dell’API Esporta foglio di calcolo come formato

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">Specifiche dell’API Esporta foglio di calcolo come formato</a> fornisce un’interfaccia di programmazione accessibile pubblicamente per effettuare interazioni REST in modo fluido.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web di Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud tramite cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
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

### Utilizzare gli SDK di Aspose.Cells Cloud

Utilizzare un SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendoti di esportare un foglio di calcolo in un file di formato con poche righe di codice.  
Prima di chiamare l’API, ottieni un token di accesso OAuth 2.0 e includilo nell’intestazione `Authorization: Bearer <token>`.

Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice illustrano come interagire con i servizi web di Aspose.Cells tramite vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}