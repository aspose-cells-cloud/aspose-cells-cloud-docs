---
title: Docke
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Nuvola
weight: 30
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Cloud Docker

Aspose.Cells Cloud Image è disponibile per Linux, Microsoft Windows 11 Pro, Microsoft Windows Server 2016, Microsoft Windows Server 2019, Microsoft Windows Server 2022.

## API Riferimento - Aspose.Cells Cloud Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Porta esposta

Porta | Descrizione | Obbligatorio
---|:--:|---:
5000 | Cartella con i font che verranno utilizzati per il rendering dei documenti | true

##  Volumi richiesti ##

Percorso di montaggio nel contenitore | Descrizione | Obbligatorio
---|:--:|---:
C:\fonts | Cartella con i font che verranno utilizzati per il rendering dei documenti | false
C:\dati | Cartella di archiviazione file | falso

##  Parametri di esecuzione ##

Nome | Descrizione | Obbligatorio
---|:--:|---:
LicensePublicKey | Chiave pubblica della licenza | true
LicensePrivateKey | Chiave privata della licenza | true
storagesCredentialsFilePath | Percorso del file di configurazione dell'archiviazione. Il file predefinito è ./storageResource.json | true

##  Esegui comando ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}

**Documento di riferimento** :

- [Esecuzione Docker]( https://docs.docker.com/engine/reference/commandline/run/)
-

Vedere:

- [Scarica informazioni](/cells/it/docker/downloads/)
- [Esegui informazioni sulla versione](/cells/it//docker/tag-list/)
- [Informazioni di archiviazione](/cells/it/docker/storage/)
