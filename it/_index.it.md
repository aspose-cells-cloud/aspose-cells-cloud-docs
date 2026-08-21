---
title: "Aspose.Cells Cloud API – Convertire, unire, dividere e proteggere file Excel"
second_title: "Documento"
ArticleTitle: "Aspose.Cells Cloud API – Convertire, unire, dividere e proteggere file Excel"
linktitle: "Centro sviluppatori"
type: docs
url: /
description: "L'API REST di Aspose.Cells Cloud consente la conversione, l'unione, la divisione, la protezione e l'elaborazione completa dei fogli di calcolo Excel. Fino a 150 chiamate al mese gratuite, SDK disponibili per 8 linguaggi."
weight: 10
keywords: "Aspose.Cells Cloud, API Excel, conversione foglio di calcolo, unire Excel, dividere Excel, proteggere Excel, SDK foglio di calcolo cloud, REST API, elaborazione Excel"
---

## Cos'è l'API Aspose.Cells Cloud?

Aspose.Cells Cloud API è una raccolta di servizi cloud per fogli di calcolo/Excel. Non è richiesta alcuna installazione di Office né configurazione del server: basta inviare una richiesta HTTP e potrai creare, modificare, convertire, pulire i dati, generare grafici, costruire tabelle pivot, crittografare, dividere, unire, aggiungere filigrane, applicare firme digitali e molto altro ancora, da qualsiasi linguaggio di programmazione.

## Perché utilizzare le API Aspose.Cells Cloud?

- Creare, modificare, convertire e analizzare fogli di calcolo su archiviazione cloud basata sui servizi API Web Aspose.Cells Cloud.  
- Creare, modificare, convertire e analizzare file di fogli di calcolo locali basati sui servizi API Web Aspose.Cells Cloud.  
- I formati di file supportati includono 30 formati, tra cui **xlsx**, **csv**, **ods**, **xlsb**, ecc.  
- Gestire i fogli di calcolo direttamente tramite l'API Web Aspose.Cells Cloud senza dipendenze da Microsoft Excel.  
- Il piano gratuito include fino a 150 chiamate API al mese.  
- Pricing in base al consumo (pay-as-you-go).  
- **Short-code**: Operazioni descritte in una frase.  
  - **Convertire XLSX in PDF** → ConvertSpreadsheetToPdf  
  - **Eliminare spazi extra in tutto il file** → TrimSpreadsheetContent  
  - **Unire oltre 10 file in un unico report** → MergeSpreadsheets  

## **Come utilizzare le API Aspose.Cells Cloud?**

### Passo 1: **Ottenere le credenziali API**  

