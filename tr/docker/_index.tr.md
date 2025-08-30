---
title: Docke
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/docker-developer-guide/
aliases: [/docker/, /docker/run/]
description: Aspose.Cells Bulut
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Docker
---
## Aspose.Cells Bulut Docker

Aspose.Cells Cloud Image, Linux, Microsoft Windows 11 Pro, Microsoft Windows Server 2016, Microsoft Windows Server 2019, Microsoft Windows Server 2022 için kullanılabilir.

## API Referans - Aspose.Cells Bulut Docker

- <https://hostname:port/swagger>
- <https://hostname:port/swagger/ui/index.html>

## Portu Açığa Çıkar

Liman | Açıklama | Gerekli
---|:--:|---:
5000 | Belgeleri oluşturmak için kullanılacak yazı tiplerinin bulunduğu klasör | true

##  Gerekli hacimler ##

Konteynerdeki montaj yolu | Açıklama | Gerekli
---|:--:|---:
C:\fonts | Belgeleri oluşturmak için kullanılacak yazı tiplerinin bulunduğu klasör | false
C:\data | Dosya depolama klasörü | false

##  Çalıştırma Parametreleri ##

Ad | Açıklama | Gerekli
---|:--:|---:
LicensePublicKey | Lisansın genel anahtarı | true
LicensePrivateKey | Lisansın özel anahtarı | true
storagesCredentialsFilePath | Depolama yapılandırma dosya yolu. Varsayılan dosya ./storageResource.json | true

##  Çalıştırma Komutu ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey  -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}

**Referans Belgesi** :

- [Docker Çalıştırma]( https://docs.docker.com/engine/reference/commandline/run/)
-

Görmek:

- [İndirme Bilgileri](/cells/tr/docker/downloads/)
- [Çalıştırma sürümü Bilgileri](/cells/tr//docker/tag-list/)
- [Depolama Bilgileri](/cells/tr/docker/storage/)
