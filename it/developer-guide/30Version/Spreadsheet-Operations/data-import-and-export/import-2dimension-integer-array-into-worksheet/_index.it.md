---
title: "Importa un array bidimensionale di interi in un foglio di calcolo Excel"
second_title: "Documento"
linktitle: "Importa array bidimensionale di interi"
type: docs
url: /import-a-2D-integer-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-integer-array-into-excel-worksheet/,
    /import-2dimension-integer-array-into-worksheet/,
    /import-data/2dimension-integer-array/,
    /import/2dimension-integer-array/,
  ]
keywords: "Aspose.Cells Cloud, importa array 2D di interi, foglio di calcolo Excel, REST API, SDK, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby, Swift"
description: "L'API REST di Aspose.Cells Cloud consente di importare array bidimensionali di interi in fogli di calcolo Excel. Gli SDK sono disponibili per Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift."
weight: 20
---

Questa **REST API importa un array bidimensionale di interi** in un foglio di calcolo Excel.

La richiesta è una richiesta HTTP con contenuto multipart (vedere [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multipart contiene i dati `Import2DimensionIntegerArrayOption`, mentre la seconda parte contiene il file con i dati.

I parametri importanti sono descritti nella tabella seguente:

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Import2DimensionIntegerArrayOption**

| Nome parametro       | Tipo       | Descrizione                                                                                                                                                                                  |
| -------------------- | ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Indice 1‑based della prima riga in cui i dati verranno inseriti.                                                                                                                            |
| FirstColumn          | int        | Indice 1‑based della prima colonna in cui i dati verranno inseriti.                                                                                                                         |
| Data                 | Integer[,] | Array bidimensionale di interi contenente i valori da importare.                                                                                                                               |
| DestinationWorksheet | string     | Nome del foglio di calcolo di destinazione.                                                                                                                                                           |
| IsInsert             | string     | `"true"` per inserire i dati (spostando le celle esistenti), `"false"` per sovrascrivere le celle esistenti.                                                                                                |
| ImportDataType       | string     | Specifica il formato dei dati. Valori supportati: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`. |
| Source               | FileSource | Indica la posizione del file dati quando il parametro `BatchData` è `null`.                                                                                                                   |

### **Esempio**

```json
{
  "Data": [
    [1, 2],
    [3, 4]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 4,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionIntArray"
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

| Codice | Significato                 | Descrizione                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400  | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401  | Non autorizzato             | Token JWT non valido o mancante. |
| 413  | Payload troppo grande       | Il file caricato supera il limite di dimensione. |
| 500  | Errore interno del server   | Errore imprevisto del server. |

## Come usare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiscono un'interfaccia di programmazione pubblicamente accessibile che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzo degli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli di basso livello, permettendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}