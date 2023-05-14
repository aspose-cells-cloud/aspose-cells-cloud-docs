---
title: Storag
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/docker/storage/
description: How to set storage position about Aspose.Cells Cloud for Docker
weight: 30
---
## Default Storage Configuration  ##

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

## Default Position  ##


- **windows**

```powershell

c:\app\storageResource.json

```

- **linux**

```linux

/app/storageResource.json


```

## Custom Storage Configuration  ##

Need to re-specify the storage profile for Aspose.Cells Cloud image file when the customer need specifies storage folder.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey	 -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.2.0

```

**Reference Document** : 
  - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/)