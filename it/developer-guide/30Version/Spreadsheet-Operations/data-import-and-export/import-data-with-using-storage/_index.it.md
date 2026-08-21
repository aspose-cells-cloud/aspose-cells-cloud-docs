---
title: "Importa dati utilizzando l'archivio"
second_title: "Documenti"
linktype: "Importa dati con archivio"
type: docs
url: /import-data-with-using-storage/
aliases:
  - /import-data-into-excel-worksheet/
  - /import-data-into-worksheet/
  - /import-data-in-excel-worksheet/
  - /import-data/
  - /import/with-using-storage/
description: "Importa dati utilizzando l'archivio: importa dati in un foglio di calcolo Excel utilizzando l'API Aspose.Cells Cloud da vari origini di archiviazione. Supporta formati JSON, CSV e altri tramite HTTPS."
keywords: "Aspose.Cells Cloud, Excel, Importa dati, API REST, Archiviazione cloud, JSON, CSV, PDF, Markdown, HTTPS"
weight: 10
ArticleTitle: "Importa dati utilizzando l'archivio - Documentazione API Aspose.Cells Cloud"
---

Questa API REST importa dati in un file Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### I parametri della richiesta sono:

| Nome parametro | Tipo   | Posizione | Descrizione                                            |
| -------------- | ------ | -------- | ------------------------------------------------------ |
| name           | string | path     | Nome del file Excel.                                   |
| folder         | string | query    | Percorso della cartella nell'archivio in cui è presente il file. |
| storageName    | string | query    | Nome del servizio di archiviazione.                    |
| importData     | object | body     | Oggetto JSON contenente i dati da importare.           |

**I parametri relativi alle opzioni di importazione** sono descritti nel <a href="/cells/import/#import-data-option-parameter" rel="noopener noreferrer">link di riferimento</a>.

**Prerequisiti:** È necessario fornire un token JWT valido nell'intestazione `Authorization` e assicurarsi che il foglio di calcolo di destinazione esista già nella posizione specificata dell'archivio.

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore interno del server   | Errore imprevisto nel server. |

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostImportData" rel="noopener noreferrer">Specifiche OpenAPI</a> definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di eseguire interazioni REST direttamente da un browser web.

È possibile utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come chiamare l'API cloud tramite cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Richiesta" tabName2="Risposta" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
     -X POST \
     -d '{"Data":[1,2,4],"DestinationWorksheet":"Sheet1","FirstRow":1,"FirstColumn":2,"IsVertical":true,"IsInsert":true,"importDataType":"IntArray"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più efficace per velocizzare lo sviluppo. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Consulta il <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.

L'esempio di codice seguente mostra come chiamare il servizio web Aspose.Cells tramite l'SDK PHP:
---