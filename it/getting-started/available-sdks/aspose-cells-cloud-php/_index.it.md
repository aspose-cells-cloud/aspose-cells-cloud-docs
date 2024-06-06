---
title: Aspose.Cells Cloud SDK per PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, PHP
---
 L'SDK è open source e concesso in licenza con la licenza MIT. Puoi accedere al codice sorgente della libreria PHP per Aspose.Cells Cloud[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Come utilizzare Aspose.Cells Cloud SDK per PHP**

Aspose.Cells Cloud SDK per PHP è una potente libreria che consente agli sviluppatori di manipolare ed elaborare i file Microsoft Excel utilizzando il linguaggio di programmazione Go. Con questo SDK puoi creare, modificare e convertire i documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK per PHP per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK for Go, devi configurare il tuo ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web Aspose per ottenere l'ID cliente e il segreto cliente.

## Come installare il pacchetto PHP per Aspose.Cells Cloud

Puoi installare Aspose.Cells Cloud SDK per PHP. Di seguito sono riportati i passaggi:

- Aggiungi Aspose.Cells Cloud come dipendenza al tuo file `composer.json`:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- Esegui l'aggiornamento di Composer per installare l'SDK:

   ```bash

   composer install

   ```

- Includi il caricatore automatico di Composer nel tuo codice PHP:

   ```php

   require 'vendor/autoload.php';

   ```

## Come utilizzare il pacchetto PHP per convertire Xlsx in PDF

- Importa libreria cloud Aspose.Cells
 Inizia importando il pacchetto necessario dall'SDK Aspose.Cells Cloud PHP nel tuo progetto.
- Configurare Cliente API con Credenziali
 Autentica il tuo client API con il tuo ID client univoco e il segreto client.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, incluso il nome del file di origine, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione della cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

```PHP
<?php
require_once('vendor\autoload.php');
use \Aspose\Cells\Cloud\Api\CellsApi;
use \Aspose\Cells\Cloud\Request\PutConvertWorkbookRequest;

$cellsApi = new CellsApi(getenv("CellsCloudClientId"),getenv("CellsCloudClientSecret"),"v3.0",getenv("CellsCloudApiBaseUrl"));

$remoteFolder = "TestData/In";

$localName = "Book1.xlsx";
$remoteName = "Book1.xlsx";

$format = "csv";

$mapFiles = array ();
$mapFiles[$localName] = CellsApiTestBase::getfullfilename($localName);
CellsApiTestBase::ready(  $this->instance,$localName ,$remoteFolder . "/" . $remoteName ,  "");
 
$request = new PutConvertWorkbookRequest();
$request->setFile( $mapFiles);
$request->setFormat( $format);
$$cellsApi->putConvertWorkbook($request);
```
