---
title: Comment définir la position de stockage pour le stockage du conteneur Cloud Docker Aspose.Cells
second_title: Documen
ArticleTitle: Aspose.Cells Cloud Docker Container Storage Configuratio
linktitle: Stockage de conteneurs
type: docs
url: /fr/docker/storage/
description: Comment définir la position de stockage pour le stockage du conteneur Cloud Docker Aspose.Cells
weight: 30
kwords: Excel Conteneur Docker Cloud, Conteneur Docker Cloud autonome, Conteneur Docker REST, Feuille de calcul, PDF, CSV, Json, Markdown, Image Docker, Exécuter le conteneur Docker
---
## Configuration de stockage par défaut ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

``` json

{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}

```

{{< /tab >}}

{{< /tabs >}}

##  Position par défaut ##

- **fenêtres**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Configuration de stockage personnalisée ##

Il est nécessaire de spécifier à nouveau le profil de stockage pour le fichier image Cloud Aspose.Cells lorsque le client doit spécifier le dossier de stockage.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Document de référence** :

- [Comment exécuter le conteneur Cloud Docker Aspose.Cells.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
