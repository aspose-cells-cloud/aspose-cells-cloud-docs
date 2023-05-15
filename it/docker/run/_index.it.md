---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/docker/run/
description: Come eseguire Aspose.Cells Cloud per Docker
weight: 30
---
## Esponi Porto

Porto | Descrizione | Necessario
---|:--:|---:
5000| Cartella con i caratteri, che verranno utilizzati per il rendering dei documenti | VERO


##  Volumi richiesti ##
Percorso di montaggio nel contenitore | Descrizione | Necessario
---|:--:|---:
C:\font | Cartella con i caratteri, che verranno utilizzati per il rendering dei documenti | falso
C:\dati | Cartella di archiviazione file | falso

##  Eseguire i parametri ##

Nome | Descrizione | Necessario
---|:--:|---:
LicenzaPublicKey | Chiave pubblica della licenza | VERO
LicensePrivateKey | Chiave privata della licenza | VERO
storageCredentialsFilePath | Archiviazione configura il percorso del file. Il file predefinito è ./storageResource.json | VERO

##  Esegui comando ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}


**Documento di riferimento** : 
  - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)