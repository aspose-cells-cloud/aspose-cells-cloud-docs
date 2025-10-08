---
title: "Aspose.Cells Cloud Docker Konteyneri Nasıl Çalıştırılır: Resmi Aspose.Cells Cloud konteynerini 3 adımda çalıştırın: çekin, yapılandırın, başlatın"
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /tr/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Docker Aspose.Cells Cloud konteyneri nasıl çalıştırılır? Aspose.Cells Cloud, Excel'i oluşturma, dönüştürme, birleştirme, bölme, korumalı, iç nesne işlemleri vb. için destekler.
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Docker Konteyneri Nasıl Çalıştırılır
---
 The**Liman işçisi** Bu teknoloji, hafif kapsayıcılar kullanılarak uygulamaların dağıtımını otomatikleştirmek üzere tasarlanmıştır. Geliştiriciler,**Docker Konteyneri** Bir uygulamayı tüm kütüphaneleri ve bağımlılıklarıyla birlikte tamamlamak ve her şeyi tek bir paket olarak dağıtmak.

 Aspose.Cells Bulut ekibi Docker Konteynerini yayınladı[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) Docker kullanıcılarının işini kolaylaştırmak için. Aşağıdaki bölümler, Docker komutlarını nasıl çalıştıracağınız veya Docker Compose aracı için bir Yaml dosyasına nasıl yapılandırma yazacağınız konusunda size rehberlik edecektir.

## Konteyner yapılandırması

### Gerekli hacimler

|Konteynerdeki montaj yolu|Tanım|
|:- |:- |
|C:\fontlar|Belgeleri oluşturmak için kullanılacak yazı tiplerinin bulunduğu klasör|
|C:\veri|Dosya depolama klasörü|

### Parametreler

|İsim|Tanım|
|:- |:- |
|LisansGenelAnahtar|Lisansın genel anahtarı|
|LisansÖzelAnahtar|Lisansın özel anahtarı|

"Lisans" parametreleri atlanırsa uygulama deneme modunda çalışacaktır.

### 1. Aspose.Cells Bulut Görüntüsünü Çekin

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Docker-Compose Aracı için Yapılandırmalar

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

### 3. Komut satırını kullanarak bir Docker konteyneri çalıştırın

 Konteyneri çektikten sonra aşağıdaki docker komutunu çalıştırabilirsiniz[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
