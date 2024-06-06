---
title: Aspose.Cells Cloud SDK per Ne
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-net/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Net
---
 L'SDK è open source e concesso in licenza con la licenza MIT. È possibile accedere al codice sorgente della libreria Net per Aspose.Cells Cloud[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-dotnet).


# **Come utilizzare la libreria Net di Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Net è una potente libreria che consente agli sviluppatori di manipolare ed elaborare file Microsoft Excel utilizzando il linguaggio di programmazione Net. Con questo SDK puoi creare, modificare e convertire i documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK for Net per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK for Go, devi configurare il tuo ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web Aspose per ottenere l'ID cliente e il segreto cliente.

## Come installare il pacchetto Net per Aspose.Cells Cloud

Puoi installare Aspose.Cells Cloud SDK for Net utilizzando nuget. Di seguito sono riportati i passaggi per nuget:

```nuget

Install-Package Aspose.Cells-Cloud

```

È possibile installare Aspose.Cells Cloud SDK for Net anche utilizzando dotnet. Di seguito sono riportati i passaggi per dotnet:

```powershell

dotnet add package Aspose.Cells-Cloud 

```

## Come utilizzare il pacchetto Net per convertire Xlsx in PDF

- Importa libreria cloud Aspose.Cells
 Inizia importando il pacchetto necessario dall'SDK Cloud DotNet Aspose.Cells nel tuo progetto.
- Configurare Cliente API con Credenziali
 Autentica il tuo client API con il tuo ID client univoco e il segreto client.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, incluso il nome del file di origine, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione della cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

### **Codice d'esempio**

```CSharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using Aspose.Cells.Cloud.SDK.Request;
using System;
using System.IO;
using System.Collections.Generic;

CellsApi cellsApi = new CellsApi("xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx");
string remoteFolder = "TestData/In";

string localName = "Book1.xlsx";
string remoteName = "Book1.xlsx";

this.UploadFile( localName, remoteFolder + "/" + remoteName, "");

IDictionary<string, Stream> mapFiles =new Dictionary<string,Stream>(); 
AddFileParameter(localName,mapFiles);       
var request = new PutConvertWorkbookRequest(
    file: mapFiles,
    format: format
);
this.CellsApi.PutConvertWorkbook(request);
```
