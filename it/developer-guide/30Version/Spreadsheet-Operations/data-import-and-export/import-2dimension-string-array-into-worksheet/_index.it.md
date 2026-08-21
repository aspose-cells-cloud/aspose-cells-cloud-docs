---
title: "Importa un array di stringhe bidimensionale in un foglio di lavoro Excel"
second_title: "Document"
linktype: "Importa un array di stringhe bidimensionale"
type: docs
url: /import-a-2d-string-array-into-excel-worksheet/
aliases:
  [
    /import-2dimension-string-array-into-excel-worksheet/,
    /import-2dimension-string-array-into-worksheet/,
    /import-data/-2dimension-string-array/,
    /import-data/2dimension-string-array/,
    /import/2dimension-string-array/,
  ]
keywords: "Aspose.Cells Cloud, importa array bidimensionale di stringhe, Excel, API REST, SDK"
description: "Scopri come utilizzare l'API REST di Aspose.Cells Cloud per importare un array di stringhe bidimensionale in un foglio di lavoro Excel. Include il formato della richiesta, i dettagli dei parametri e gli esempi di codice SDK per C#, PHP e Ruby."
weight: 20
---

Questa API REST **importa un array di stringhe bidimensionale** in un foglio di lavoro Excel.

La richiesta è una richiesta HTTP con contenuto multipart (vedere [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). La prima parte del contenuto multipart contiene i dati `Import2DimensionStringArrayOption`, mentre la seconda parte contiene il file dei dati.

## API REST

```bash
POST https://api.aspose.cloud/v3.0/cells/import
POST https://api.aspose.cloud/v3.0/cells/{name}/importdata
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

I parametri importanti sono descritti nella tabella seguente:

### **Import2DimensionStringArrayOption**

| Nome parametro       | Tipo                | Descrizione                                                                           |
| -------------------- | ------------------- | ------------------------------------------------------------------------------------- |
| FirstRow             | int                 | Indice in base zero della riga da cui inizia l'importazione.                         |
| FirstColumn          | int                 | Indice in base zero della colonna da cui inizia l'importazione.                      |
| Data                 | String[,]           | Array bidimensionale contenente i valori di stringa da importare.                    |
| DestinationWorksheet | string              | Nome del foglio di lavoro che riceverà i dati importati.                             |
| IsInsert             | string (true/false) | Se **true**, i dati vengono inseriti e le celle esistenti vengono spostate di conseguenza. |
| ImportDataType       | string              | Specifica il tipo di dati; per questa operazione utilizzare `TwoDimensionStringArray`. |
| Source               | FileSource          | Indica la posizione del file dei dati quando il parametro `BatchData` è null.        |

### Corpo della richiesta di esempio

```json
{
  "Data": [
    ["1.0", "2.9"],
    ["2.0", "2.1"]
  ],
  "DestinationWorksheet": "Sheet2",
  "FirstRow": 1,
  "FirstColumn": 1,
  "ImportDataType": "TwoDimensionStringArray"
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
| 400    | Richiesta non valida        | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato             | Token JWT non valido o mancante.                                            |
| 413    | Payload troppo grande       | Il file caricato supera il limite di dimensione.                           |
| 500    | Errore interno del server   | Errore imprevisto del server.                                               |

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/DataProcessing/PostImportData) definiscono un'interfaccia di programmazione pubblicamente accessibile che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per integrare questa funzionalità. Un SDK astrae i dettagli a basso livello, consentendoti di concentrarti sulla logica aziendale. Consulta la [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-2String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}