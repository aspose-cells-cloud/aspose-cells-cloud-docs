---
title: "Aspose.Cells Cloud Docker Operation Manual: Host the Aspose.Cells Cloud application on your own private infrastructure."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Operation Manual"
linktitle: "Docker"
type: docs
url: /docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: "Aspose.Cells Cloud Docker Container is a containerized service provided by Aspose that is based on Docker, allowing you to deploy the functionalities of the Aspose.Cells Cloud API in local or private cloud environments without relying on Aspose's public cloud services."
weight: 30
kwords: Excel Cloud Docker Container, Self-Cloud Docker Container, REST Docker Container, Spreadsheet, PDF, CSV, Json, Markdown, Docker Image, Docker Container
---

Aspose.Cells Cloud is a cloud-based spreadsheet processing service that supports the creation, editing, conversion, and manipulation of files in formats such as Excel. It can be quickly set up as an independent service environment through Docker deployment, simplifying dependency management and cross-platform deployment processes.

This manual will provide a detailed introduction to the complete operational steps from environment preparation to service verification.

## Environment Preparation

Before deploying the Aspose.Cells Cloud Docker container, ensure that the local environment meets the following dependency requirements to avoid deployment failures due to missing components.

### Basic dependency components

- **Docker Engine:** The container runtime core engine is responsible for creating and managing containers. Minimum Version Requirement is 18.09.0.
- **Operating Systems:** Mainstream operating systems that support Docker

   | Operating System Type | Version |
   |:-- |:-- |
   | Windows | Windows 10/11, |
   | Windows | Windows Server 2016/2019/2022 |
   | Linux | CentOS 7+/Ubuntu 20.04+ |

- **Hardware resources:** Ensure the service runs smoothly to avoid crashes due to insufficient resources.

  - CPU: 2 cores or more.
  - Memory: 4GB or more.
  - Disk: 10GB of free space.

### Key prerequisite conditions

- **Aspose License**: You need to register for an Aspose official account to obtain a valid License (you can apply for a trial version or purchase a commercial version). Without a license, service functionality may be restricted. Please refer to the [License](https://purchase.aspose.com/buy) page for more details.

- **Network Connectivity**: Ensure that the deployment environment can access Docker Hub (to pull images).

## Obtain the Aspose.Cells Cloud Docker image

The Aspose.Cells Cloud image is hosted on Docker Hub and can be directly pulled using the docker pull command, without the need for manual building.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest

```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0

```

## Run Aspose.Cells Cloud Docker Container

### **Run Parameters**

|Name | Description | Remark |
| ---|:--:|---: |
| LicensePublicKey | Set up the public key of the license when using the Metered billing mode.  | Only effective when the Metered billing mode is adopted. |
| LicensePrivateKey | Set up the private key of the license when using the Metered billing mode. | Only effective when the Metered billing mode is adopted. |
| storagesCredentialsFilePath | Storage configure file path. Default file is ./storageResource.json  |  |
| LicenseFile | Set up the license file when using the LicenseFile billing mode. | Only effective when the LicenseFile billing mode is adopted. |
| AccessToken | Set the token for accessing the API.   | If the AccessToken is empty, there is no need for AccessToken confirmation. |

### **Run Command**

Running the container in trial mode is as simple as this:

```
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

For full-fledged execution, you should obtain [Metered license](https://purchase.aspose.com/faqs/licensing/metered/) and mount a host folder for file storage. Here is how run command would look like in this case:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.25.9.0

```

{{< /tab >}}

{{< /tabs >}}

### **API Reference** - Aspose.Cells Cloud Docker

- ` <https://hostname:port/swagger> `
- ` <https://hostname:port/swagger/ui/index.html> `

### **Expose Port**

|Port | Description | Required|
|---|:--:|---:|
5000 |  Folder with fonts, which will be used to render documents | true

### **Required volumes**

| Mount path in container | Description | Required | Remark |
| ---|:--:|---: | ---: |
| C:\fonts |  Folder with fonts, which will be used to render documents | false | Resolve some issues in the spreadsheet/Excel caused by missing fonts. |
| C:\data | File storage folder | false | Increase storage space for easier file management and access. |

## **Reference Document**

<!-- - [Docker Run]( https://docs.docker.com/engine/reference/commandline/run/) -->
- [Download Information](/cells/docker/downloads/)
- [Run version Information](/cells//docker/tag-list/)
- [Storage Information](/cells/docker/storage/)
