---
title: "Come unire più file di fogli di calcolo con Aspose.Cells Cloud"
linktype: "Come unire più file di fogli di calcolo"
type: docs
url: /it/how-to-merge-multiple-files
description: "Come unire più file di fogli di calcolo con Aspose.Cells Cloud."
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, JSON, Markdown, Come unire più file tramite Aspose.Cells Cloud
---

## Introduzione

L'API Aspose.Cells Cloud è una soluzione basata sul cloud potente, progettata per la creazione, la modifica e la conversione di file di fogli di calcolo. In questo articolo ti guideremo attraverso il processo di utilizzo dell'API Aspose.Cells Cloud per l’unione di file in diversi formati, inclusi casi d’uso tipici e codice di esempio.

## Panoramica

L'API Aspose.Cells Cloud fornisce API robuste per unire più file di fogli di calcolo in un unico file in vari formati. I formati supportati includono **Excel** (XLS, XLSX), **CSV**, **HTML**, **PDF** e altri. Utilizzando l'API Aspose.Cells Cloud, puoi facilmente unire più file di fogli di calcolo in un unico file nei formati più diffusi, soddisfacendo esigenze molto varie.

Sono disponibili numerose API per l’unione dei file, generalmente compatibili con diversi ambienti online. Di seguito una descrizione dettagliata di tali API:

