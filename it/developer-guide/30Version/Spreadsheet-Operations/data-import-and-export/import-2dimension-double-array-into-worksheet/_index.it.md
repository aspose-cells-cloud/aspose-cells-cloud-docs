---
title: "Importa un array bidimensionale di doppi in un foglio di lavoro Excel"
second_title: "Documento"
linktype: "Importa un array bidimensionale di doppi"
type: docs
url: /it/import-a-2D-double-array-into-excel-worksheet/
aliases:
  [
    "/import-2dimension-double-array-into-excel-worksheet/",
    "/import-2dimension-double-array-into-worksheet/",
    "/import-data/2dimension-double-array/",
    "/import/2dimension-double-array/",
  ]
keywords: "Importa array bidimensionale di doppi, Excel, Aspose Cells Cloud, API REST, Foglio di calcolo, Importazione dati"
description: "Scopri come importare un array bidimensionale di doppi in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud. Include il formato della richiesta, i parametri e esempi di codice SDK."
weight: 20
---

Questa API REST **importa un array bidimensionale di doppi** in un foglio di lavoro Excel.

La richiesta è un HTTP `POST` con contenuto multipart (vedi [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del corpo multipart contiene i dati **Import2DimensionDoubleArrayOption**, mentre la seconda parte contiene il file dei dati di origine.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

I parametri importanti sono descritti nella tabella seguente:

### Import2DimensionDoubleArrayOption

| Nome parametro         | Tipo         | Descrizione                                                                                                             |
| ---------------------- | ------------ | ----------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**           | `int`        | Indice di riga (1-based) in cui inizia l'importazione.                                                                  |
| **FirstColumn**        | `int`        | Indice di colonna (1-based) in cui inizia l'importazione.                                                               |
| **Data**               | `Double[,]`  | Array bidimensionale di valori doppi da importare.                                                                      |
| **DestinationWorksheet**| `string`    | Nome del foglio di lavoro che riceverà i dati.                                                                          |
| **IsInsert**           | `string`     | `"true"` per inserire righe, `"false"` per sovrascrivere le celle esistenti.                                            |
| **ImportDataType**     | `string`     | Tipo di dati in fase di importazione (es. `IntArray`, `DoubleArray`, `TwoDimensionDoubleArray`, `BatchData`, `csvData`, ecc.). |
| **Source**             | `FileSource` | Indica la posizione del file dati quando il parametro `BatchData` è null.                                               |

**Esempio**

```json
{
  "Data": [
    [1.0, 2.9, 3.1],
    [2.0, 2.1, 3.1]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "importDataType": "TwoDimensionDoubleArray"
}
```

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di stato HTTP**

| Codice | Significato                 | Descrizione                                                                 |
|--------|-----------------------------|-----------------------------------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida        | Parametri mancanti o non validi (es. tipo di file non supportato).         |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                           |
| 500    | Errore interno del server   | Errore imprevisto sul server.                                               |

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiscono un'interfaccia di programmazione pubblicamente accessibile che consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Gli SDK gestiscono i dettagli di basso livello, permettendoti di concentrarti sulla logica di business. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}