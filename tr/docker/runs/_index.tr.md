---
title: Aspose.Cells Cloud Docker Containe nasıl çalıştırılır
second_title: Documen
ArticleTitle: How to run Aspose.Cells Cloud Docker Containe
linktitle: Konteyner Ru
type: docs
url: /tr/run-aspose-cells-cloud-docker-container/
description: Aspose.Cells Cloud Docker Konteyneri nasıl çalıştırılır? Aspose.Cells Cloud Docker Konteyneri, Aspose tarafından sağlanan ve Docker tabanlı bir konteyner hizmetidir. Bu hizmet, Aspose.Cells Cloud API'in genel bulut hizmetlerine güvenmeden yerel veya özel bulut ortamlarında Aspose.Cells işlevlerini dağıtmanıza olanak tanır.
weight: 30
kwords: Excel Bulut Docker Konteyneri, Kendi Bulut Docker Konteyneri, REST Docker Konteyneri, Elektronik Tablo, PDF, CSV, Json, Markdown, Docker Görüntüsü, Docker Konteynerini Çalıştırma
---
## Aspose.Cells Cloud Docker Konteynerini Deneme Modunda Çalıştırın

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0

```

## Aspose.Cells Bulut Docker Konteynerini Ölçülü Faturalama Modunda Çalıştırın

```powershell
# Windows Server 2022
# Metered billing mode: set LicensePublicKey and LicensePrivateKey to environment of docker container
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```

## Lisans Faturalama Modunda Aspose.Cells Bulut Docker Konteynerini Çalıştırın

```powershell
# Windows Server 2022
# License billing mode: set LicenseFile to environment of docker container. 
# Bind storage folder:  -v c:/data:c:/data
# Bind fonts folder: -v C:/Windows/Fonts:C:/Windows/Fonts
docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicenseFile=c:/data/aspose.cells.lic  -e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:ltsc2022.25.9.0

```



## Referans Belgesi

- [Aspose.Cells Cloud Docker Konteyner depolaması nasıl yapılandırılır.](https://docs.aspose.cloud/cells/docker/storage/)
