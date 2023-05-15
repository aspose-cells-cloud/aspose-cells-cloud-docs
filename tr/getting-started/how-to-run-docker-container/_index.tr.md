---
title: Docker Container Nasıl Çalıştırılır?
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Docker Aspose.Cells Bulut kapsayıcısı nasıl çalıştırılır. Aspose.Cells Bulut, oluşturma, dönüştürme, birleştirme, bölme, korumalı, iç nesne işlemi vb. için Excel'i destekler
weight: 100
---
 bu**Liman işçisi** teknolojisi, hafif kapsayıcılar kullanarak uygulamaların dağıtımını otomatikleştirmek için tasarlanmıştır. Geliştiriciler bir**Docker Konteyneri** bir uygulamayı tüm kitaplıkları ve bağımlılıkları ile sarmak ve her şeyi tek bir paket olarak dağıtmak.

 Aspose.Cells Bulut ekibi, Docker Container'ı şu adreste yayınladı:[Docker Hub'ı](https://hub.docker.com/r/aspose/cells-cloud) Docker kullanıcılarını kolaylaştırmak için. Aşağıdaki bölümler, Docker oluşturma aracı için bir Docker komutlarının nasıl çalıştırılacağı veya bir Yaml dosyasında yapılandırma yazılacağı konusunda size rehberlik edecektir.

## Kapsayıcı yapılandırması

### Gerekli hacimler

|Yolu kapsayıcıya bağlama|Tanım|
|:- |:- |
|C:\yazı tipleri|Belgeleri işlemek için kullanılacak yazı tiplerini içeren klasör|
|C:\veri|Dosya depolama klasörü|

### parametreler

|İsim|Tanım|
|:- |:- |
|LisansGenelAnahtar|Lisansın genel anahtarı|
|LisansÖzel Anahtar|Lisansın özel anahtarı|


"Lisans" parametreleri atlanırsa uygulama deneme modunda çalışacaktır.


### Komut satırını kullanarak bir Docker konteyneri çalıştırın

 Kapsayıcıyı çektikten sonra aşağıdaki docker komutunu çalıştırabilirsiniz.[Docker Hub'ı](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Docker-Compose Aracı için Yapılandırmalar

Docker-Compose aracı için yaml dosyanıza aşağıdaki yapılandırmaları yazabilirsiniz:

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
