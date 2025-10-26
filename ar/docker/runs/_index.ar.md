---
title: كيفية تشغيل Aspose.Cells Cloud Docker Containe
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: حاوية رو
type: docs
url: /ar/run-aspose-cells-cloud-docker-container/
description: كيفية تشغيل Aspose.Cells Cloud Docker Container. Aspose.Cells Cloud Docker Container هي خدمة حاويات تقدمها Aspose وتعتمد على Docker، مما يسمح لك بنشر وظائف Aspose.Cells Cloud API في بيئات سحابية محلية أو خاصة دون الاعتماد على خدمات السحابة العامة Aspose
weight: 30
kwords: Excel حاوية Docker السحابية، حاوية Docker ذاتية السحابة، حاوية REST Docker، جدول بيانات، PDF، CSV، JSON، Markdown، صورة Docker، تشغيل حاوية Docker
---
## تشغيل Aspose.Cells Cloud Docker Container في وضع التجربة

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## تشغيل حاوية Cloud Docker Aspose.Cells في وضع الفوترة المقاسة

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## تشغيل Aspose.Cells Cloud Docker Container في وضع فوترة الترخيص

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## وثيقة مرجعية

- [كيفية تكوين تخزين حاوية Cloud Docker Aspose.Cells.](https://docs.aspose.cloud/cells/docker/storage/)
