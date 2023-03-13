---
title: "How to Run Docker Container"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "How to run Docker Aspose.Cells Cloud container. Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 100
---

The **Docker** technology is designed to automate the deployment of the applications by using lightweight containers. Developers can use a **Docker Container** to wrap up an application with all of its libraries and dependencies and deploy everything as a single package.

Aspose.Cells Cloud team has published the Docker Container on [Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) to facilitate the Docker users. The following sections will guide you that how to run a Docker commands or write configuration in a Yaml file for Docker compose tool.

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


### Run a Docker container using command line

You can simply run the following docker command after pulling the container from [Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Configurations for Docker-Compose Tool

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
