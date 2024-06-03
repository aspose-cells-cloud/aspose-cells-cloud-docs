---
title: Come eseguire Docker Container
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Come eseguire Docker Aspose.Cells Contenitore cloud. Aspose.Cells Cloud supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni di oggetti interni e così via
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Come eseguire il contenitore Docker
---
 IL**Docker**la tecnologia è progettata per automatizzare la distribuzione delle applicazioni utilizzando contenitori leggeri. Gli sviluppatori possono utilizzare a**Contenitore Docker** per racchiudere un'applicazione con tutte le sue librerie e dipendenze e distribuire tutto come un unico pacchetto.

 Aspose.Cells Il team Cloud ha pubblicato il Docker Container su[Hub Docker](https://hub.docker.com/r/aspose/cells-cloud) per facilitare gli utenti di Docker. Le sezioni seguenti ti guideranno su come eseguire comandi Docker o scrivere la configurazione in un file Yaml per lo strumento di composizione Docker.

## Configurazione del contenitore

### Volumi richiesti

|Montare il percorso nel contenitore|Descrizione|
|:- |:- |
|C:\caratteri|Cartella con i caratteri, che verranno utilizzati per eseguire il rendering dei documenti|
|C:\dati|Cartella di archiviazione dei file|

### Parametri

|Nome|Descrizione|
|:- |:- |
|LicensePublicKey|Chiave pubblica della licenza|
|LicenzaPrivateKey|Chiave privata della licenza|


Se i parametri "Licenza" vengono omessi, l'app funzionerà in modalità di prova.


### Esegui un contenitore Docker utilizzando la riga di comando

Puoi semplicemente eseguire il seguente comando docker dopo aver estratto il contenitore[Hub Docker](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Configurazioni per lo strumento Docker-Compose

Puoi scrivere le seguenti configurazioni nel tuo file yaml per lo strumento Docker-Compose:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
