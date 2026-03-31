---
title: "Run Aspose.Cells Cloud Docker Container – Pull, Configure & Start"
second_title: "Document"
ArticleTitle: "How to Run Aspose.Cells Cloud Docker Container"
LinkTitle: "Docker Container"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "Learn how to pull, configure, and run the Aspose.Cells Cloud Docker container on Windows or Linux. Includes Docker‑Compose YAML, license setup, port mapping, and troubleshooting tips."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker container"
  - "Docker Compose"
  - "license keys"
  - "Excel"
  - "spreadsheet"
  - "cloud API"
---

Docker technology is designed to automate the deployment of applications by using lightweight containers. Developers can use a Docker container to bundle an application with all of its libraries and dependencies and deploy everything as a single package.

The Aspose.Cells Cloud team has published the Docker container on [Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) to facilitate Docker users.  

**Prerequisites** – Ensure Docker Engine ≥ 20.x is installed and that your operating system (Windows 10/Server 2019/2022 or a supported Linux distribution) meets the requirements. An optional license key can be supplied to run in licensed mode.

## Container configuration

### Required volumes

| Mount path in container | Description |
| :--- | :--- |
| C:\fonts | Folder with fonts that will be used to render documents |
| C:\data | File‑storage folder |

**Linux/macOS alternative** – Use `/fonts` and `/data` in the container and map them to host directories such as `/home/user/fonts` and `/home/user/data` when running the container.

### Parameters

| Name | Description |
| :--- | :--- |
| LicensePublicKey | Public key of the license |
| LicensePrivateKey | Private key of the license |

If the **License** parameters are omitted, the app runs in trial mode.

### 1. Pull Aspose.Cells Cloud Image

```bash
# Pull a specific version of the Aspose.Cells Cloud image
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Pull Aspose.Cells Cloud image for Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Pull Aspose.Cells Cloud image for Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Pull Aspose.Cells Cloud image for Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

### 2. Configurations for Docker‑Compose Tool

You can write the following configuration in a **docker‑compose.yml** file:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # host 5000 → container 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **Note:** The port mapping `5000:80` means that the API will be reachable at `http://localhost:5000`.

### 3. Run a Docker container using the command line

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

#### Viewing logs & health‑check (optional)

```bash
# Show container logs
docker logs <container-id>

# Simple health‑check (add to docker‑compose if desired)
# healthcheck:
#   test: ["CMD", "curl", "-f", "http://localhost:80/health"]
#   interval: 30s
#   timeout: 10s
#   retries: 3
```

---

[^1]: See the official Aspose.Cells Cloud release notes for version 25.9.0 and later.