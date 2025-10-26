---
title: Elimina cartella
second_title: Documen
linktitle: Elimina cartella
type: docs
url: /it/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: Scopri come eliminare una cartella in Aspose.Cells utilizzando deleteFolder API, inclusi parametri ed esempi di codice
weight: 100
kwords: Excel API, Office Cloud, REST API, Gestione fogli di calcolo, PDF, CSV, JSON, Markdown, elimina cartella nel foglio di lavoro Excel
---
## **Excel API : Elimina cartella**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Descrizione della funzione**

`deleteFolder` API consente agli utenti di rimuovere una cartella specificata dall'archiviazione cloud associata a Aspose.Cells. Questa funzionalità può essere utile per mantenere l'organizzazione e gestire efficacemente l'archiviazione.

###  I parametri di richiesta di**eliminaCartella** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
| sentiero| Corda| Sentiero| Percorso della cartella da eliminare.|
| Nome di archiviazione| Corda| Domanda| Nome dell'archivio in cui si trova la cartella.|
| ricorsivo| Booleano| Domanda| Indica se l'eliminazione deve essere ricorsiva, rimuovendo anche tutto il contenuto all'interno della cartella.|

### **Descrizione della risposta**

```json
{
Void
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
