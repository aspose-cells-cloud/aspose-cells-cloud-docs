---
title: "Aspose.Cells Cloud Docker Görüntü Etiketleri"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Docker Görüntü Etiketleri"
linktype: "Etiketler"
type: docs
url: /tr/docker/tag-list/
description: "Windows Sunucusu (2016‑2022) ve Linux için en son Aspose.Cells Cloud Docker görüntü etiketlerini bulun. Çekme komutlarını, mimari ayrıntılarını ve yükseltme notlarını tek bir yerde alın."
weight: 30
keywords:
  - "Aspose.Cells Cloud Docker Görüntü Etiketleri"
  - "Docker çekme komutları"
  - "Windows Sunucusu Docker etiketleri"
  - "Linux Docker etiketleri"
  - "Aspose.Cells Cloud"
---

Aspose.Cells Cloud, Windows Sunucusu (2016, 2019, 2022) ve Linux için çalışır durumda gelen Docker görüntüleri sağlar.  
Her görüntü, ürün sürümünü ve hedef işletim sistemini belirleyen bir **etiket** ile sürüm numaralandırılmıştır.  
Aşağıdaki etiketleri kullanarak ihtiyaç duyduğunuz tam görüntüyü çekin ve hızlı başlangıç için eşlik eden çekme ve çalıştırma örneklerine bakın.

*Son güncelleme: 2026-07-01*

**Önkoşullar:** Docker Engine 20.10 veya sonraki bir sürümün kurulu olduğundan ve geçerli bir Aspose.Cells Cloud lisans anahtarınızın olduğundan emin olun. Görüntüler, belirtilen Windows Sunucusu sürümleri veya Linux x64 için derlenmiştir.

## Windows Sunucusu 2016 Görüntüleri ##

Etiketler | Mimari | Dockerfile | Açıklama
---|---|---|---
✅ `ltsc2016.23.5.0` | x64 | Dockerfile yayınlanmamıştır – derleme ayrıntıları için [yayın notlarına](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2016) bakın. | Windows Sunucusu 2016 için daha yeni bir etiket planlanmamıştır; bu, yayınlanan son sürümüdür.

```bash
docker pull aspose/cells:ltsc2016.23.5.0
docker run -d --name cells-ws2016 -p 8080:80 aspose/cells:ltsc2016.23.5.0
```

Ek kaynaklar: [Docker indirme](/cells/docker/downloads/), [Yayın notları](/cells/release-notes/), [Önkoşullar](/cells/docker/prerequisites/).  
Daha fazla ayrıntı için [Docker Genel Bakış](/cells/docker/) sayfasına bakın.

## Windows Sunucusu 2019 Görüntüleri ##

Etiketler | Mimari | Dockerfile | Açıklama
---|---|---|---
✅ `ltsc2019.25.10.0` | x64 | Dockerfile yayınlanmamıştır – derleme ayrıntıları için [yayın notlarına](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2019) bakın. | —
```bash
docker pull aspose/cells:ltsc2019.25.10.0
docker run -d --name cells-ws2019 -p 8080:80 aspose/cells:ltsc2019.25.10.0
```

Ek kaynaklar: [Docker indirme](/cells/docker/downloads/), [Yayın notları](/cells/release-notes/), [Önkoşullar](/cells/docker/prerequisites/).  
Daha fazla ayrıntı için [Docker Genel Bakış](/cells/docker/) sayfasına bakın.

## Windows Sunucusu 2022 Görüntüleri ##

Etiketler | Mimari | Dockerfile | Açıklama
---|---|---|---
✅ `ltsc2022.25.10.0` | x64 | Dockerfile yayınlanmamıştır – derleme ayrıntıları için [yayın notlarına](https://github.com/aspose-cells/dockerfiles/tree/main/ltsc2022) bakın. | —
```bash
docker pull aspose/cells:ltsc2022.25.10.0
docker run -d --name cells-ws2022 -p 8080:80 aspose/cells:ltsc2022.25.10.0
```

Ek kaynaklar: [Docker indirme](/cells/docker/downloads/), [Yayın notları](/cells/release-notes/), [Önkoşullar](/cells/docker/prerequisites/).  
Daha fazla ayrıntı için [Docker Genel Bakış](/cells/docker/) sayfasına bakın.

## Linux Görüntüleri ##

Etiketler | Mimari | Dockerfile | Açıklama
---|---|---|---
✅ `linux.25.10.0` | x64 | Dockerfile yayınlanmamıştır – derleme ayrıntıları için [yayın notlarına](https://github.com/aspose-cells/dockerfiles/tree/main/linux) bakın. | —
```bash
docker pull aspose/cells:linux.25.10.0
docker run -d --name cells-linux -p 8080:80 aspose/cells:linux.25.10.0
```

Ek kaynaklar: [Docker indirme](/cells/docker/downloads/), [Yayın notları](/cells/release-notes/), [Önkoşullar](/cells/docker/prerequisites/).  
Daha fazla ayrıntı için [Docker Genel Bakış](/cells/docker/) sayfasına bakın.

**Sürüm değişiklikleri günlükçesi**

Etiket | Değişiklikler
---|---
`ltsc2016.23.5.0` | Windows Sunucusu 2016 için son sürüm; güvenlik yamalarını ve performans iyileştirmelerini içerir.
`ltsc2019.25.10.0` | Aspose.Cells 25.10.0’a güncellendi; yeni formül desteği ve hata düzeltmeleri ekledi.
`ltsc2022.25.10.0` | 2019 etiketiyle aynıdır, Windows Sunucusu 2022 çalışma zamanı için optimize edilmiştir.
`linux.25.10.0` | Aspose.Cells 25.10.0 içeren temel Linux görüntüsü; güncellenmiş bağımlılıkları ve Linux’a özel iyileştirmeleri içerir.
---