---
title: "Come eseguire il contenitore Cloud Docker Aspose.Cells: esegui il contenitore Cloud ufficiale Aspose.Cells in 3 passaggi: estrai, configura, avvia"
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /it/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Come eseguire il contenitore cloud Docker Aspose.Cells. Il cloud Aspose.Cells supporta Excel per creare, convertire, unire, dividere, proteggere, operazioni su oggetti interni e così via
weight: 100
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Come eseguire un contenitore Docker
---
 IL**Docker** La tecnologia è progettata per automatizzare la distribuzione delle applicazioni utilizzando contenitori leggeri. Gli sviluppatori possono utilizzare un**Contenitore Docker** per comporre un'applicazione con tutte le sue librerie e dipendenze e distribuire tutto come un unico pacchetto.

 Aspose.Cells Il team Cloud ha pubblicato il Docker Container su[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) Per facilitare gli utenti Docker. Le sezioni seguenti ti guideranno su come eseguire comandi Docker o scrivere la configurazione in un file Yaml per lo strumento Docker Compose.

## Configurazione del contenitore

### Volumi richiesti

|Percorso di montaggio nel contenitore|Descrizione|
|:- |:- |
|C:\caratteri|Cartella con i font che verranno utilizzati per il rendering dei documenti|
|C:\dati|Cartella di archiviazione dei file|

### Parametri

|Nome|Descrizione|
|:- |:- |
|LicenzaChiave Pubblica|Chiave pubblica della licenza|
|LicenzaChiavePrivata|Chiave privata della licenza|

Se si omettono i parametri "Licenza", l'app funzionerà in modalità di prova.

### 1. Estrarre l'immagine della nuvola Aspose.Cells

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Configurazioni per lo strumento Docker-Compose

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

### 3. Eseguire un contenitore Docker utilizzando la riga di comando

 Puoi semplicemente eseguire il seguente comando docker dopo aver estratto il contenitore da[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