- **[Registrare un account Aspose Cloud](https://dashboard.aspose.cloud/signup)**  
- **[Ottenere le credenziali client](https://dashboard.aspose.cloud/#/applications)**  

### Passo 2: **Chiamare le API Web per fogli di calcolo tramite SDK (raccomandato)**  

Si consiglia di utilizzare l'SDK ufficiale per semplificare l'autenticazione e la gestione delle richieste. L'SDK acquisisce e aggiorna automaticamente i token di accesso.

#### **[Installare SDK .NET (NuGet)](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab)**

```powershell
dotnet add package Aspose.Cells-Cloud --version 26.6.0
```

#### Esempio: **Convertire Excel in PDF tramite SDK**

```csharp
CellsApi cellsApi = new CellsApi(
    Environment.GetEnvironmentVariable("ProductClientId"),
    Environment.GetEnvironmentVariable("ProductClientSecret"));
cellsApi.ConvertSpreadsheet(
    new ConvertSpreadsheetRequest { Spreadsheet = "EmployeeSalesSummary.xlsx", format = "pdf" },
    "EmployeeSalesSummary.pdf");
```

#### Descrizione

- **Spreadsheet**: Nome del file Excel presente nell'archiviazione locale.  
- **Format**: Formato di destinazione (ad esempio, pdf, png, csv, json).  
- **File di output**: Il file risultante verrà salvato localmente con il nome specificato.  

## **Funzionalità principali**

Aspose.Cells Cloud offre le seguenti funzionalità chiave per soddisfare le esigenze di automazione dei fogli di calcolo a livello enterprise:

### **Conversione foglio di calcolo**

- **[Convertire foglio di calcolo in file PDF](https://docs.aspose.cloud/cells/convert-excel-file-to-pdf-file/)**  
- **[Convertire grafico foglio di calcolo in immagine](https://docs.aspose.cloud/cells/convert-chart-to-image/)**  
- **[Salva foglio di calcolo come](https://docs.aspose.cloud/cells/save-an-excel-file-as-other-formats-files/)**  

### **Elaborazione dati**

- **[Unire fogli di calcolo](https://docs.aspose.cloud/cells/merge-spreadsheets/)**  
- **[Dividere fogli di calcolo](https://docs.aspose.cloud/cells/split-spreadsheet/)**  
- **[Eliminare righe vuote dal foglio di calcolo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-rows/)**  
- **[Eliminare colonne vuote dal foglio di calcolo](https://docs.aspose.cloud/cells/delete-spreadsheet-blank-columns/)**  
- **[Sostituire contenuto foglio di calcolo](https://docs.aspose.cloud/cells/replace-spreadsheet-content/)**  

> **Nota**: Schema dettagliati delle richieste/risposte, metodi HTTP, parametri di query e risposte di esempio per ogni endpoint sono disponibili nel **Riferimento API Web Aspose.Cells Cloud per fogli di calcolo**, indicato di seguito.

**Riferimento rapido agli endpoint**

| Operazione | Metodo HTTP | Percorso | Parametri obbligatori | Risposta di esempio |
|-----------|-------------|------|---------------------|-----------------|
| Convertire foglio di calcolo | POST | `/cells/convert` | `Spreadsheet` (file), `format` (string) | File binario (ad esempio, PDF) |
| Unire fogli di calcolo | POST | `/cells/worksheets/merge` | `files` (elenco di file) | Cartella di lavoro unita |
| Dividere foglio di calcolo | POST | `/cells/worksheets/split` | `Spreadsheet` (file), `format` (string) | Archivio di file divisi |
| Eliminare righe vuote | POST | `/cells/worksheets/blankrows/delete` | `Spreadsheet` (file) | Cartella di lavoro aggiornata |
| Sostituire contenuto | POST | `/cells/replace` | `Spreadsheet` (file), `oldValue`, `newValue` | Cartella di lavoro aggiornata |

## SDK supportati (**SDK disponibili**)

- Aspose.Cells Cloud fornisce [SDK](https://github.com/aspose-cells-cloud) pronti all’uso in ogni linguaggio principale: clona, codifica e distribuisci:

| Linguaggio | Metodo di installazione | Repository GitHub SDK |
|------|----------|-------------|
| [Java](https://www.oracle.com/java/) | [Maven](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/blob/master/Aspose.Cells.Cloud.pom.xml) | [Repository GitHub SDK Java](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java) |
| [.NET](https://dotnet.microsoft.com/) | [NuGet](https://www.nuget.org/packages/Aspose.cells-Cloud/#readme-body-tab) | [Repository GitHub SDK .NET](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet) |
| [Python](https://www.python.org/) | [pip](https://pypi.org/project/asposecellscloud/) | [Repository GitHub SDK Python](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python) |
| [Node.js](https://nodejs.org/en) | [npm](https://www.npmjs.com/package/asposecellscloud) | [Repository GitHub SDK Node.js](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node) |
| [PHP](https://www.php.net/) | [Composer](https://packagist.org/packages/aspose/cells-sdk-php) | [Repository GitHub SDK PHP](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php) |
| [GoLang](https://go.dev/) | [Go Modules](https://pkg.go.dev/github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25) | [Repository GitHub SDK Go](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go) |
| [Ruby](https://www.ruby-lang.org/) | [RubyGems](https://rubygems.org/gems/aspose_cells_cloud) | [Repository GitHub SDK Ruby](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby) |
| [Perl](https://www.perl.org/) | [CPAN](https://metacpan.org/dist/AsposeCellsCloud-CellsApi) | [Repository GitHub SDK Perl](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl) |
| **Endpoint API** | [Riferimento API Web Aspose.Cells Cloud per fogli di calcolo](https://reference.aspose.cloud/cells/) |  |

## **Esempi di codice e progetti open source**

Tutti gli SDK sono open-source e includono numerosi esempi:

- [Esempi SDK Java su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java/tree/master/Examples)  
- [Esempi SDK .NET su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet/tree/master/examples)  
- [Esempi SDK Python su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-python/tree/master/examples)  
- [Esempi SDK Node.js su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node/tree/master/Examples)  
- [Esempi SDK PHP su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php/tree/master/examples)  
- [Esempi SDK Go su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go/tree/master/examples)  
- [Esempi SDK Ruby su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby/tree/master/examples)  
- [Esempi SDK Perl su GitHub.](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl/tree/master/examples)  
---