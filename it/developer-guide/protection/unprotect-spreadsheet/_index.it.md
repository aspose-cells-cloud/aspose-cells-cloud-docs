---
title: Aspose.Cells Cloud Web API - Sproteggi foglio di calcolo con password
second_title: Documen
ArticleTitle: Unprotect the Spreadsheet with passwor
linktitle: Rimuovi protezione foglio di calcolo
type: docs
url: /it/unprotect-spreadsheet/
keywords: Excel API, Unprotect Spreadsheet, Password Removal, Encryption, Office Cloud, REST API, Spreadsheet Security, Excel File Managemen
description: Rimuove in modo efficiente la protezione con password a doppio strato dai fogli di calcolo Excel, supportando sia l'apertura che la modifica delle password con tecniche di crittografia avanzate
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Abbina tutte le celle vuote in un foglio di lavoro Excel
---
Applica la protezione dei fogli di calcolo Excel con password, supportando sia le password di apertura che di modifica.

## **Rimuovi protezione foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/unprotection/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Caricare il file del foglio di calcolo da non proteggere.|
|password|Corda|Domanda|La password di crittografia per il file del foglio di calcolo.|
|modificaPassword|Corda|Domanda|La password richiesta per modificare il file protetto.|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Percorso della cartella in cui verrà archiviata la cartella di lavoro non protetta. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Specifica il nome di archiviazione del file di output.|
|regione|Corda|Domanda|Definisce le impostazioni della regione del foglio di calcolo.|

### **Risposta**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Codici di errore

- **400 Richiesta non valida**: URI Apose.Cells Cloud API non valido.
- **401 Non autorizzato**: Token di accesso non valido. Oppure ID client e segreto non validi.
- **404 Non trovato**: Il file del foglio di calcolo non è accessibile.
- **Errore del server 500**: Il foglio di calcolo ha riscontrato un'anomalia nell'ottenimento dei dati di calcolo.

## Dove dovremmo usare l'opzione Elimina colonne vuote del foglio di calcolo API?

Quando è necessario trasformare i dati, è possibile utilizzare questo API.

## Perché dovresti usare Elimina colonne vuote del foglio di calcolo API?

- Elimina rapidamente tutte le colonne vuote che non contengono dati o altri oggetti da un foglio di calcolo Excel.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare l'opzione Elimina colonne vuote del foglio di calcolo API con gli SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/UnprotectSpreadsheet) definisce un'interfaccia di programmazione accessibile al pubblico, che consente di eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice l'eliminazione delle colonne vuote per le celle dei fogli di calcolo con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come chiamare i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UnprotectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UnprotectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UnprotectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UnprotectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UnprotectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UnprotectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UnprotectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UnprotectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
