---
title: Docke
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Nuage
weight: 30
kwords: Excel, Office Cloud, REST API, Tableur, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Cloud Docker

L'image Cloud Aspose.Cells est disponible pour Linux, Microsoft Windows 11 Pro, Microsoft Windows Server 2016, Microsoft Windows Server 2019, Microsoft Windows Server 2022.

## Référence API - Aspose.Cells Cloud Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Exposer le port

Port | Description | Obligatoire
---|:--:|---:
5000 | Dossier contenant les polices qui seront utilisées pour le rendu des documents | vrai

##  Volumes requis ##

Chemin de montage dans le conteneur | Description | Obligatoire
---|:--:|---:
C:\fonts | Dossier contenant les polices, qui seront utilisées pour restituer les documents | faux
C:\data | Dossier de stockage de fichiers | false

##  Paramètres d'exécution ##

Nom | Description | Obligatoire
---|:--:|---:
LicensePublicKey | Clé publique de la licence | true
LicensePrivateKey | Clé privée de la licence | true
storagesCredentialsFilePath | Chemin du fichier de configuration du stockage. Le fichier par défaut est ./storageResource.json | true

##  Exécuter la commande ##

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

**Document de référence** :

- [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)
-

voir:

- [Télécharger les informations](/cells/fr/docker/downloads/)
- [Informations sur la version d'exécution](/cells/fr//docker/tag-list/)
- [Informations de stockage](/cells/fr/docker/storage/)
