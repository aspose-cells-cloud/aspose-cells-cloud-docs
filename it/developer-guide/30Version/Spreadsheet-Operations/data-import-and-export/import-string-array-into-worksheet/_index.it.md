---
title: "Importa array di stringhe in un foglio di lavoro Excel – Aspose.Cells Cloud"
second_title: "Document"
linktype: "Importa array di stringhe"
type: docs
url: /import-string-array-into-excel-worksheet/
aliases:
  - /import-string-array-into-worksheet/
  - /import-data/string-array/
  - /import/string-array/
keywords: "Aspose.Cells Cloud, importa array di stringhe, API REST Excel, upload multipart, importazione dati nel foglio di lavoro, SDK cloud"
description: "Scopri come importare un array di stringhe in un foglio di lavoro Excel utilizzando l'API REST di Aspose.Cells Cloud (v3.0). Include il formato della richiesta, i parametri e gli esempi di SDK."
weight: 40
ArticleTitle: "Importa array di stringhe in un foglio di lavoro Excel – Aspose.Cells Cloud"
---

Importare un array di stringhe in un foglio di lavoro Excel è un'operazione comune quando si popolano fogli elettronici con dati strutturati in elenco. Questa operazione risulta utile in scenari come il caricamento di valori di configurazione, il trasferimento di dati da fonti esterne o l'inizializzazione di fogli di lavoro con raccolte predefinite di stringhe.

**Prerequisiti:**  
- Un token JWT valido ottenuto tramite il flusso di autenticazione di Aspose.Cells Cloud.  
- Un foglio di lavoro esistente (o la capacità di crearne uno) nella memoria di Aspose Cloud.  
- La versione appropriata dell'SDK che supporta il modello `ImportStringArrayOption`.

Questa API REST importa dati di tipo array di stringhe in un foglio di lavoro Excel.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'[autenticazione basata su token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### **Parametri della richiesta**

La richiesta utilizza contenuto HTTP multipart (vedi [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La prima parte del corpo multipart contiene un payload **ImportStringArrayOption**; la seconda parte contiene il file sorgente dei dati.

I parametri importanti sono descritti nella tabella seguente:

<caption>Parametri di ImportStringArrayOption</caption>
### **ImportStringArrayOption**

| Nome parametro       | Tipo       | Descrizione                                                                                                                                                              |
| -------------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| FirstRow             | int        | L'indice della riga iniziale (1-based) in cui verranno inseriti i dati.                                                                                                  |
| FirstColumn          | int        | L'indice della colonna iniziale (1-based) in cui verranno inseriti i dati.                                                                                               |
| IsVertical           | boolean    | `true` per inserire i dati verticalmente; `false` per inserirli orizzontalmente.                                                                                         |
| Data                 | String[]   | L'array di stringhe da importare.                                                                                                                                        |
| DestinationWorksheet | string     | Il nome del foglio di lavoro che riceverà i dati.                                                                                                                        |
| IsInsert             | boolean    | `true` per inserire righe/colonne (spostando le celle esistenti); `false` per sovrascrivere le celle esistenti.                                                         |
| ImportDataType       | string     | Tipo di dati da importare (ad esempio `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`). |
| Source               | FileSource | Descrive la posizione del file di dati quando **BatchData** è null (ad esempio `CloudFileSystem`, `LocalFile`). Obbligatorio se `BatchData` non è fornito.              |

### Esempio

```xml
<ImportStringArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>StringArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_string_xml.txt</FilePath>
    </Source>
</ImportStringArrayOption>
```

### Risposta

Una richiesta riuscita restituisce **HTTP 200** con un payload JSON simile al seguente:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Codici di stato possibili:

| Codice | Significato                                  |
| ------ | -------------------------------------------- |
| 200    | Importazione riuscita                        |
| 400    | Richiesta non valida – dati mancanti o errati |
| 401    | Non autorizzato – token non valido o mancante |
| 500    | Errore interno del server                    |


## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifiche OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiscono un'interfaccia di programmazione pubblicamente accessibile e consentono di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per velocizzare lo sviluppo. Un SDK gestisce i dettagli a basso livello, consentendoti di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web di Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-String.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}