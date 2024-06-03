---
title: Docker Contain Nasıl Çalıştırılır
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Docker Aspose.Cells Bulut konteyneri nasıl çalıştırılır. Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, koruma, iç nesne işlemleri vb. için Excel'i destekler
weight: 100
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Docker Container Nasıl Çalıştırılır
---
**Liman işçisi**teknolojisi, hafif kaplar kullanarak uygulamaların dağıtımını otomatikleştirmek için tasarlanmıştır. Geliştiriciler şunları kullanabilir:**Docker Konteyneri** Bir uygulamayı tüm kitaplıkları ve bağımlılıklarıyla birlikte sarmak ve her şeyi tek bir paket olarak dağıtmak için.

 Aspose.Cells Bulut ekibi Docker Container'ı şu tarihte yayınladı:[Docker Merkezi](https://hub.docker.com/r/aspose/cells-cloud) Docker kullanıcılarını kolaylaştırmak için. Aşağıdaki bölümler, Docker komutlarını nasıl çalıştıracağınız veya Docker oluşturma aracı için Yaml dosyasına yapılandırmayı nasıl yazacağınız konusunda size yol gösterecektir.

## Konteyner yapılandırması

### Gerekli hacimler

|Konteynere montaj yolu|Tanım|
|:- |:- |
|C:\fontlar|Belgeleri oluşturmak için kullanılacak yazı tiplerini içeren klasör|
|C:\veri|Dosya depolama klasörü|

### Parametreler

|İsim|Tanım|
|:- |:- |
|LisansGenelAnahtar|Lisansın genel anahtarı|
|LisansÖzelAnahtar|Lisansın özel anahtarı|


"Lisans" parametreleri atlanırsa uygulama deneme modunda çalışacaktır.


### Komut satırını kullanarak Docker kapsayıcısını çalıştırın

Konteyneri çıkardıktan sonra aşağıdaki docker komutunu çalıştırabilirsiniz.[Docker Merkezi](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Docker-Compose Tool için Yapılandırmalar

Docker-Compose aracı için yaml dosyanıza aşağıdaki konfigürasyonları yazabilirsiniz:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
