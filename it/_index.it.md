---
title: "Aspose.Cells Cloud Web: archiviazione cloud, conversione di fogli di calcolo, unione, suddivisione, protezione, elaborazione dati e altro ancora"
second_title: Documen
ArticleTitle: "Aspose.Cells Cloud Web: Cloud storage, Spreadsheet conversion, merged, splitting, protecting, data processing, and mor"
linktitle: Centro sviluppatori
type: docs
url: /it/
description: Aspose.Cells Le API Web Cloud supportano Spreadsheet/Excel per creare, convertire, unire, dividere, proteggere ed eseguire operazioni sugli oggetti interni, tra le altre funzioni. Aspose.Cells Cloud fornisce un documento completo, supporta interfacce RESTful ed esempi di codice per aiutare gli sviluppatori a integrare rapidamente
weight: 10
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Aspose.Cells Documento Cloud
---
## Che cosa sono le API cloud Aspose.Cells?

Le API cloud Aspose.Cells sono un set di servizi cloud Spreadsheet/Excel: non è necessario installare Office, non è necessario configurare i server, basta inviare una richiesta HTTP e potrai eseguire tutte le operazioni comuni come creazione, modifica, conversione di formato, pulizia dei dati, grafici, tabelle pivot, crittografia, suddivisione, unione, filigrane, firme digitali, ecc., ovunque e in qualsiasi lingua.

## Perché utilizzare le API cloud Aspose.Cells?

- Creazione, modifica, conversione e analisi di fogli di calcolo nell'archiviazione cloud basata sui servizi Cloud Web Aspose.Cells.
- Crea, modifica, converti e analizza file di fogli di calcolo locali basati sui servizi Cloud Web Aspose.Cells API.
- I formati di file supportati sono 30, come xlsx, csv, ods, xlsb, ecc.
- Gestisci i fogli di calcolo direttamente tramite Aspose.Cells Cloud Web API senza la necessità di dipendenze Microsoft Excel.
- 150 chiamate gratuite al mese al numero API.
- Addebito graduale: quanto consumano gli utenti, quanto addebitano, più consumano, più sconti offrono.
- **Codice abbreviato**:Cose che si possono fare in una frase.
  - **Convertire XLSX in PDF** → ConvertiFoglioDiCalcoloInPdf
  - **Elimina gli spazi extra nell'intero file** → TrimSpreadsheetContent
  - **Combina più di 10 file in un unico report** → Unisci fogli di calcolo

## **Come utilizzare le API cloud Aspose.Cells?**

###  Fase 1:**Ottieni le credenziali API**

- **[Registra Aspose Account Cloud](https://dashboard.aspose.cloud/signup)**
- **[Ottieni le credenziali del cliente](https://dashboard.aspose.cloud/#/applications)**

###  Fase 2:**Chiama le API Web del foglio di calcolo con SDK (consigliato)**

Si consiglia di utilizzare l'SDK ufficiale per semplificare il processo di autenticazione e richiesta.

#### **[Installa SDK (usando .NET come esempio)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell

dotnet add package Aspose.Cells-Cloud --version 25.8.0

```

####  Esempio:**Converti Excel in PDF con SDK**

```C#
    CellsApi cellsApi = new CellsApi(Environment.GetEnvironmentVariable("ProductClientId"), Environment.GetEnvironmentVariable("ProductClientSecret"));
    cellsApi.ConvertSpreadsheet(new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" }, "EmployeeSalesSummary.pdf");
```

#### Descrizione

- **Foglio di calcolo**: Il nome del file Excel che deve trovarsi nella memoria locale.
- **Formato**Formato di destinazione. Ad esempio pdf, png, csv, json, ecc.
- **File di output** verrà salvato nella posizione locale. Il nome del file di output è "EmployeeSalesSummary.pdf".

## **Funzioni principali**

Aspose.Cells Cloud offre le seguenti funzionalità chiave per soddisfare le esigenze di automazione dei fogli di calcolo a livello aziendale:

### **Convertitore di fogli di calcolo**

- **[Converti foglio di calcolo in file PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**
- **[Converti grafico del foglio di calcolo in immagine](https://docs.aspose.cloud/cells/convert-chart-to-image/)**
- **[Salva foglio di calcolo con nome](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**

### **Elaborazione dei dati**

- **[Unisci fogli di calcolo](https://docs.aspose.cloud/cells/merge-spreadsheets/)**
- **[Fogli di calcolo divisi](https://docs.aspose.cloud/cells/split-spreadsheet/)**
- **[Elimina le righe vuote del foglio di calcolo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**
- **[Elimina le colonne vuote del foglio di calcolo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**
- **[Sostituisci il contenuto del foglio di calcolo](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**

## Supporta gli SDK (**SDK disponibili**)

-  Aspose.Cells Offerte cloud[SDK](https://github.com/aspose-cells-cloud)** in più lingue, pronto all'uso:

| Lingua| Metodo di installazione| Repository GitHub|
||----|-------|
|[Java](https://www.oracle.com/java/) |[Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) |[Java Repository GitHub dell'SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
|[.NET](https://dotnet.microsoft.com/) |[NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) |[.NET Repository GitHub dell'SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
|[Python](https://www.python.org/) |[pip](https://pypi.org/project/asposecellscloud/) |[Python Repository GitHub dell'SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
|[Node.js](https://nodejs.org/en) |[npm](https://www.npmjs.com/package/asposecellscloud) |[Repository GitHub dell'SDK Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
|[PHP](https://www.php.net/) |[Compositore](https://packagist.org/packages/aspose/cells-sdk-php) |[PHP Repository GitHub dell'SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
|[GoLang](https://go.dev/) |[Moduli Go](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) |[Repository GitHub dell'SDK GoLang](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
|[Rubino](https://www.ruby-lang.org/) |[RubyGems](https://rubygems.org/gems/aspose_cells_cloud) |[Repository GitHub dell'SDK Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
|[Perl](https://www.perl.org/) |[CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) |[Perl Repository GitHub dell'SDK](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |

- **API Punto finale**: [Aspose.Cells Cloud Spreadsheet Web API Riferimento](https://reference.aspose.cloud/cells/)

## **Esempi di codice e progetti open source**

Tutti gli SDK sono open source e includono esempi completi:

- [Java Esempi SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)
- [.NET Esempi SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)
- [Python Esempi SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)
- [Esempi di Node.js SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)
- [PHP Esempi SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)
- [Esempi di Go SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)
- [Esempi di Ruby SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)
- [Perl Esempi SDK su Github.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)
