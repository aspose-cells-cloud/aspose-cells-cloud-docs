---
title: Aspose.Cells Cloud Web API - Proteggi foglio di calcolo
second_title: Developer Guide for Excel Protectio
ArticleTitle: Protect the Spreadsheet with passwor
linktitle: Proteggi foglio di calcolo
type: docs
url: /it/protect-spreadsheet/
keywords: Aspose.Cells Cloud Web API, password protection, encrypt spreadsheet, modify passwor
description: Questo API applica una protezione con password a doppio strato ai fogli di calcolo Excel, garantendo un accesso e una modifica sicuri tramite crittografia
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, protezione con password a doppio livello, crittografia foglio di calcolo, Exce sicuro
---
Applica la protezione tramite password ai fogli di calcolo Excel, supportando sia le password di apertura che quelle di modifica.

## **Proteggi foglio di calcolo API**

```http
PUT http://api.aspose.cloud/v4.0/cells/protection/spreadsheet
```

### **Parametri di richiesta:**

| Nome del parametro| Tipo| Percorso/Stringa di query/Corpo HTTP| Descrizione|
|:- |:- |:- |:- |
|Foglio di calcolo|File|FormData|Carica il file del foglio di calcolo da proteggere.|
|password|Corda|Domanda|Password di crittografia per il file del foglio di calcolo.|
|modificaPassword|Corda|Domanda|Password richiesta per modificare il foglio di calcolo.|
|Percorso in uscita|Corda|Domanda|(Facoltativo) Percorso della cartella in cui verrà archiviata la cartella di lavoro protetta. Il valore predefinito è null.|
|outStorageName|Corda|Domanda|Nome dell'archivio per i file di output.|
|regione|Corda|Domanda|Definisce le impostazioni regionali per il foglio di calcolo.|

## **Risposta**

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

## Dove dovremmo usare Protect Spreadsheet API?

Quando hai bisogno di bloccare un foglio di calcolo con una password, puoi usare questo API.

## Perché dovresti usare Protect Spreadsheet API?

- Blocca rapidamente i fogli di calcolo con password.
- Lo sviluppo può essere completato rapidamente tramite l'SDK esistente.

## Come utilizzare Protect Spreadsheet API con gli SDK

### Specifiche OpenAPI

 IL[Specifiche OpenAPI](https://reference.aspose.cloud/cells/#/ProtectionController/ProtectSpreadsheet)fornisce un'interfaccia di programmazione dettagliata per eseguire interazioni REST direttamente da un browser web.

### Utilizzare gli SDK cloud Aspose.Cells

Utilizzare l'SDK è il modo migliore per accelerare lo sviluppo. L'SDK gestisce i dettagli sottostanti, consentendo di implementare in modo semplice la protezione dei fogli di calcolo per le celle con un codice minimo.
 Si prega di controllare il[Repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo di Aspose.Cells Cloud SDK.

I seguenti esempi di codice illustrano come interagire con i servizi Web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ProtectSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ProtectSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ProtectSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ProtectSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ProtectSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ProtectSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ProtectSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ProtectSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
