---
title: "Importazione di dati in batch in un foglio di Excel"
second_title: "Document"
linktype: "Importazione di dati in batch"
type: docs
url: /it/import-batch-data-into-excel/
aliases:
  - /import-batch-data-into-worksheet/
  - /import-data/batch-data/
  - /import/batch-data/
keywords: "Aspose.Cells, API cloud, importazione di dati in batch, Excel, CSV, JSON, XML, array"
description: "Scopri come importare dati in batch (CSV, JSON, XML, array) in un foglio di Excel utilizzando l'API REST Aspose.Cells Cloud. Include esempi di autenticazione, richieste/risposte, frammenti di codice SDK e gestione degli errori."
weight: 19
ArticleTitle: "Importazione di dati in batch in un foglio di Excel – Documentazione di Aspose.Cells Cloud"
---

Questa API REST **importa dati in batch** in un foglio di Excel. Accetta una richiesta multipart in cui la prima parte contiene l'oggetto **ImportBatchDataOption** e la seconda parte trasporta il file di dati effettivo (CSV, JSON, XML, ecc.).

L'operazione utilizza una richiesta HTTP con contenuto multipart (vedere [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### ImportBatchDataOption

| Nome parametro           | Tipo              | Descrizione                                                                                                                                                                                   |
| ------------------------ | ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **BatchData**            | `List<CellValue>` | Raccolta di valori di cella da scrivere direttamente.                                                                                                                                         |
| **DestinationWorksheet** | `string`          | Nome del foglio di lavoro in cui verranno importati i dati.                                                                                                                                  |
| **IsInsert**             | `bool`            | Se `true`, i dati vengono inseriti e le celle esistenti vengono spostate; se `false`, i dati sovrascrivono le celle esistenti.                                                             |
| **ImportDataType**       | `string`          | Formato dei dati da importare. Valori ammessi: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | `FileSource`      | Specifica la posizione del file di dati quando **BatchData** è `null`.                                                                                                                       |

### CellValue

| Nome parametro  | Tipo     | Descrizione                                              |
| --------------- | -------- | -------------------------------------------------------- |
| **rowIndex**    | `int`    | Indice di riga (base zero) della cella di destinazione. |
| **columnIndex** | `int`    | Indice di colonna (base zero) della cella di destinazione. |
| **type**        | `string` | Tipo di dati del valore (ad esempio, `int`, `double`, `string`). |
| **value**       | `string` | Valore effettivo da scrivere nella cella.               |
| **style**       | `Style`  | Informazioni facoltative sullo stile della cella.       |

### FileSource

| Nome parametro     | Tipo     | Descrizione                                                           |
| ------------------ | -------- | --------------------------------------------------------------------- |
| **FileSourceType** | `string` | Origine del file: `InMemoryFiles`, `CloudFileSystem` o `RequestFiles`. |
| **FilePath**       | `string` | Percorso o identificatore del file all'interno dell'origine scelta.   |

### Esempio (XML)

```xml
<ImportBatchDataOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>IntArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_int_xml.txt</FilePath>
    </Source>
</ImportBatchDataOption>
```

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                   |
|------|-----------------------------|--------------------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante.                             |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione.            |
| 500  | Errore interno del server   | Errore imprevisto nel server.                                |

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifica OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definisce un'interfaccia di programmazione accessibile pubblicamente che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Gli SDK gestiscono i dettagli a basso livello, consentendoti di concentrarti sulla logica di business. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells con diversi SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportBatchData.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}