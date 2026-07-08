---
title: "Aspose.Cells Cloud Docker Image Tags"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Image Tags"
linktitle: "Image Tags"
type: docs
url: /docker/tag-list/
description: "Find the latest Aspose.Cells Cloud Docker image tags for Windows Server (2016‑2022) and Linux. Get pull commands, architecture details, and upgrade notes in one place."
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker Image Tags"
  - "Docker pull commands"
  - "Windows Server Docker tags"
  - "Linux Docker tags"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud provides ready‑to‑run Docker images for Windows Server (2016, 2019, 2022) and Linux.  
Each image is versioned with a **tag** that identifies the product release and the target operating system.  
Use the tags below to pull the exact image you need, and refer to the accompanying pull‑and‑run examples for quick start‑up.

*Last updated: 2026-07-01*

**Prerequisites:** Ensure Docker Engine 20.10 or later is installed and you have a valid Aspose.Cells Cloud license key. The images are built for the specified Windows Server versions or Linux x64.

## Windows Server 2016 Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | No newer tag is planned for Windows Server 2016; this is the final released version.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Refer to the [Docker Overview](/cells/docker/) for additional details.

## Windows Server 2019 Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Refer to the [Docker Overview](/cells/docker/) for additional details.

## Windows Server 2022 Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Refer to the [Docker Overview](/cells/docker/) for additional details.

## Linux Images ##

Tags | Architecture | Dockerfile | Remark
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile not published – image is built from an internal base; see the release notes for build details. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Refer to the [Docker Overview](/cells/docker/) for additional details.

**Version change log**

Tag | Changes
---|---
`ltsc2016.23.5.0` | Final release for Windows Server 2016; includes security patches and performance improvements.
`ltsc2019.25.10.0` | Updated to Aspose.Cells 25.10.0; adds new formula support and bug fixes.
`ltsc2022.25.10.0` | Same as 2019 tag, optimized for Windows Server 2022 runtime.
`linux.25.10.0` | Base Linux image with Aspose.Cells 25.10.0; includes updated dependencies and Linux‑specific optimizations.