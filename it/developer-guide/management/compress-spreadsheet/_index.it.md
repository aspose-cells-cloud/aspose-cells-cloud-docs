---
title: Aspose.Cells Cloud Web API - Comprimi le dimensioni del foglio di calcolo
second_title: Documen
ArticleTitle: Compress the size of the Spreadshee
linktitle: Comprimi foglio di calcolo
type: docs
url: /it/compress-spreadsheet/
keywords: Spreadsheet Compression, Reduce File Size, Aspose.Cells Cloud Web AP
description: Compress Spreadsheet API consente agli utenti di ridurre in modo efficiente le dimensioni dei file dei fogli di calcolo applicando livelli di compressione specificati, ottimizzando l'archiviazione e migliorando le prestazioni
weight: 100
kwords: Excel, Office Cloud, REST, Compressione fogli di calcolo, Ottimizzazione dimensioni file, PDF, CSV, Json, Markdow
---
Comprimi le dimensioni del foglio di calcolo.

## **Comprimi foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo da comprimere.|
|livello|Intero|Domanda|Specifica il livello di compressione da applicare, che va da 0 (nessuna compressione) a 9 (compressione massima).|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Percorso della cartella in cui verrà archiviata la cartella di lavoro compressa. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome di archiviazione del file di output.|
|regione|Corda|Domanda|Impostazione della regione del foglio di calcolo.|
|password|Corda|Domanda|La password richiesta per aprire il file del foglio di calcolo.|

### **Risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo usare il foglio di calcolo Compress API?

Quando hai bisogno di ridurre le dimensioni dei fogli di calcolo, puoi usare questo API.

## Perché dovresti usare Compress Spreadsheet API?

- Il foglio di calcolo è troppo grande ed è necessario ridurne le dimensioni.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare il foglio di calcolo compresso API con gli SDK

### Specifiche di Comprimi foglio di calcolo API

 IL[Specifiche di Comprimi foglio di calcolo API](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet) fornisce un'interfaccia accessibile al pubblico per le interazioni REST, consentendo chiamate dirette API da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo più rapido per sviluppare, poiché astrae i dettagli di basso livello, consentendo di comprimere le dimensioni del foglio di calcolo con codice breve.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice mostrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
