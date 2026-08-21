---
title: "Importa array di interi in un foglio di lavoro Excel"
linktitle: "Importa array di interi"
type: docs
url: /import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, importa array di interi, API REST, SDK, C#, PHP, Ruby, Java, Python"
description: "Scopri come importare un array di interi in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include la sintassi della richiesta, i parametri, il codice di esempio per diversi SDK e i dettagli della risposta."
weight: 30
ArticleTitle: "Importa array di interi in un foglio di lavoro Excel – API Aspose.Cells Cloud"
---

Questa REST API importa un array di interi in un foglio di lavoro Excel.

La richiesta deve essere una **POST** HTTP con contenuto multipart (vedi [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del corpo multipart contiene il payload JSON **ImportIntegerArrayOption**, mentre la seconda parte contiene il file di dati sorgente (ad esempio, un file CSV o un file Excel binario).

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Entrambi gli endpoint accettano lo stesso payload multipart. Il primo endpoint esegue un'operazione di importazione generica, mentre il secondo si concentra su un workbook specifico identificato da `{name}`.

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione tramite token JWT</a>.

### **Parametri della richiesta**

### ImportIntegerArrayOption

| Nome parametro           | Tipo       | Descrizione                                                                                                                                                                                    |
| ------------------------ | ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**             | int        | Indice in base zero della prima riga in cui verranno posizionati i dati.                                                                                                                       |
| **FirstColumn**          | int        | Indice in base zero della prima colonna in cui verranno posizionati i dati.                                                                                                                    |
| **IsVertical**           | boolean    | `true` per inserire l’array verticalmente (giù per una colonna); `false` per inserirlo orizzontalmente (attraverso una riga).                                                                  |
| **Data**                 | Integer[]  | L’array di interi da importare.                                                                                                                                                               |
| **DestinationWorksheet** | string     | Nome del foglio di lavoro che riceverà i dati.                                                                                                                                                 |
| **IsInsert**             | boolean    | `true` per inserire righe/colonne prima di scrivere i dati; `false` per sovrascrivere le celle esistenti.                                                                                     |
| **ImportDataType**       | string     | Tipo di dati da importare. Valori validi: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| **Source**               | FileSource | Indica la posizione del file di dati quando il parametro **BatchData** è `null`.                                                                                                              |

#### Esempio di corpo della richiesta

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Risposta

Una richiesta riuscita restituisce **HTTP 200** con un payload JSON simile a:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codici di stato possibili:

| Codice | Significato                              |
| ------ | ---------------------------------------- |
| 200    | Importazione riuscita                    |
| 400    | Richiesta non valida – dati mancanti o non validi |
| 401    | Non autorizzato – token non valido o mancante |
| 500    | Errore interno del server                |

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiscono un'interfaccia di programmazione accessibile pubblicamente e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Gli SDK astraggono i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per l'elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---