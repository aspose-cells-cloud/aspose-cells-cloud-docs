---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/docker/run/
description: Aspose.Cells Cloud for Docker nasıl çalıştırılır
weight: 30
---
## Bağlantı Noktasını Açığa Çıkar

Liman | Açıklama | Gerekli
---|:--:|---:
5000 | Belgeleri işlemek için kullanılacak yazı tiplerini içeren klasör | doğru


##  Gerekli hacimler ##
Yolu kapsayıcıya monte edin | Açıklama | Gerekli
---|:--:|---:
C:\yazı tipleri | Belgeleri işlemek için kullanılacak yazı tiplerini içeren klasör | YANLIŞ
C:\veri | Dosya depolama klasörü | YANLIŞ

##  Çalıştırma Parametreleri ##

İsim | Açıklama | Gerekli
---|:--:|---:
LisansKamuAnahtarı | Lisansın genel anahtarı | doğru
LisansÖzel Anahtar | Lisansın özel anahtarı | doğru
depolarKimlik BilgileriFilePath | Depolama, dosya yolunu yapılandırır. Varsayılan dosya ./storageResource.json | doğru

##  Çalıştır Komutu ##

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows

docker run  -d  -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux

docker run  -d  -p 47900:5000  -e LicensePublicKey=yourLicensePublicKey	 -e LicensePrivateKey=yourLicensePrivateKey-e storagesCredentialsFilePath=./storageResource.json --name asposecellscloud  aspose/cells-cloud:linux.22.2.0


```

{{< /tab >}}

{{< /tabs >}}


**Referans Belgesi** : 
  - [Docker Çalıştır]( https://docs.docker.com/engine/reference/commandline/run/)