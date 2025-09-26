---
title: "How to set the storage position for Aspose.Cells Cloud Docker Container storage"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Container Storage Configuration"
linktitle: "Container Storage"
type: docs
url: /docker/storage/
description: "How to set the storage position for Aspose.Cells Cloud Docker Container storage."
weight: 30
kwords: Excel Cloud Docker Container, Self-Cloud Docker Container, REST Docker Container, Spreadsheet, PDF, CSV, Json, Markdown, Docker Image, Run Docker Container
---


## Default Storage Configuration ##

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

## Default Position ##

- **windows**

```powershell

c:\app\storageResource.json

```

- **linux**

```linux

/app/storageResource.json


```

## Custom Storage Configuration ##

Need to re-specify the storage profile for Aspose.Cells Cloud image file when the customer need specifies storage folder.

``` powershell

docker run  -d  -v c:/data:c:/data  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey  -e storagesCredentialsFilePath=c:/data/storageResource.json --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0

```

**Reference Document** :

- [How to run Aspose.Cells Cloud Docker container.]( https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
