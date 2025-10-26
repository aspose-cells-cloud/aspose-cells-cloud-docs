---
title: Copia cartella
second_title: Documen
linktitle: Copia cartella
type: docs
url: /it/copy-folder/
keywords: Excel API, Copy Folder, Office Cloud, REST API, Spreadsheet Management, File Operation
description: Scopri come utilizzare CopyFolder API per copiare in modo efficiente le cartelle nell'ambiente cloud Aspose.Cells
weight: 100
kwords: Excel, Office Cloud, REST API, Copia cartella, Gestione file, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel
---
## **Excel API: Copia cartella**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Descrizione della funzione**

 IL**CopiaCartella**API consente agli utenti di duplicare una cartella esistente all'interno dell'archivio cloud Aspose.Cells. Questa funzionalità è essenziale per gestire i file in modo efficiente, consentendo agli utenti di creare backup o organizzare il proprio lavoro senza dover trasferire manualmente i contenuti.

###  I parametri di richiesta del**CopiaCartella** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|----------------|--|-----------------------|-------------------------------------|
| Percorso src| Corda| Sentiero| Percorso della cartella di origine da copiare.|
| Percorso di destinazione| Corda| Domanda| Il percorso in cui verrà creata la nuova cartella.|
| NomeArchiviazioneSorgente| Corda| Domanda| Nome dell'archivio contenente la cartella di origine.|
| NomeArchiviazioneDest| Corda| Domanda| Nome dell'archivio di destinazione in cui copiare la cartella.|

### **Descrizione della risposta**

```json
{
Void
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK si occupa dei dettagli di basso livello e ti consente di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