| Funzione | Descrizione | Riferimento API |
| :------------------------- | :------------------------- | :------------------------- |
| **[MergeSpreadsheets](https://docs.aspose.cloud/cells/merge-spreadsheets/)** | Unisce file di fogli di calcolo locali in un file in un formato specificato. | [MergeSpreadsheets](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheets) |
| **[MergeRemoteSpreadsheet](https://docs.aspose.cloud/cells/merge-remote-spreadsheet/)** | Unisce file di fogli di calcolo presenti in una cartella dello storage cloud in un file in un formato specificato. | [Merge Remote Spreadsheet](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeRemoteSpreadsheet) |
| **[Merge Spreadsheets In Remote Folder](https://docs.aspose.cloud/cells/merge-spreadsheets-in-remote-folder/)** | Unisce file di fogli di calcolo presenti in una cartella dello storage cloud in un file in un formato specificato. | [Merge Spreadsheets In Remote Folder](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/MergeSpreadsheetsInRemoteFolder) |

# Come unire più file in un unico file tramite Aspose.Cells Cloud

L'API Aspose.Cells Cloud fornisce [diversi SDK](https://github.com/aspose-cells-cloud) per diversi linguaggi di programmazione. Scegli l’SDK corrispondente al linguaggio di programmazione che preferisci e segui la documentazione accompagnatoria per l’installazione e l’inizializzazione. In alternativa, puoi creare il tuo SDK in base al [riferimento API](https://reference.aspose.cloud/cells/). In questa sezione, utilizzeremo C# come esempio per descrivere nel dettaglio il processo di unione dei file.

## Registrazione e ottenimento della chiave API

Prima di iniziare, devi [registrare un account Aspose Cloud](https://id.containerize.com/signup) e [ottenere una chiave API per l'autenticazione](https://dashboard.aspose.cloud/applications). Accedendo al sito ufficiale di Aspose Cloud, puoi creare un account gratuito e ottenere una chiave API da utilizzare per l’autenticazione.

Per operazioni più avanzate, fai riferimento ai seguenti documenti: [Avvio rapido con Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)

## Installazione e inizializzazione dell'SDK Aspose.Cells Cloud

Installa il pacchetto NuGet Aspose.Cells-Cloud nel tuo progetto .NET, utilizzando la Console di Gestione Pacchetti o il Gestore Pacchetti NuGet in Visual Studio.
Ecco come installare il pacchetto tramite la Console di Gestione Pacchetti:

```Powershell

Install-Package Aspose.Cells-Cloud

```

Crea una nuova istanza della classe CellsApi, inizializzandola con il tuo client ID e client secret. Di seguito i dettagli del frammento di codice precedente:

```CSharp

CellsApi cellsInstance = new CellsApi(clientID, clientSecret);

```

Assicurati di sostituire YOUR_API_KEY, YOUR_APP_SID e YOUR_APP_KEY con la tua chiave API, l’application SID e l’application key effettivi.

## Costruire la richiesta API e richiamare l’API

### Utilizzare i servizi cloud per unire fogli di calcolo locali e consegnare i file uniti, come output locali o come stream in memoria, in qualsiasi formato richiesto

```CSharp

using System.Collections.Generic;

var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));

// Costruisci la richiesta di unione dei fogli di calcolo
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsRequest();
// Imposta i file da unire.
IDictionary<string, System.IO.Stream> mapFiles = new Dictionary<string, System.IO.Stream>();
mapFiles.Add("Book1.xlsx", File.OpenRead("Book1.xlsx"));
mapFiles.Add("Book2.xlsx", File.OpenRead("Book2.xlsx"));
request.Spreadsheet = mapFiles;
// Imposta il formato di output
request.outFormat = "pdf";

cellsApi.MergeSpreadsheets(request, "MergedResultFile.pdf");

```

### Unione in cloud di fogli di calcolo memorizzati nel cloud e consegna del file unito, in locale o nuovamente nello storage cloud, in qualsiasi formato richiesto

```C#
// Ottieni il tuo Client ID e Client Secret da https://dashboard.aspose.cloud (è richiesta una registrazione gratuita).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Costruisci i parametri della richiesta di unione
var request = new Aspose.Cells.Cloud.SDK.Request.MergeRemoteSpreadsheetRequest();
// Imposta il file principale nel cloud
request.name = "Book1.xlsx";
request.folder = "RemoteFolder1";
// Imposta il file da unire nel cloud
request.mergedSpreadsheet = "RemoteFolder2/Book2.xlsx";
request.outFormat = "pdf";
cellsApi.MergeRemoteSpreadsheet(request, "MergedResultOutPutToLocalFile.pdf");
```

### Unione automatica dei file corrispondenti in una directory cloud, esportazione del risultato unito nel formato specificato e consegna in locale o nuovamente nello storage cloud

```csharp
// Ottieni il tuo Client ID e Client Secret da https://dashboard.aspose.cloud (è richiesta una registrazione gratuita).
var cellsApi = new Aspose.Cells.Cloud.SDK.Api.CellsApi(System.Environment.GetEnvironmentVariable("ProductClientId"), System.Environment.GetEnvironmentVariable("ProductClientSecret"));
// Costruisci i parametri della richiesta di unione
var request = new Aspose.Cells.Cloud.SDK.Request.MergeSpreadsheetsInRemoteFolderRequest();
// Cartella di archiviazione i cui file devono essere uniti
request.folder = "RemoteFolder";
request.fileMatchExpression = "*xlsx$";
request.outFormat = "pdf";
cellsApi.MergeSpreadsheetsInRemoteFolder(request, "MergedResultOutPutToLocalFile.pdf");
```

## Casi d’uso

La funzionalità di **unione** di più file dell’API Aspose.Cells Cloud è utile in diversi scenari pratici. Di seguito alcuni scenari comuni:

- **Unire più file Excel in un unico file Excel** per l’analisi e l’archiviazione dei dati.
- **Unire file di dati in un unico file Excel** per l’analisi dei dati.
- **Unire più file immagine in un file PDF** per una condivisione agevole.
- **Unire più file in un unico file HTML** per la visualizzazione e l’integrazione nelle pagine web.

## Conclusione

Con l'API Aspose.Cells Cloud puoi facilmente effettuare l’unione di più file di fogli di calcolo in un unico file. Effettuando semplici chiamate API e impostando le opzioni di unione appropriate, puoi soddisfare in modo efficiente diverse esigenze di unione dei file. Integra l'API Aspose.Cells Cloud nelle tue applicazioni per migliorare la produttività e risparmiare tempo nello sviluppo.

Si ricorda che il codice di esempio riportato sopra ha solo scopo dimostrativo e, nell’uso pratico, dovrai sostituirlo con credenziali di autenticazione valide e percorsi di file corretti. Inoltre, l’API Aspose.Cells Cloud offre molte altre funzionalità, tra cui creazione, modifica, manipolazione e elaborazione dei dati dei fogli di calcolo. La documentazione dettagliata dell’API e il codice di esempio sono disponibili nella [guida per sviluppatori del sito ufficiale di Aspose](/developer-guide/).

Speriamo che questo articolo ti aiuti a comprendere come utilizzare l’API Aspose.Cells Cloud per l’unione dei file. Buona fortuna con la tua implementazione!