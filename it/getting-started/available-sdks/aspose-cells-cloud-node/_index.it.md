---
title: Aspose.Cells Cloud SDK per Nod
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/available-sdks/aspose-cells-cloud-node/
description: Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Node
---
 L'SDK è open source e concesso in licenza con la licenza MIT. Puoi accedere al codice sorgente della libreria Node per Aspose.Cells Cloud[Qui](https://github.com/aspose-cells-cloud/aspose-cells-cloud-node).


# **Come utilizzare la libreria Node di Aspose.Cells Cloud**

Aspose.Cells Cloud SDK per Node è una potente libreria che consente agli sviluppatori di manipolare ed elaborare i file Microsoft Excel utilizzando il linguaggio di programmazione Node. Con questo SDK puoi creare, modificare e convertire i documenti Excel nel cloud, senza installare software aggiuntivo o dipendenze sul tuo computer locale.


In questo articolo esploreremo come utilizzare Aspose.Cells Cloud SDK for Node per eseguire alcune attività comuni, come la creazione di una nuova cartella di lavoro Excel, l'inserimento di dati nelle celle e il salvataggio della cartella di lavoro modificata nel cloud.

## Iniziare

 Prima di poter iniziare a utilizzare Aspose.Cells Cloud SDK for Go, devi configurare il tuo ambiente di sviluppo e installare le dipendenze necessarie. Fare riferimento a[l'articolo](https://docs.aspose.cloud/cells/quickstart/) sul sito web Aspose per ottenere l'ID cliente e il segreto cliente.

## Come installare il pacchetto Node per Aspose.Cells Cloud

Puoi installare Aspose.Cells Cloud SDK per Node utilizzando npm. Di seguito sono riportati i passaggi per npm:


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

## Come utilizzare il pacchetto Node per convertire Xlsx in PDF

- Importa libreria cloud Aspose.Cells
 Inizia importando il pacchetto necessario dall'SDK Cloud NodeJS Aspose.Cells nel tuo progetto.
- Configurare Cliente API con Credenziali
 Autentica il tuo client API con il tuo ID client univoco e il segreto client.
- Preparare i parametri di conversione
 Definire i parametri per l'attività di conversione, incluso il nome del file di origine, il formato di output desiderato e il percorso della cartella di archiviazione.
- Esegui la conversione della cartella di lavoro
 Richiamare il processo di conversione utilizzando il metodo PostConvertWorkbook e gestire la risposta.

```javascript
var fs = require('fs');
var path = require('path');
const _ = require('asposecellscloud');

const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret,"v3.0",process.env.CellsCloudApiBaseUrl);

var remoteFolder = "TestData/In"
  
var localName = "Book1.xlsx"
var remoteName = "Book1.xlsx"

var localNameRequest = new  model.UploadFileRequest();
localNameRequest.uploadFiles ={localName:fs.createReadStream(localPath  + localName)};
localNameRequest.path = remoteFolder + "/" + remoteName ;
localNameRequest.storageName ="";
cellsApi.uploadFile(localNameRequest );
 
var format = "csv"

var mapFiles = {};           

 mapFiles[localName]= fs.createReadStream(localPath  +localName) ;

var request = new model.PutConvertWorkbookRequest();
request.file =  mapFiles;
request.format =  format;
return cellsApi.putConvertWorkbook(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});
```
