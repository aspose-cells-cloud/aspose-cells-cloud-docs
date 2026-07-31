---
title: "Aspose.Cells Cloud Docker Core Functionality: Spreadsheet Conversion, Merging, Splitting, Protecting, Data Processing, and More."
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud Docker Core Functionality"
linktitle: "Features"
type: docs
url: /docker-container-features/
description: "Run the Aspose.Cells Cloud API locally with the Aspose.Cells Cloud Docker Container—a Docker‑based, containerized service that delivers full spreadsheet processing, privacy, and offline capability without using Aspose’s public cloud."
weight: 30
keywords:
  - Aspose.Cells
  - Docker
  - Spreadsheet conversion
  - Excel processing
  - PDF export
  - CSV handling
  - REST API
  - Containerized service
  - Private cloud
  - Offline processing
---

## What is Aspose.Cells Cloud Docker Container?

Aspose.Cells Cloud Docker Container is a containerized service provided by Aspose that is based on Docker, allowing you to deploy the functionalities of the Aspose.Cells Cloud API in local or private cloud environments without relying on Aspose's public cloud services.

## Why Use Aspose.Cells Cloud Docker Container?

Aspose.Cells Cloud Docker Container is a powerful spreadsheet‑processing service container that supports:

### Core Features

- Reading and writing Excel files (XLS, XLSX, CSV, ODS, etc.)
- Formula calculations, charts, conditional formatting, pivot tables, etc.
- Format conversion (such as Excel to PDF, HTML, images, etc.)
- Cell operations, style settings, worksheet management, etc.

Aspose.Cells Cloud Docker Container encapsulates these features as a RESTful API and packages them into a Docker image, allowing you to run it on your own infrastructure.

### Main Advantages

| Benefits               | Description                                                                 |
| ---------------------- | --------------------------------------------------------------------------- |
| Data privacy and security | All file processing is done within your private network; no need to upload to a third‑party cloud. |
| Offline availability   | Does not rely on Aspose public cloud, suitable for intranet or isolated environments. |
| Scalability            | Easily scale out via Docker/Kubernetes.                                    |
| Unified API            | Fully compatible with the Aspose.Cells Cloud public API; no code changes required. |
| License control        | Supports two types of authorization; choose the one that suits your situation. |

## How to Use Aspose.Cells Cloud Docker Container

Refer to the user manual — [How to Use Aspose.Cells Cloud Docker Container](https://docs.aspose.cloud/cells/docker-developer-guide/#run-asposecells-cloud-docker-container).

**Prerequisites**

- Docker Engine 20.10 or later installed on the host machine.  
- Minimum 2 GB RAM and 2 CPU cores allocated to the container for typical workloads.  
- A valid Aspose.Cells Cloud license file (or access token) placed in a directory that will be mounted into the container.

**Quick start**

1. Pull the Docker image: `docker pull aspose/cells-cloud`.  
2. Run the container, mounting the license and data directories, e.g.:  
   ```bash
   docker run -d -p 8080:80 \
     -v /path/to/license:/app/license \
     -v /path/to/data:/app/data \
     aspose/cells-cloud
   ```  
3. Access the REST API at `http://localhost:8080/v3.0/`. For detailed API usage, see the [Aspose.Cells Cloud API reference](https://docs.aspose.cloud/cells/api-reference/).

## Reference Document

- [How to configure Aspose.Cells Cloud Docker Container storage.](https://docs.aspose.cloud/cells/docker/storage/)