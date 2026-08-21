---
title: "Esporta foglio di lavoro – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Documento"
ArticleTitle: "Come esportare un foglio di lavoro di un foglio di calcolo remoto in un altro formato: Guida passo-passo"
linktitle: "Esporta foglio di lavoro"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, esporta foglio di lavoro, API cloud, PDF, PNG, CSV, conversione Excel"
description: "Converte un foglio di lavoro memorizzato in Aspose.Cells Cloud in PDF, PNG, SVG, CSV o altri formati tramite una singola richiesta GET. Include esempi di codice per C#, Java, Python e altro."
weight: 100
---

Esporta un foglio di lavoro di un foglio di calcolo/Excel in cloud in un file di un altro formato utilizzando l’API Web Aspose.Cells Cloud.

## **API Esporta foglio di lavoro in un formato**

### API Web

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Nome parametro     | Tipo   | Percorso/Stringa di query/Corpo HTTP | Descrizione                                                                                                                                         |
| :----------------- | :----- | :----------------------------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Percorso                             | (Obbligatorio) Il nome del file del foglio di calcolo da recuperare.                                                                               |
| **worksheet**      | String | Percorso                             | (Obbligatorio) Il foglio di lavoro specifico da convertire.                                                                                        |
| **format**         | String | Query                                | (Obbligatorio) Il formato di output desiderato (ad esempio, `png`, `pdf`, `svg`).                                                                  |
| **folder**         | String | Query                                | (Opzionale) Il percorso della cartella in cui è memorizzato il foglio di calcolo. Il valore predefinito è `null`.                                   |
| **storageName**    | String | Query                                | (Opzionale) Il nome dell’archiviazione cloud personalizzata. Usa l’archiviazione predefinita se omesso.                                             |
| **outPath**        | String | Query                                | (Opzionale) Il percorso della cartella di output. Il valore predefinito è `null`.                                                                  |
| **outStorageName** | String | Query                                | (Opzionale) Nome dell’archiviazione per il file di output.                                                                                         |
| **fontsLocation**  | String | Query                                | (Opzionale) Specifica i caratteri personalizzati, se necessario.                                                                                   |
| **region**         | String | Query                                | (Opzionale) Impostazione di regione/lingua del foglio di calcolo (ad esempio, `en-US`, `fr-FR`). Influenza la formattazione dei numeri, il parsing delle date e il comportamento specifico della localizzazione. |
| **password**       | String | Query                                | (Opzionale) La password per accedere al file del foglio di calcolo.                                                                                |

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

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                      |

## **Dove dovresti utilizzare l’API Esporta foglio di lavoro in un altro formato?**

- **Migrazione di sistemi legacy** – Converti migliaia di file XLS legacy in XLSX per sistemi moderni.
- **Standardizzazione dell’archiviazione** – Normalizza vari formati di fogli di calcolo (XLS, XLSM, ODS, CSV) a un unico formato per l’archiviazione.
- **Interoperabilità con suite per ufficio** – Converti file Excel in formati compatibili con LibreOffice, Google Sheets o Apple Numbers.
- **Normalizzazione delle fonti dati** – Converti vari formati di fogli di calcolo in CSV o JSON per l’ingestione in database.
- **Pubblicazione web** – Converti modelli finanziari in HTML per la visualizzazione web.

## Perché utilizzare l’API Esporta foglio di lavoro in un altro formato?

- **Supporto SDK multi-linguaggio** – Fornisce librerie client per diversi linguaggi di programmazione, consentendo agli sviluppatori di chiamare direttamente l’API dal proprio ambiente preferito.
- **Conversione diretta senza caricamento intermedio** – Consente di convertire un foglio di lavoro memorizzato nell’archiviazione cloud nel formato richiesto, senza la necessità di scaricare e ricaricare il file.
- **Estrazione solo dati** – Restituisce il contenuto del foglio di lavoro nel formato selezionato, senza conservare lo stile visivo.

## Come utilizzare l’API Esporta foglio di lavoro in un formato con gli SDK?

### Specifica dell’API Esporta foglio di lavoro in un formato

La [Specifica dell’API Esporta foglio di lavoro in un formato](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) fornisce un’interfaccia di programmazione accessibile pubblicamente per eseguire interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L’esempio seguente mostra come effettuare chiamate all’API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
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

L’uso dell’SDK è il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello, consentendo di esportare un foglio di lavoro di un foglio di calcolo in un file di formato con codice breve.  
Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}