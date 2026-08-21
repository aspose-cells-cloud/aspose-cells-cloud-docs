---
title: "Çalışma Sayfası Arka Plan Resmini Ekleme veya Silme – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Arka Plan"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud, çalışma sayfası arka planı, Excel API, arka plan resmi ekleme, çalışma sayfası arka planını silme, SDK örnekleri"
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasına arka plan resmi eklemeyi veya kaldırmayı öğrenin. İstek sözdizimi, Java, .NET, Python, PHP için SDK örnekleri ve hata yönetimi içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API ile Çalışma Sayfası Arka Plan Resmini Ekleme veya Silme"
---

## Excel çalışma sayfasında arka plan ile çalışma

**Genel Bakış:** Bir çalışma sayfası arka planı, çalışma sayfası hücrelerinin arkasında görünen bir resimdir; markalaştirme veya görsel ipuçları için kullanışlıdır. Aspose.Cells Cloud API, bu arka plan resmini programlı olarak eklemenizi veya silmenizi sağlar.

**Önkoşullar:**  
- Geçerli Aspose.Cells Cloud erişim belirteci (OAuth 2.0).  
- Bulutta depolanan bir Excel çalışma kitabı.  
- Arka plan için bir resim dosyası (PNG, JPEG, BMP).

- **Arka plan ekle** – Bir çalışma sayfasına arka plan resmi ayarlayın. Ayrıntılı kılavuz için bkz. [Excel çalışma sayfasına arka plan nasıl ayarlanır](/cells/worksheets/background/add/).  
- **Arka plan sil** – Bir çalışma sayfasından mevcut bir arka plan resmini kaldırın. Ayrıntılı kılavuz için bkz. [Excel çalışma sayfasından arka plan nasıl silinir](/cells/worksheets/background/delete/).

Bir çalışma sayfası arka planı kullanmak, markalaştırmayı geliştirebilir, önemli bölümleri vurgulayabilir veya son kullanıcılar için görsel ipuçları sağlayabilir. Aspose.Cells Cloud API, bu arka plan resmini doğrudan uygulamanızdan ayarlamayı veya temizlemeyi kolaylaştırır.

### API referansı

| İşlem | HTTP Yöntemi | Uç Nokta | Yol parametreleri | İstek gövdesi | Başarılı yanıt |
|-------|-------------|----------|----------------|--------------|----------------|
| Arka plan ekle | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – çalışma kitabı dosya adı<br>`sheetName` – hedef çalışma sayfası | Görüntü dosyası (PNG, JPEG, BMP), multipart/form‑data olarak | `200 OK` – arka plan uygulandı |
| Arka plan sil | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – çalışma kitabı dosya adı<br>`sheetName` – hedef çalışma sayfası | *hiçbiri* | `200 OK` – arka plan kaldırıldı |

#### Örnek (Java SDK)

```java
// Arka plan resmi ekle
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Arka plan resmini sil
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Örnek (Python SDK)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# Arka plan ekle
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Arka plan sil
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

Ek dil örnekleri (C#, PHP, Ruby) için SDK belgelerine bakınız.

**İlgili konular**  
- Çalışma sayfalarını genel olarak yönetme hakkında daha fazla bilgi edinin: [Çalışma sayfalarına genel bakış](/cells/worksheets/).  
- Aspose.Cells Cloud ile kimlik doğrulama nasıl yapılır anlayın: [API kimlik doğrulama kılavuzu](/cells/authentication/).  
- Grafikler, tablolar ve formüller gibi diğer elektronik tablo öğelerini inceleyin: [Elektronik tablo öğeleri dizini](/cells/elements/).
---