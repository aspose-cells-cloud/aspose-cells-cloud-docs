---
title: "Importazione di un Array Double in un Foglio di Lavoro Excel"
second_title: "Documento"
linktitle: "Importazione di array double"
type: docs
url: /it/import-double-array-into-excel-worksheet/
aliases:
  - /import-double-array-into-worksheet/
  - /import-data/double-array/
  - /import/double-array/
keywords: "Aspose.Cells, importazione di array double, API Excel, SDK cloud"
description: "Scopri come importare un array double in un foglio di lavoro Excel utilizzando l'API REST Aspose.Cells Cloud. Include autenticazione, formato della richiesta, parametri, esempi XML/JSON e dettagli sulla risposta."
weight: 20
ArticleTitle: "Importazione di un Array Double in un Foglio di Lavoro Excel – Guida Aspose.Cells Cloud"
---

Questa API REST **importa dati di tipo double-array** in un foglio di lavoro Excel.

> **Prerequisiti:** Prima di chiamare questa API è necessario disporre di un token JWT valido. Per ulteriori informazioni, consultare la guida all'autenticazione.

Invii una richiesta HTTP con contenuto **multipart** (vedere [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) o [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).  
La prima parte del corpo multipart contiene i dati **ImportDoubleArrayOption**, mentre la seconda parte contiene il file dei dati.

## API PostImportData

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l’<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

#### **ImportDoubleArrayOption**

| Nome parametro       | Tipo       | Descrizione                                                                                               |
| -------------------- | ---------- | --------------------------------------------------------------------------------------------------------- |
| FirstRow             | int        | Indice in base zero della prima riga in cui i dati verranno posizionati.                                 |
| FirstColumn          | int        | Indice in base zero della prima colonna in cui i dati verranno posizionati.                              |
| IsVertical           | boolean    | `true` / `false` – determina se l’array viene inserito verticalmente (`true`) o orizzontalmente (`false`). |
| Data                 | Double[]   | Array di valori double da importare.                                                                     |
| DestinationWorksheet | string     | Nome del foglio di lavoro di destinazione.                                                               |
| IsInsert             | boolean    | `true` / `false` – se `true`, i dati vengono inseriti; se `false`, le celle esistenti vengono sovrascritte. |
| ImportDataType       | string     | Tipo di dati da importare (ad esempio, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`). |
| Source               | FileSource | Specifica la posizione del file dei dati quando il parametro `BatchData` è null.                         |

#### Esempio (XML)

```xml
<ImportDoubleArrayOption>
    <DestinationWorksheet>Sheet1</DestinationWorksheet>
    <IsInsert>false</IsInsert>
    <ImportDataType>DoubleArray</ImportDataType>
    <FirstRow>1</FirstRow>
    <FirstColumn>1</FirstColumn>
    <IsVertical>true</IsVertical>
    <Data>1.99,1.9,2.0</Data>
    <Source>
        <FileSourceType>CloudFileSystem</FileSourceType>
        <FilePath>Array_double_xml.txt</FilePath>
    </Source>
</ImportDoubleArrayOption>
```

#### Esempio (JSON)

```json
{
  "Data": [1.99, 1.9, 2.0],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 0,
  "FirstColumn": 0,
  "IsVertical": false,
  "IsInsert": true,
  "ImportDataType": "DoubleArray"
}
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

| Codice | Significato                                    |
| ------ | ---------------------------------------------- |
| 200    | Importazione riuscita                          |
| 400    | Richiesta non valida – dati mancanti o errati |
| 401    | Non autorizzato – token non valido o mancante |
| 500    | Errore interno del server                      |

### Gestione degli errori

Quando si verifica un errore, l'API restituisce un oggetto JSON contenente il codice di errore e un messaggio descrittivo. Esempio per una richiesta non autorizzata:

```json
{
  "Code": 401,
  "Status": "Error"
}
```

Per ulteriori informazioni sulle operazioni di importazione correlate, consulta le pagine della documentazione “Importazione di un Array Double Bidimensionale” e “Importazione di un Array di Interi”.

## Come utilizzare l'API PostImportData con gli SDK

### Specifica dell'API PostImportData

La [Specifica OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzo degli SDK Aspose.Cells Cloud

L'utilizzo di un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli a basso livello e ti consente di concentrarti sulle attività del tuo progetto. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-Double.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}