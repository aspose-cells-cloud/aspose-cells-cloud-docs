---
title: "Aspose.Cells Cloud Docker Konteynerini Çalıştırın – Çekin, Yapılandırın ve Başlatın"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud Docker Konteyneri Nasıl Çalıştırılır?"
LinkTitle: "Docker Konteyneri"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "Aspose.Cells Cloud Docker konteynerini Windows veya Linux’ta nasıl çekeceğinizi, yapılandıracağınızı ve başlatacağınızı öğrenin. Docker‑Compose YAML, lisans ayarı, bağlantı noktası eşlemesi ve sorun giderme ipuçlarını içerir."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "Docker konteyneri"
  - "Docker Compose"
  - "lisans anahtarları"
  - "Excel"
  - "tablo"
  - "bulut API"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

Docker teknolojisi, hafif konteynerler kullanarak uygulamaların dağıtımını otomatikleştirmek için tasarlanmıştır. Geliştiriciler, bir Docker konteynerini uygulamayı tüm kütüphaneleri ve bağımlılıklarıyla birlikte paketlemek ve her şeyi tek bir paket olarak dağıtmak için kullanabilir.

Aspose.Cells Cloud ekibi, Docker kullanıcılarını kolaylaştırmak amacıyla Docker konteynerini <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a>’da yayımlamıştır.

**Önkoşullar** – Docker Motoru ≥ 20.x’in kurulu olduğundan ve işletim sisteminizin (Windows 10/Server 2019/2022 veya desteklenen bir Linux dağıtımı) gerekleri karşıladığından emin olun. Lisanslı modda çalıştırmak için isteğe bağlı bir lisans anahtarı sağlanabilir.

- Docker Motoru ≥ 20.x kurulu  
- Desteklenen İşletim Sistemi (Windows 10/Server 2019/2022 veya bir Linux dağıtımı)  
- Lisanslı mod için isteğe bağlı lisans anahtarı  

## Konteyner yapılandırması

### Gerekli birimler

| Konteynerdeki bağlama yolu | Açıklama |
| :--- | :--- |
| C:\fonts | Belgelerin işlenmesinde kullanılacak yazı tiplerinin bulunduğu klasör |
| C:\data | Dosya depolama klasörü |

**Linux/macOS alternatifi** – Konteynerde `/fonts` ve `/data` kullanın ve konteyneri çalıştırırken bunları `/home/user/fonts` ve `/home/user/data` gibi ana makine dizinleriyle eşleyin.

### Parametreler

| Ad | Açıklama |
| :--- | :--- |
| LicensePublicKey | Lisansın ortak anahtarı |
| LicensePrivateKey | Lisansın özel anahtarı |

**License** parametreleri atlanırsa uygulama deneme modunda çalışır.

### 1. Aspose.Cells Cloud Görüntüsünü Çekin

```bash
# Aspose.Cells Cloud görüntüsünün belirli bir sürümünü çekin
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Windows Server 2019 için Aspose.Cells Cloud görüntüsünü çekin
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Windows Server 2022 için Aspose.Cells Cloud görüntüsünü çekin
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Windows 11 için Aspose.Cells Cloud görüntüsünü çekin
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Not:** Her zaman en son sürümü almak için `latest` etiketini de çekebilirsiniz: `docker pull aspose/cells-cloud:latest`.

### 2. Docker‑Compose Aracı İçin Yapılandırmalar

Aşağıdaki yapılandırmayı bir **docker‑compose.yml** dosyasına yazabilirsiniz:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # ana makine 5000 → konteyner 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **Not:** `5000:80` bağlantı noktası eşlemesi, API’nin `http://localhost:5000` adresinden erişilebilir olacağı anlamına gelir.

### 3. Komut Satırını Kullanarak Docker Konteynerini Çalıştırın

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Sorun giderme:**  
- **Bağlantı noktası çakışması:** Ana makinede 5000 bağlantı noktasının boş olduğundan emin olun veya kullanılmayan bir bağlantı noktasına eşlemeyi değiştirin.  
- **Lisans yükleme hatası:** Ortağın ve özel anahtarın ortam değişkenleri olarak veya dosyalar olarak doğru şekilde iletilip iletilmediğini doğrulayın.  
- **Yazı tipi eksikliği:** Belgeler yanlış yazı tipleriyle işleniyorsa, yazı tipi dizininin doğru şekilde bağlandığından ve gerekli yazı tipi dosyalarını içerdiğinden emin olun.

**İlgili kaynaklar:**  
- <a href="/cells/api/">API referansı</a> | <a href="/cells/license/">Lisans etkinleştirme kılavuzu</a> | <a href="/cells/getting-started/">Başlangıç genel bakışı</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Aspose.Cells Cloud Docker Konteynerini Çalıştırın",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Docker görüntüsünü çekin",
      "text": "Gerekli görüntüyü indirmek için `docker pull aspose/cells-cloud:<version>` komutunu çalıştırın."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "docker‑compose dosyası oluşturun",
      "text": "`docker‑compose.yml` dosyasında görüntüyü, bağlantı noktalarını, birimleri ve lisans ortam değişkenlerini tanımlayın."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "Konteyneri çalıştırın",
      "text": "Uygun ortam değişkenleri, birim bağlamaları ve bağlantı noktası eşlemesiyle `docker run` komutunu yürütün."
    }
  ]
}
```