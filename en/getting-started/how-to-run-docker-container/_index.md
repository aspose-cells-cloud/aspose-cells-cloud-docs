---
title: "How to Run Aspose.Cells Cloud Docker Container:Run the official Aspose.Cells Cloud container in 3 steps: pull, configure, start."
second_title: "Document"
ArticleTitle: "How to Run Aspose.Cells Cloud Docker Container"
LinkTitle: "Docker Container"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "How to run Docker Aspose.Cells Cloud container. Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 100
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdown, How to Run Docker Container
---

The **Docker** technology is designed to automate the deployment of the applications by using lightweight containers. Developers can use a **Docker Container** to wrap up an application with all of its libraries and dependencies and deploy everything as a single package.

Aspose.Cells Cloud team has published the Docker Container on [Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) to facilitate the Docker users. The following sections will guide you on how to run Docker commands or write configuration in a Yaml file for the Docker compose tool.

## Container configuration

### Required volumes

|Mount path in container|Description|
| :- | :- |
|C:\fonts|Folder with fonts, which will be used to render documents|
|C:\data|File storage folder|

### Parameters

|Name|Description|
| :- | :- |
|LicensePublicKey|Public key of the license|
|LicensePrivateKey|Private key of the license|

If "License" parameters are omitted, the app will work in trial mode.

### 1. Pull Aspose.Cells Cloud Image

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Configurations for Docker-Compose Tool

You can write the following configurations in your yaml file for Docker-Compose tool:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```

### 3. Run a Docker container using command line

You can simply run the following docker command after pulling the container from [Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
