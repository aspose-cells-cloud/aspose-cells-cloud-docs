---
title: "Aspose.Cells Cloud Docker Image Tags – Pull Commands for Windows Server and Linux"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Image Tags – Pull Commands for Windows Server and Linux"
linktitle: "Image Tags"
type: docs
url: /docker/tag-list/
description: "Official list of Aspose.Cells Cloud Docker image tags for Windows Server 2016, 2019, 2022, and Linux. Includes pull commands, architecture details, and upgrade information."
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker tags"
  - "Docker pull commands Aspose Cells"
  - "Windows Server 2016 Docker image"
  - "Windows Server 2019 Docker image"
  - "Windows Server 2022 Docker image"
  - "Linux Docker image Aspose.Cells"
  - "Aspose Cells Docker"
---

Aspose.Cells Cloud provides ready‑to‑run Docker images for Windows Server (2016, 2019, 2022) and Linux.  
Each image is versioned with a **tag** that identifies the product release and the target operating system.  
Use the tags below to pull the exact image you need, and refer to the accompanying pull‑and‑run examples for quick startup.

## Windows Server 2016 Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | No newer tag is planned for Windows Server 2016; this is the final released version.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

## Windows Server 2019 Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

## Windows Server 2022 Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

## Linux Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```