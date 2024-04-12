---
title: Stockage
second_title: Aspose.Cells Cloud Documen
type: docs
url: /fr/docker/storage/
description: Comment définir la position de stockage sur Aspose.Cells Cloud pour Docker
weight: 30
---
##  Configuration de stockage par défaut ##

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


- **les fenêtres**

```powershell

c:\app\storageResource.json

```

- **Linux**

```linux

/app/storageResource.json


```

##  Configuration de stockage personnalisée ##

Il est nécessaire de re-spécifier le profil de stockage pour le fichier image Cloud Aspose.Cells lorsque le client a besoin de spécifier le dossier de stockage.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Document de référence** : 
  - [Exécution Docker]( https://docs.docker.com/engine/reference/commandline/run/)