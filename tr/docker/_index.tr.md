---
title: "Aspose.Cells Cloud Docker İşletim Kılavuzu: Aspose.Cells Cloud uygulamasını kendi özel altyapınızda barındırın."
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Docker İşletim Kılavuzu"
linktitle: "Docker"
type: docs
url: /tr/docker-developer-guide/
aliases: [  /tr/docker/ , /tr/docker/run/ ]
description: "Aspose.Cells Cloud’u özel veya kendi altyapınızda Docker konteyneri olarak dağıtın; böylece Aspose’un ortak bulutunu kullanmadan elektronik tablo işleme (Excel, PDF, CSV, JSON, Markdown) yapabilirsiniz."
keywords:
  [
    "Aspose.Cells Cloud",
    "Docker",
    "Docker Görüntüsü",
    "Elektronik Tablo API’si",
    "Excel",
    "PDF",
    "CSV",
    "JSON",
    "Markdown",
    "Özel Bulut",
    "Dağıtım",
  ]
weight: 30
---

Aspose.Cells Cloud, Excel gibi formatlardaki dosyaların oluşturulması, düzenlenmesi, dönüştürülmesi ve manipüle edilmesini destekleyen, bulut tabanlı bir elektronik tablo işleme hizmetidir. Docker dağıtımıyla bağımsız bir hizmet ortamı olarak hızlıca kurulabilir; böylece bağımlılık yönetimi ve platformlar arası dağıtım süreçleri basitleştirilir.

Bu kılavuz, ortam hazırlığından hizmet doğrulamasına kadar tüm işlem adımlarını ayrıntılı olarak açıklamaktadır.

## Ortam Hazırlığı

Aspose.Cells Cloud Docker konteynerini dağıtmadan önce, eksik bileşenler nedeniyle dağıtım hatalarını önlemek için yerel ortamın aşağıdaki bağımlılık gereksinimlerini karşıladığından emin olun.

### Temel bağımlılık bileşenleri

- **Docker Motoru:** Konteynerlerin oluşturulması ve yönetilmesinden sorumlu konteyner çalışma zamanı temel motoru. Minimum sürüm gereksinimi **18.09.0**’dır.
- **İşletim Sistemleri:** Docker’ı destekleyen ana akım işletim sistemleri

  | İşletim Sistemi Türü | Sürüm                     |
  | :-------------------- | :------------------------ |
  | Windows               | Windows 10/11             |
  | Windows Server        | 2016 / 2019 / 2022        |
  | Linux                 | CentOS 7+ / Ubuntu 20.04+ |

- **Donanım kaynakları:** Hizmetin yetersiz kaynaklar nedeniyle çökmesini önlemek için yeterli kaynak sağlayın.
  - CPU: 2 çekirdek veya daha fazla.
  - Bellek: 4 GB veya daha fazla.
  | Disk: 10 GB boş alan. |

### Temel önkoşullar

- **Aspose Lisansı:** Geçerli bir lisans almak için Aspose resmi hesabı oluşturun (deneme sürümü başvurusunda bulunabilir veya ticari sürümü satın alabilirsiniz). Lisans olmadan hizmet işlevselliği kısıtlanabilir. Daha fazla bilgi için [Lisans](https://purchase.aspose.com/buy) sayfasına bakınız.
- **Ağ Bağlantısı:** Dağıtım ortamının Docker Hub’a erişebildiğinden (görüntüleri çekmek için) emin olun.

## Aspose.Cells Cloud Docker Görüntüsünü Edinin

Aspose.Cells Cloud görüntüsü Docker Hub’ta barındırılmakta olup, manuel olarak derlemeye gerek kalmadan doğrudan `docker pull` komutuyla çekilebilir.

```bash
# Linux
docker pull aspose/cells-cloud:linux.22.2.0
docker pull aspose/cells-cloud:latest
```

```powershell
# Windows
docker pull aspose/cells-cloud:ltsc2019.25.9.0
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

## Aspose.Cells Cloud Docker Konteynerini Çalıştırın

### Çalıştırma Parametreleri

| Adı                         | Açıklama                                                                           | Açıklama                                                       |
| --------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------ |
| LicensePublicKey            | Ölçülü faturalandırma modunu kullandığınızda lisansın ortak anahtarını ayarlar.    | Yalnızca Ölçülü faturalandırma modu benimsendiğinde geçerlidir.     |
| LicensePrivateKey           | Ölçülü faturalandırma modunu kullandığınızda lisansın özel anahtarını ayarlar.     | Yalnızca Ölçülü faturalandırma modu benimsendiğinde geçerlidir.     |
| storagesCredentialsFilePath | Depolama yapılandırma dosyasının yolu. Varsayılan dosya `./storageResource.json` |                                                              |
| LicenseFile                 | LicenseFile faturalandırma modunu kullandığınızda lisans dosyasını ayarlar.        | Yalnızca LicenseFile faturalandırma modu benimsendiğinde geçerlidir. |
| AccessToken                 | API’ye erişim için belirteç.                                                       | Boşsa, belirteç doğrulaması gerekmez.                 |

### Çalıştırma Komutu

Konteyneri deneme modunda çalıştırmak şu kadar basittir:

```bash
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

Tüm işlevselliği elde etmek için bir [Ölçülü lisans](https://purchase.aspose.com/faqs/licensing/metered/) edinin ve dosya depolama için bir ana bilgisayar klasörünü bağlayın. Bu durumda çalıştırma komutu şu şekilde olur:

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```windows
docker run -d \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2022.25.9.0
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```linux
docker run -d \
  -p 47900:5000 \
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=./storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:linux.25.9.0
```

{{< /tab >}}

{{< /tabs >}}

### API Referansı – Aspose.Cells Cloud Docker

- `<https://hostname:port/swagger>`
- `<https://hostname:port/swagger/ui/index.html>`

### Portu Dışa Aktarın

| Port | Açıklama                                | Gerekli |
| ---- | ---------------------------------------- | -------- |
| 5000 | Belgeleri oluşturmak için kullanılan yazı tiplerinin bulunduğu klasör | true     |

### Gerekli birimler

| Konteynerdeki bağlama yolu | Açıklama                                | Gerekli | Açıklama                                                         |
| -------------------------- | ---------------------------------------- | -------- | -------------------------------------------------------------- |
| C:\fonts                   | Belgeleri oluşturmak için kullanılan yazı tiplerinin bulunduğu klasör | false    | Eksik yazı tipleri nedeniyle elektronik tablo/Excel sorunlarını çözer.     |
| C:\data                    | Dosya depolama klasörü                  | false    | Daha kolay dosya yönetimi ve erişimi için depolama alanını artırır. |

## Referans Belgesi

- [Aspose.Cells Cloud Docker Konteyneri Temel Özellikleri](https://docs.aspose.cloud/cells/docker-container-features/)
- [Aspose.Cells Cloud Docker Konteyneri depolama nasıl yapılandırılır?](https://docs.aspose.cloud/cells/docker/storage/)
- [Aspose.Cells Cloud Docker konteyneri nasıl çalıştırılır?](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)