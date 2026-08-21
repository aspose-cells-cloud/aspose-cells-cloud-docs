---
title: "Salva foglio di calcolo in un altro formato – Aspose.Cells Cloud API (v4.0)"
second_title: "Documento"
ArticleTitle: "Come salvare un foglio di calcolo in un altro formato su archiviazione remota: Guida passo dopo passo"
linktitle: "Salva foglio di calcolo come"
type: docs
url: /it/save-spreadsheet-as/
keywords: "Aspose Cells, conversione foglio di calcolo, salva come, API, XLSX in PDF, archiviazione cloud, Excel in PDF, esportazione CSV, conversione cloud"
description: "Scopri come salvare un foglio di calcolo memorizzato in Aspose Cloud in un altro formato (XLSX, PDF, CSV, ecc.) utilizzando l'API Aspose.Cells Cloud per il salvataggio del foglio di calcolo. Include sintassi della richiesta, parametri, esempio curl e codice SDK."
weight: 100
---

Salva un foglio di calcolo o un file Excel in cloud in un formato diverso sull'archiviazione cloud.

## **API per salvare il foglio di calcolo**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### **Parametri della richiesta**

| Nome parametro  | Tipo   | Posizione | Descrizione                                                                               |
| :-------------- | :----- | :-------- | :---------------------------------------------------------------------------------------- |
| name            | Stringa | Path      | **Obbligatorio.** Il nome del file del workbook da convertire.                            |
| format          | Stringa | Query     | **Obbligatorio.** Il formato di output desiderato (ad esempio, `Xlsx`, `PDF`, `CSV`).     |
| saveOptionsData | Classe  | Body      | Dati opzionali per le opzioni di salvataggio. Se omessi, il valore predefinito è `null`.  |
| folder          | Stringa | Query     | Percorso della cartella opzionale dove è memorizzato il workbook sorgente. Se omesso, il valore predefinito è `null`. |
| storageName     | Stringa | Query     | Nome opzionale di un'archiviazione personalizzata. Se omesso, viene utilizzata l'archiviazione predefinita. |
| outPath         | Stringa | Query     | Percorso di output opzionale per il file convertito. Se omesso, il valore predefinito è `null`. |
| outStorageName  | Stringa | Query     | Nome opzionale dell'archiviazione per il file di output.                                  |
| fontsLocation   | Stringa | Query     | Percorso opzionale per i caratteri personalizzati.                                        |
| region          | Stringa | Query     | Impostazione opzionale della regione del foglio di calcolo.                               |
| password        | Stringa | Query     | Password opzionale per aprire il file del foglio di calcolo.                              |

**Formati di output supportati**

| Formato  | Estensione                                       |
| :------- | :----------------------------------------------- |
| Xlsx     | .xlsx                                            |
| Pdf      | .pdf                                             |
| Csv      | .csv                                             |
| Html     | .html                                            |
| Ods      | .ods                                             |
| Xls      | .xls                                             |
| Txt      | .txt                                             |
| Mhtml    | .mhtml                                           |
| Tiff     | .tiff                                            |
| Pptx     | .pptx                                            |
| … (altro) | Consulta la specifica dell’API per l’elenco completo (oltre 20 formati) |

### **Risposta**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Esempio di risposta di errore (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Parametri di richiesta non validi."
}
```

**Codici di stato HTTP**

| Codice | Significato            | Descrizione                                                       |
| ------ | ---------------------- | ----------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Bad Request            | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Unauthorized           | Token JWT non valido o mancante.                                  |
| 413    | Payload Too Large      | Il file caricato supera il limite di dimensione.                 |
| 500    | Internal Server Error  | Errore imprevisto del server.                                     |

## Dove dovresti utilizzare l’API per salvare il foglio di calcolo?

### Sistema aziendale di gestione documenti

- Salva automaticamente i report finanziari come archivi PDF.
- Esegui regolarmente il backup dei dati delle vendite in formato CSV.
- Salva i piani di progetto come file in sola lettura per impedire modifiche accidentali.

### Integrazione di dati e processi ETL

- Esporta i dati del sistema CRM e salvali come modello Excel standard.
- Converti i dati ERP in CSV per l'importazione in altri sistemi.
- Salva i dati grezzi in formato JSON per la trasmissione tramite API.

### scenari di sviluppo e automazione

- Elaborazione backend per applicazioni web.
- Sistemi automatizzati di generazione di report.
- Piattaforme di collaborazione cloud.
- Integrazione nei processi di approvazione.
- Backup e migrazione dati.

## Perché dovresti utilizzare l’API per salvare il foglio di calcolo?

- **Facile per gli sviluppatori** – Fornisce SDK per molteplici linguaggi con documentazione dettagliata, semplificando l’integrazione.
- **Efficiente in termini di tempo** – Esegue la conversione sul server, riducendo la necessità di scrivere codice personalizzato per la conversione.
- **Prezzo basato sull’uso** – Addebita solo per le chiamate API effettuate, senza costi iniziali per la licenza.
- **Nessuna manutenzione del server** – Il servizio viene eseguito in cloud, eliminando la necessità di gestire l’infrastruttura di conversione.
- **Ampia compatibilità con i formati** – Supporta la conversione tra oltre 20 formati di fogli di calcolo.
- **Fedeltà dei dati** – Preserva layout, formule e stili durante la conversione.

## Come utilizzare l’API per salvare il foglio di calcolo con gli SDK?

### Specifica dell’API per salvare il foglio di calcolo

La [Specifiche dell’API per salvare il foglio di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) definisce un'interfaccia di programmazione accessibile pubblicamente, consentendo di effettuare interazioni REST direttamente da un browser web.

**Esempio con corpo della richiesta e cURL**

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. Il seguente esempio mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello e consente di salvare un foglio di calcolo in un altro formato con un codice minimo. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}