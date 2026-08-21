---
title: "Aspose.Cells Cloud PHP SDK – Excel Dosyalarını Dönüştürün, Birleştirin, Bölün, Koruyun"  
second_title: "Belge"  
ArticleTitle: "Aspose.Cells Cloud PHP SDK – Excel Dosyalarını Dönüştürün, Birleştirin, Bölün, Koruyun"  
linktitle: "Aspose.Cells Cloud PHP SDK"  
type: docs  
url: /available-sdks/aspose-cells-cloud-php/  
description: "Aspose.Cells Cloud PHP SDK’sini (v24.3) indirin. Composer üzerinden nasıl kurulacağını, kimlik doğrulaması nasıl yapılacağını, XLSX’i PDF/CSV’ye dönüştürmeyi, çalışma kitaplarını birleştirmeyi, sayfaları korumayı ve daha fazlasını öğrenin – Office kurmadan bunların hepsini yapın."  
keywords: "Aspose.Cells, Bulut, PHP, SDK, Excel, Dönüştür, Birleştir, Böl, Koru"  
weight: 30  
---  

Bu SDK açık kaynaklıdır ve MIT Lisansı altında lisanslanmıştır. Aspose.Cells Cloud için PHP kütüphanesinin kaynak koduna <a href="https://github.com/aspose-cells-cloud/aspose-cells-cloud-php" target="_blank" rel="noopener noreferrer">buradan</a> ulaşabilirsiniz.

# **Aspose.Cells Cloud SDK for PHP Nasıl Kullanılır**

Aspose.Cells Cloud SDK for PHP, geliştiricilerin Microsoft Excel dosyalarını **PHP programlama dili** kullanarak işlemesini ve işlemesini sağlayan güçlü bir kütüphanedir. Bu SDK ile, yerel makinenize ek yazılım veya bağımlılıklar kurmadan bulutta Excel belgeleri oluşturabilir, düzenleyebilir ve dönüştürebilirsiniz.

Bu makalede, Aspose.Cells Cloud SDK for PHP ile bazı yaygın görevleri nasıl gerçekleştireceğimizi inceleyeceğiz; örneğin yeni bir Excel çalışma kitabı oluşturma, hücrelere veri ekleme ve değiştirilmiş çalışma kitabını buluta kaydetme.

## Başlangıç

Aspose.Cells Cloud SDK for **PHP** kullanmaya başlamadan önce geliştirme ortamınızı kurmanız ve gerekli bağımlılıkları yüklemeniz gerekir. İstemci kimliğiniz ve istemci gizli anahtarınızı almak için Aspose web sitesindeki <a href="https://docs.aspose.cloud/cells/quickstart/" target="_blank" rel="noopener noreferrer">makaleye</a> bakın.

**Önkoşullar**

- PHP 7.4 veya üzeri  
- Geliştirme makinenizde Composer yüklü  
- Geçerli Aspose Cloud istemci kimliği ve istemci gizli anahtarı  
- Aspose Cloud depolama konumuna erişim (varsayılan veya özel)  

## Aspose.Cells Cloud için PHP paketi nasıl yüklenir

Aspose.Cells Cloud SDK for PHP’yi yükleyebilirsiniz. Aşağıda adımlar yer almaktadır:

- `composer.json` dosyanıza Aspose.Cells Cloud’u bağımlılık olarak ekleyin:

   ```json
   {
       "require": {
           "aspose/cells-cloud": "^24.3"
       }
   }
   ```

- SDK’yı yüklemek için Composer güncellemesini çalıştırın:

   ```bash
   composer install
   ```

- PHP kodunuzda Composer’in otomatik yükleyicisini ekleyin:

   ```php
   require 'vendor/autoload.php';
   ```

## PHP paketi ile Xlsx’i diğer formatlara dönüştürme

- Aspose.Cells Cloud Kitaplığını İçe Aktar  
  Öncelikle Aspose.Cells Cloud PHP SDK’sından projenize gerekli paketi içe aktarın.

- Kimlik Bilgileri ile API İstemcisini Yapılandırma  
  API istemcinizi benzersiz istemci kimliğiniz ve istemci gizli anahtarınız ile kimlik doğrulaması yapın.

- Dönüştürme Parametrelerini Hazırlama  
  Dönüştürme görevi için kaynak dosya adı, istenen çıktı formatı ve depolama klasör yolu gibi parametreleri tanımlayın.

- Çalışma Kitabı Dönüştürmesini Gerçekleştirme  
  `PostConvertWorkbook` yöntemini kullanarak dönüştürme işlemini çağırın ve yanıtı işleyin.

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_AvailableSDKs.php" >}}

### `PostConvertWorkbook` için API Referansı

| Parametre      | Açıklama                                     | Tür    | Gerekli |
|----------------|----------------------------------------------|--------|---------|
| `file`         | Kaynak Excel dosyasının adı (örn. `sample.xlsx`). | string | Evet    |
| `format`       | İstenen çıktı formatı (`pdf`, `csv`, `png`, vb.). | string | Evet    |
| `storage`      | Kaynak dosyanın bulunduğu depo adı veya klasör yolu. | string | Hayır   |
| `outPath`      | Dönüştürülmüş dosyayı doğrudan depoda kaydetmek için isteğe bağlı yol. | string | Hayır   |

**HTTP Yöntemi:** POST  
**Uç Nokta:** `/cells/convert/{format}`  

**Yanıt Örneği (JSON)**  

```json
{
  "status": "OK",
  "url": "https://api.aspose.cloud/v3.0/cells/convert/output.pdf"
}
```

**Durum Kodları**

- `200` – Dönüştürme başarılı.  
- `400` – Geçersiz istek (eksik veya geçersiz parametreler).  
- `401` – Kimlik doğrulama başarısız.  
- `500` – Sunucu hatası.  
---