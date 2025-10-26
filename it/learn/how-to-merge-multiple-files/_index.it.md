---
title: Come unire più file di fogli di calcolo con Aspose.Cells Clou
linktitle: Come unire più file di fogli di calcolo
type: docs
url: /it/how-to-merge-multiple-files
description: Come unire più file di fogli di calcolo con Aspose.Cells Cloud
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Come unire più file tramite Aspose.Cells Cloud
---
## Introduzione

Aspose.Cells Cloud API è una potente soluzione basata su cloud pensata per la creazione, la modifica e la conversione di file di fogli di calcolo. In questo articolo, vi guideremo attraverso il processo di utilizzo di Aspose.Cells Cloud API per l'unione di formati di file, includendo casi d'uso tipici e codice di esempio.

## Panoramica

 Il Cloud Aspose.Cells API fornisce API robuste per unire più file di fogli di calcolo in un unico file con diversi formati. I formati supportati includono**Excel** (XLS, XLSX),**CSV**, **HTML**, **PDF**e altro ancora. Sfruttando il Cloud Aspose.Cells API, puoi unire senza sforzo più file di fogli di calcolo in un unico file con formati ampiamente utilizzati, soddisfacendo una vasta gamma di esigenze.

Sono disponibili numerose API per l'unione di file, generalmente compatibili con vari ambienti online. Di seguito una descrizione dettagliata di queste API:

| Funzione| Descrizione| API Riferimento|
|:------------------------- |:------------------------- |:------------------------- |
|**[Unisci fogli di calcolo](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Unisci i file di fogli di calcolo locali in un file di formato specificato.|[Unisci fogli di calcolo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
|**[UnisciFoglioDiSpreadRemoto](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Unisci i file dei fogli di calcolo nella cartella dell'archiviazione cloud in un file di formato specificato.|[Unisci foglio di calcolo remoto](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
|**[Unisci fogli di calcolo in cartella remota](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Unisci i file dei fogli di calcolo nella cartella dell'archiviazione cloud in un file di formato specificato.|[Unisci fogli di calcolo nella cartella remota](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Come unire più file tramite Aspose.Cells Cloud

 Il Cloud Aspose.Cells fornisce[più SDK](https://github.com/aspose-cells-cloud)per diversi linguaggi di programmazione. Scegli l'SDK più adatto al tuo linguaggio di programmazione preferito e segui la documentazione allegata per l'installazione e l'inizializzazione. In alternativa, puoi creare il tuo SDK in base alle[API riferimento](https://reference.aspose.cloud/cells/)In questa sezione useremo C# come esempio per descrivere in dettaglio il processo di unione dei file.

## Registrazione e ottenimento della chiave API

 Prima di iniziare, è necessario[registra un account Cloud Aspose](https://id.containerize.com/signup) E[ottenere una chiave API per l'autenticazione](https://dashboard.aspose.cloud/applications)Accedendo al sito web ufficiale Aspose Cloud, puoi creare un account gratuito e ottenere una chiave API per l'autenticazione.

 Per operazioni più approfondite, fare riferimento ai seguenti documenti:[Avvio rapido con Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installazione e inizializzazione del Cloud SDK Aspose.Cells

Installa il pacchetto Aspose.Cells-Cloud NuGet nel tuo progetto .NET, puoi utilizzare la console di gestione pacchetti NuGet o il gestore pacchetti NuGet in Visual Studio.
Ecco come puoi installare il pacchetto utilizzando la console di Package Manager:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Crea una nuova istanza della classe CellsApi, inizializzandola con il tuo ID client e il tuo segreto client. Di seguito sono riportati i dettagli del frammento di codice sopra menzionato:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Assicurati di sostituire il TUO_API_CHIAVE, LA TUA_APP_SID e IL TUO_APP_CHIAVE con la tua chiave API effettiva, SID dell'applicazione e chiave dell'applicazione.

## Compila la richiesta API e chiama lo API

### Sfrutta i servizi cloud per unire fogli di calcolo locali e fornire i file consolidati, come output locali o flussi in memoria, in qualsiasi formato richiesto

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Suild merged spreadsheet request
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Set need merged files.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Set output format
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Unisci i fogli di calcolo archiviati nel cloud e distribuisci il file consolidato, localmente o di nuovo nell'archiviazione cloud, in qualsiasi formato richiesto

```C#
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Set cloud main file
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Set cloud merged file
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Unisci automaticamente i file corrispondenti in una directory cloud, esporta il risultato consolidato nel formato specificato e consegnalo localmente o di nuovo all'archiviazione cloud

```csharp
// Get your Client ID and Client Secret from https://dashboard.aspose.cloud (free registration is required).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Build merge request parameters 
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Storage directory that needs to merge files
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Casi d'uso

 I file multipli**unito** La funzionalità Aspose.Cells Cloud API è utile in vari casi d'uso pratici. Ecco alcuni scenari comuni:

- **Unisci più file Excel in un file Excel** per l'analisi e l'archiviazione dei dati.
- **Unisci i file di dati in un file Excel** per l'analisi dei dati.
- **Unisci più file di immagini in un file PDF** per una facile condivisione.
- **Unisci più file in un file html** per la visualizzazione e l'incorporamento nelle pagine web.

## Conclusione

Con Aspose.Cells Cloud API, puoi facilmente eseguire l'unione di più file di fogli di calcolo in un unico file. Eseguendo semplici chiamate API e impostando le opzioni di unione appropriate, puoi soddisfare in modo efficiente diversi requisiti di unione di file. Integra Aspose.Cells Cloud API nelle tue applicazioni per migliorare la produttività e risparmiare tempo di sviluppo.

 Si prega di notare che il codice di esempio sopra riportato è solo a scopo dimostrativo e sarà necessario sostituirlo con credenziali di autenticazione e percorsi di file validi quando lo si utilizza nella pratica. Inoltre, Aspose.Cells Cloud API offre molte altre funzionalità, come la creazione, la modifica, la manipolazione e l'elaborazione dei dati di fogli di calcolo. La documentazione dettagliata e il codice di esempio di API sono disponibili su[guida per gli sviluppatori del sito web ufficiale Aspose](/developer-guide/).

Ci auguriamo che questo articolo ti aiuti a capire come utilizzare Aspose.Cells Cloud API per l'unione di file. In bocca al lupo per l'implementazione!
