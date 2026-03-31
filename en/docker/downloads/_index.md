---  
title: "Aspose.Cells Cloud Docker Image Download"  
second_title: "Document"  
ArticleTitle: "Aspose.Cells Cloud Docker Image Download"  
linktitle: "Image Download"  
type: docs  
url: /docker/downloads/  
description: "Get the latest Aspose.Cells Cloud Docker images for Windows Server 2016/2019 and Linux. Follow step‑by‑step instructions, prerequisites, and security tips to run the container locally."  
weight: 30  
keywords: "Aspose.Cells Cloud, Docker image, download, Windows Server, Linux"  
---  

## Overview  

`aspose/cells-cloud` – the official Docker image that hosts the **Aspose.Cells Cloud** REST API. The image lets you run the full spreadsheet‑processing engine inside a container, enabling offline or private‑cloud deployments without relying on Aspose’s public cloud services.  

---

## Prerequisites  

| Requirement | Details |
|-------------|---------|
| **Docker Engine** | Docker 20.10 or later installed on the host OS. |
| **Operating System** | Windows Server 2016, Windows Server 2019, or any modern Linux distribution. |
| **Docker Hub Access** | An active Docker Hub account (optional but recommended for private images). Run `docker login` if you need to pull from a private repository. |
| **Aspose Cloud Credentials** | `ASPOSE_CLIENT_ID` and `ASPOSE_CLIENT_SECRET` – obtain them from the Aspose Cloud dashboard. |

> **Tip:** Verify Docker installation with `docker --version`.  

---

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---

## Running the Container  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Environment Variables** – `ASPOSE_CLIENT_ID` and `ASPOSE_CLIENT_SECRET` supply the credentials required by the API.  
* **Port Mapping** – The container exposes port 80; map it to a host port (e.g., 8080) to reach the service.  
* **Detach Mode (`-d`)** – Runs the container in the background.  

---

## Versioning & Updates  

| OS | Tag | Release Date | How to Get the Latest |
|----|-----|--------------|-----------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2024‑09‑15 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2024‑09‑15 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2024‑09‑15 | `docker pull aspose/cells-cloud:linux.latest` |

> **Note:** Tag `21.9` is the current stable release. Use the `latest` tag or check the [Aspose.Cells Cloud release notes](/cells/release-notes/) for newer versions.  

---

## Verification & Security  

* **Image Digest Check**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Vulnerability Scan** (recommended)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Best Practices** – Keep Docker up‑to‑date, run containers with the least privileges required, and regularly scan images for known CVEs.  

---

## Common Issues & Troubleshooting  

| Symptom | Possible Cause | Resolution |
|---------|----------------|------------|
| `docker: command not found` | Docker not installed or PATH not set | Install Docker and restart the terminal. |
| Authentication failure when pulling | Missing or incorrect `docker login` | Run `docker login` with valid Docker Hub credentials. |
| Container exits immediately | Missing required environment variables | Provide `ASPOSE_CLIENT_ID` and `ASPOSE_CLIENT_SECRET` as shown in the **Running the Container** section. |
| Port conflict on host | Host port already in use | Choose a different host port (e.g., `-p 8081:80`). |

---

## See Also  

* [Aspose.Cells Cloud API Documentation](/cells/cloud/api/)  
* [Aspose.Cells Cloud Release Notes](/cells/release-notes/) – detailed changelog for version 21.9 and newer.  

---  

*Authored by the Aspose Cloud Engineering Team.*  