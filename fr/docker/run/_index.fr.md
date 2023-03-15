﻿---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/docker/run/
description: Comment exécuter Aspose.Cells Cloud pour Docker
weight: 30
---
## Exposer le port

Port | Descriptif | Requis
---|:--:|---:
5000 | Dossier avec les polices, qui seront utilisées pour rendre les documents | vrai


##  Volumes requis ##
Monter le chemin dans le conteneur | Descriptif | Requis
---|:--:|---:
C:\polices | Dossier avec les polices, qui seront utilisées pour rendre les documents | FAUX
C:\données | Dossier de stockage de fichiers | FAUX

##  Paramètres d'exécution ##

Nom | Descriptif | Requis
---|:--:|---:
LicencePublicKey | Clé publique de la licence | vrai
LicencePrivateKey | Clé privée de la licence | vrai
storagesCredentialsFilePath | Chemin d'accès au fichier de configuration du stockage. Le fichier par défaut est ./storageResource.json | vrai

##  Exécuter la commande ##

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


**Document de référence** : 
  - [Exécution Docker]( https://docs.docker.com/engine/reference/commandline/run/)