---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/docker/run/
description: Come eseguire Aspose.Cells Cloud per Docker
weight: 30
---
## Porto esposto

Porto | Descrizione | Necessario
---|:--:|---:
5000| Cartella con i caratteri, che verranno utilizzati per visualizzare i documenti | VERO


##  Volumi richiesti ##
Montare il percorso nel contenitore | Descrizione | Necessario
---|:--:|---:
C:\caratteri | Cartella con i caratteri, che verranno utilizzati per visualizzare i documenti | falso
C:\dati | Cartella di archiviazione file | falso

##  Esegui parametri ##

Nome | Descrizione | Necessario
---|:--:|---:
LicensePublicKey | Chiave pubblica della licenza | VERO
LicenzaPrivateKey | Chiave privata della licenza | VERO
archiviCredentialsFilePath | L'archiviazione configura il percorso del file. Il file predefinito è ./storageResource.json | VERO

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
  - [Esegui Docker]( https://docs.docker.com/engine/reference/commandline/run/)