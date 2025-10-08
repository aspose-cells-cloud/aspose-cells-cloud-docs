---
title: Elimina file - Excel AP
second_title: Documen
linktitle: Elimina file
type: docs
url: /it/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: Scopri come eliminare i file in Excel utilizzando Aspose.Cells API. Questa guida fornisce informazioni dettagliate sull'endpoint deleteFile API, sui parametri di richiesta e sulla struttura di risposta
weight: 100
kwords: Elimina file, Excel API, REST API, Office Cloud, Gestione fogli di calcolo, Eliminazione file, Archiviazione cloud, API usag
---
## **Excel API : Elimina file**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Descrizione della funzione**

 IL**eliminaFile** API consente agli utenti di rimuovere file specifici dall'archiviazione cloud, garantendo una gestione efficiente delle risorse e dei dati.

###  I parametri di richiesta per il**eliminaFile** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|sentiero|Corda|Sentiero|Il percorso del file che deve essere eliminato.|
|Nome di archiviazione|Corda|Domanda|Nome dell'archivio in cui si trova il file. Facoltativo se si utilizza l'archivio predefinito.|
|ID versione|Corda|Domanda|ID della versione del file da eliminare, se applicabile.|

### **Descrizione della risposta**

```json
{
Void
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
