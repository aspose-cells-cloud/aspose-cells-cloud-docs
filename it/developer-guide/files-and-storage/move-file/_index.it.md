---
title: Sposta file
second_title: Documen
linktitle: Sposta file
type: docs
url: /it/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: Scopri come utilizzare MoveFile API per gestire i file nell'archiviazione cloud Aspose.Cells
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Sposta file, Gestione file, Archiviazione cloud
---
## **Excel API: Sposta file**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Descrizione della funzione**

 IL**spostaFile** API consente di spostare un file da una posizione all'altra all'interno dello storage cloud Aspose.Cells. Questa funzionalità è particolarmente utile per organizzare i file e gestire efficacemente lo storage.

###  I parametri di richiesta di**spostaFile** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|---------------|--|------------------------|--------------------------------------|
| Percorso src| Corda| Sentiero| Percorso di origine del file da spostare.|
| Percorso di destinazione| Corda| Domanda| Percorso di destinazione in cui verrà spostato il file.|
| NomeArchiviazioneSorgente| Corda| Domanda| Nome dell'archivio di origine, se applicabile.|
| NomeArchiviazioneDest| Corda| Domanda|Nome dell'archiviazione di destinazione, se applicabile.|
| ID versione| Corda| Domanda| L'ID della versione del file, se applicabile.|

### **Descrizione della risposta**

```json
{
Void
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:
