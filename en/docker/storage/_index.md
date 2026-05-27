---
title: "Configure Storage Position for Aspose.Cells Cloud Docker Container – Windows & Linux Guide"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Container Storage Configuration Guide"
linktitle: "Container Storage"
type: docs
url: /docker/storage/
description: "Learn how to configure default and custom storage locations for Aspose.Cells Cloud Docker containers on Windows and Linux, including JSON schema and Docker run commands."
weight: 30
keywords: "Aspose.Cells Cloud, Docker storage, container storage configuration, storageResource.json, Windows Docker, Linux Docker"
---

## Default Storage Configuration ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
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

```json
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

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## Custom Storage Configuration ##

You need to re‑specify the storage profile for the Aspose.Cells Cloud image when you want to use a custom storage folder.

```bash
docker run -d -v c:/data:/data -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e STORAGE_CREDENTIALS_FILE_PATH=c:/data/storageResource.json \
  --name asposecellscloud aspose/cells-cloud:ltsc2019.22.9.0
```

**Reference Document** :

- [How to run Aspose.Cells Cloud Docker container.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)