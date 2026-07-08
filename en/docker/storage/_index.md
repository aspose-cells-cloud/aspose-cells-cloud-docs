---
title: "How to set the storage position for Aspose.Cells Cloud Docker Container storage"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Container Storage Configuration"
linktitle: "Container Storage"
type: docs
url: /docker/storage/
description: "How to set the storage position for Aspose.Cells Cloud Docker Container storage."
weight: 30
keywords: "Aspose.Cells, Docker storage, container configuration, JSON, PowerShell, Bash"
---

## Default Storage Configuration ##

**Prerequisites**: Ensure Docker Engine 20.10+ is installed, you have valid Aspose.Cells Cloud license keys (`LicensePublicKey` and `LicensePrivateKey`), and the host folder you intend to use for storage (e.g., `c:/data` on Windows or `/data` on Linux) exists with appropriate permissions.

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

- **windows**

```powershell
c:\app\storageResource.json
```

- **linux**

```bash
/app/storageResource.json
```

## Custom Storage Configuration ##

Re‑specify the storage profile when you need to use a custom storage folder for Aspose.Cells Cloud images.

```bash
docker run -d \
  -v c:/data:c:/data \   # mount host folder as container storage
  -p 47900:5000 \        # map API port
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*Linux example*:

```bash
docker run -d \
  -v /data:/data \   # mount host folder as container storage
  -p 47900:5000 \    # map API port
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**Reference Document** :

- [How to run Aspose.Cells Cloud Docker container.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [Docker Container Features](https://docs.aspose.cloud/cells/docker/container-features/)
- [Downloading Aspose.Cells Cloud Docker Image](https://docs.aspose.cloud/cells/docker/download-image/)
- [Managing Container Tags](https://docs.aspose.cloud/cells/docker/manage-tags/)