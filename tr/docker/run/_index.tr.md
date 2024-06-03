---
title: Ru
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/docker/run/
description: Docker için Aspose.Cells Cloud nasıl çalıştırılır
weight: 30
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Çalıştır
---
## Bağlantı Noktasını Göster

Liman | Açıklama | Gerekli
---|:--:|---:
5000 | Belgeleri oluşturmak için kullanılacak yazı tiplerini içeren klasör | doğru


##  Gerekli hacimler ##
Konteynere montaj yolu | Açıklama | Gerekli
---|:--:|---:
C:\fontlar | Belgeleri oluşturmak için kullanılacak yazı tiplerini içeren klasör | YANLIŞ
C:\veri | Dosya depolama klasörü | YANLIŞ

##  Parametreleri Çalıştır ##

İsim | Açıklama | Gerekli
---|:--:|---:
LisansGenelAnahtar | Lisansın genel anahtarı | doğru
LisansÖzelAnahtar | Lisansın özel anahtarı | doğru
depolarKimlik BilgileriDosyaYolu | Depolama yapılandırma dosyası yolu. Varsayılan dosya: ./storageResource.json | doğru

##  Komutu Çalıştır ##

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
  - [Docker Çalıştırması]( https://docs.docker.com/engine/reference/commandline/run/)
