---
title: "Aspose.Cells Cloud Docker Görüntüsü İndirme"  
second_title: "Belge"  
ArticleTitle: "Aspose.Cells Cloud Docker Görüntüsü İndirme"  
linktitle: "Görüntü İndirme"  
type: docs  
url: /docker/downloads/  
description: "Windows Server 2016/2019 ve Linux için en son Aspose.Cells Cloud Docker görüntülerini edinin. Konteyneri yerel olarak çalıştırmak için adım adım talimatları, ön koşulları ve güvenlik ipuçlarını izleyin."  
weight: 30  
keywords: "Aspose.Cells, Bulut, Docker, konteyner, görüntü, indirme, Windows Server, Linux, REST API"  
---

## Genel Bakış  

`aspose/cells-cloud` – **Aspose.Cells Cloud** REST API’sini barındıran resmi Docker görüntüsüdür. Bu görüntü, Aspose’un kamusal bulut hizmetlerine bağımlı kalmadan, tam bir elektronik tablo işleme motorunu konteyner içinde yerel veya özel bulut dağıtımları olarak çalıştırmanızı sağlar.  

**Son güncelleme tarihi:** 2026‑06‑30  

**Hızlı başlangıç kontrol listesi**

- Docker Motoru sürümünüzün 20.10 veya daha üst versiyonunda olduğundan emin olun.  
- İşletim sisteminize uygun görüntüyü çekin (aşağıdaki bölümlere bakın).  
- `ASPOSE_CLIENT_ID` ve `ASPOSE_CLIENT_SECRET` ortam değişkenlerini ayarlayın.  
- Konteyneri, iç bağlantı noktası 80’e karşılık gelen 8080 bağlantı noktasıyla eşleyerek çalıştırın.  

---  

## Ön Koşullar  

| Gereksinim | Detaylar |
|------------|----------|
| **Docker Motoru** | Docker 20.10 veya daha üst sürüm, ana makine işletim sisteminize kurulu olmalı. |
| **İşletim Sistemi** | Windows Server 2016, Windows Server 2019 veya modern bir Linux dağıtımından herhangi biri. |
| **Docker Hub Erişimi** | Aktif bir Docker Hub hesabı (isteğe bağlıdır ancak özel görüntüler için önerilir). Özel bir depodan çekme yapmanız gerekirse `docker login` komutunu çalıştırın. |
| **Aspose Cloud Kimlik Bilgileri** | `ASPOSE_CLIENT_ID` ve `ASPOSE_CLIENT_SECRET` – bu kimlik bilgilerini Aspose Cloud kontrol panelinden edinin. |

> **İpucu:** Docker kurulumunu `docker --version` komutuyla doğrulayın.  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## Konteyneri Çalıştırma  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Ortam Değişkenleri** – `ASPOSE_CLIENT_ID` ve `ASPOSE_CLIENT_SECRET`, API tarafından gerekli olan kimlik bilgilerini sağlar.  
* **Bağlantı Noktası Eşlemesi** – Konteyner 80 numaralı bağlantı noktasını açar; hizmete erişmek için bunu bir ana makine bağlantı noktasına (örneğin 8080) eşleyin.  
* **Ayırık Mod (`-d`)** – Konteyneri arka planda çalıştırır.  

---  

## Sürümleme ve Güncellemeler  

| İşletim Sistemi | Etiket | Yayınlama Tarihi | En Son Sürümü Alma Yöntemi |
|-----------------|--------|------------------|----------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026‑06‑30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Not:** `21.9` etiketi şu anki kararlı sürümü temsil eder. Daha yeni sürümler için `latest` etiketini kullanın veya [Aspose.Cells Cloud sürüm notlarını](/cells/release-notes/) kontrol edin.  

---  

## Doğrulama ve Güvenlik  

* **Görüntü Özet Kontrolü**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Zafiyet Taraması** (önerilir)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **En İyi Uygulamalar** – Docker’ı güncel tutun, konteynerleri gerekenden daha fazla yetkiyle çalıştırmayın ve bilinen CVE’leri tespit etmek için düzenli olarak görüntüleri taratın.  

* **Yapılandırılmış Veri (JSON‑LD) Örneği**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker Görüntüsü",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## Yaygın Sorunlar ve Sorun Giderme  

| Belirti | Olası Neden | Çözüm |
|---------|-------------|-------|
| `docker: command not found` | Docker kurulu değil veya PATH ayarlanmamış | Docker’ı kurun ve terminali yeniden başlatın. |
| Çekme sırasında kimlik doğrulama hatası | Eksik veya hatalı `docker login` | Geçerli Docker Hub kimlik bilgileriyle `docker login` komutunu çalıştırın. |
| Konteyner hemen kapanıyor | Gerekli ortam değişkenleri eksik | **Konteyneri Çalıştırma** bölümünde gösterildiği gibi `ASPOSE_CLIENT_ID` ve `ASPOSE_CLIENT_SECRET` değerlerini sağlayın. |
| Ana makinede bağlantı noktası çakışması | Ana makine bağlantı noktası zaten kullanımda | Farklı bir ana makine bağlantı noktası seçin (örneğin `-p 8081:80`). |

---  

## Ayrıca Bakınız  

* [Aspose.Cells Cloud API Belgesi](/cells/cloud/api/)  
* [Aspose.Cells Cloud Sürüm Notları](/cells/release-notes/) – 21.9 ve sonraki sürümler için ayrıntılı değişiklik günlüğü.  
* [Aspose.Cells Docker Konteyner Özellikleri](/cells/docker/features/)  
* [Aspose.Cells Docker Görüntüsü Etiketleri](/cells/docker/tag-list/)  

---  

*Yazar: Aspose Cloud Mühendislik Ekibi.*