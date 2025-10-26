---
title: Copia file - Excel AP
second_title: Documen
linktitle: Copia file
type: docs
url: /it/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Scopri come utilizzare CopyFile API per Excel per duplicare in modo efficiente fogli di calcolo e gestire vari formati di file
weight: 100
kwords: Excel API, Office Cloud, REST API, Copia foglio di calcolo, PDF Conversione, Esportazione CSV, Gestione JSON, Supporto Markdown, Copia file Excel, Corrispondenza cella vuota
---
## **Excel API: Copia file**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Descrizione della funzione**

 IL**copiaFile** API consente agli utenti di duplicare un file Excel da un percorso di origine specificato a un percorso di destinazione, supportando varie opzioni di archiviazione.

###  I parametri di richiesta di**copiaFile** API sono

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP|Descrizione|
|-------------- ||--------------------- |-------------------------------------- |
| Percorso src| Corda| Sentiero| Percorso di origine del file da copiare.|
| Percorso di destinazione| Corda| Domanda| Percorso di destinazione in cui verrà salvato il file.|
| NomeArchiviazioneSorgente| Corda| Domanda| Nome dell'archivio di origine.|
| NomeArchiviazioneDest| Corda| Domanda| Nome dell'archivio di destinazione.|
| ID versione| Corda| Domanda| ID versione facoltativo del file da copiare.|

### **Descrizione della risposta**

```json
{
Void
}
```

## Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/FileController/CopyFile) definisce un'interfaccia di programmazione accessibile al pubblico e consente di eseguire interazioni REST direttamente da un browser web.

## Excel API SDK

 Utilizzare un SDK è il modo migliore per accelerare lo sviluppo. Un SDK gestisce i dettagli di basso livello, consentendoti di concentrarti sulle attività del progetto. Dai un'occhiata a[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come effettuare chiamate ai servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
