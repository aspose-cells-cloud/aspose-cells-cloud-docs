---
title: Aspose.Cells Cloud SDK per Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Node
---
 L'SDK è open source e concesso in licenza MIT. È possibile accedere al codice sorgente della libreria Node per Aspose.Cells Cloud.[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).

# **Come utilizzare la libreria Node di Aspose.Cells Cloud**

Aspose.Cells Cloud SDK per Node è una potente libreria che consente agli sviluppatori di manipolare ed elaborare file Microsoft e Excel utilizzando il linguaggio di programmazione Node. Con questo SDK, puoi creare, modificare e convertire documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.

In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK per Node per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Cloud SDK per Go Aspose.Cells, è necessario configurare l'ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito Aspose per ottenere il tuo ID cliente e il tuo segreto cliente.

## Come installare il pacchetto Node per Aspose.Cells Cloud

Puoi installare Cloud SDK Aspose.Cells per Node utilizzando npm. Di seguito sono riportati i passaggi per npm:

```Powershell

npm install asposecellscloud

```

## Come aggiungere dipendenze nella configurazione del pacchetto per Aspose.Cells Cloud

file di configurazione del nodo: package.json

```Node

{
    "requires": true,
    "lockfileVersion": 1,
    "dependencies": {
        "@types/jest": "^26.0.24",
        "@types/request": "^2.48.7",
        "asposecellscloud": "24.4",
        "axios": "^1.5.1",
        "JSON": "^1.0.0",
        "mocha": "^10.2.0",
        "request": "^2.88.2",
        "request-debug": "^0.2.0"
    }
}

```

## Come utilizzare il pacchetto Node per convertire Xlsx in altri formati

- Importa Aspose.Cells Cloud Library
 Per prima cosa, importa il pacchetto necessario dall'SDK Cloud NodeJS Aspose.Cells nel tuo progetto.
- Configurare il client API con credenziali
 Autentica il tuo cliente API con il tuo ID cliente univoco e il tuo segreto cliente.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, tra cui il nome del file sorgente, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui conversione cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_AvailableSDKs.ts" >}}
