---
title: Aspose.Cells Cloud SDK per PH
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-php/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, PHP
---
L'SDK è open source e concesso in licenza MIT. È possibile accedere al codice sorgente della libreria PHP per Aspose.Cells Cloud.[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-php).

# **Come utilizzare Aspose.Cells Cloud SDK per PHP**

Aspose.Cells Cloud SDK per PHP è una potente libreria che consente agli sviluppatori di manipolare ed elaborare file Microsoft Excel utilizzando il linguaggio di programmazione Go. Con questo SDK, puoi creare, modificare e convertire documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK per PHP per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Cloud SDK per Go Aspose.Cells, è necessario configurare l'ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito Aspose per ottenere il tuo ID cliente e il tuo segreto cliente.

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

- Eseguire l'aggiornamento di Composer per installare l'SDK:

   ```bash

   composer install

   ```

- Includi il caricatore automatico di Composer nel tuo codice PHP:

   ```php

   require 'vendor/autoload.php';

   ```

## Come utilizzare il pacchetto PHP per convertire Xlsx in altri formati

- Importa Aspose.Cells Cloud Library
 Per prima cosa, importa il pacchetto necessario dall'SDK Cloud Aspose.Cells nel tuo progetto.
- Configurare il client API con credenziali
 Autentica il tuo cliente API con il tuo ID cliente univoco e il tuo segreto cliente.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, tra cui il nome del file sorgente, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui conversione cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}
