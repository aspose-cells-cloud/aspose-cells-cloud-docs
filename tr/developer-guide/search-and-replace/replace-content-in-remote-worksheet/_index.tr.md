---
title: Aspose.Cells Cloud Web API - Uzak Elektronik Tablodaki Çalışma Sayfası İçeriğini Değiştir
second_title: Documen
ArticleTitle: Replace Worksheet Content in Remote a Spreadshee
linktitle: Uzak Çalışma Sayfası İçeriğini Değiştir
type: docs
url: /tr/replace-content-in-remote-worksheet/
keywords: Aspose.Cells Cloud Web API, Replace Content, Remote Worksheet, Cloud Spreadsheet, Text Replacement, Office Cloud Integratio
description: Aspose.Cells API'i kullanarak uzak bir elektronik tablonun çalışma sayfasındaki metni verimli bir şekilde değiştirin
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir, ReplaceContentInRemoteWorksheet
---
Uzak bir elektronik tablo dosyasının çalışma sayfasında belirtilen metni verimli bir şekilde değiştirin.

## **Uzak Çalışma Sayfasındaki İçeriği Değiştir API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/replace/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| isim| Sicim| Yol| Değiştirilecek çalışma kitabı dosyasının adı.|
| çalışma sayfası| Sicim| Yol| Değiştirme için çalışma sayfasını belirtin.|
| aramaMetni| Sicim| Sorgu| Çalışma sayfasında aranacak metin.|
| Metni değiştir| Sicim| Sorgu| Aranan metnin yerine konulacak metin.|
| dosya| Sicim| Sorgu| Çalışma kitabının saklandığı klasör yolu.|
| depolamaAdı| Sicim| Sorgu|(İsteğe bağlı) Özel bulut depolama alanı kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanını kullanın.|
| bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

### **Cevap**

```json
{
  "Name": "CellsCloudResponse",
  "Type": "Class",
  "Properties": [
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Uzaktan Çalışma Sayfası API'de Çalışma Sayfasının İçeriğini Değiştir seçeneğini nerede kullanmalıyız?

Uzaktaki bir elektronik tabloda Çalışma Sayfasının içeriğini değiştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Uzaktan Çalışma Sayfasındaki API numaralı Çalışma Sayfasının içeriğini değiştir özelliğini neden kullanmalısınız?

- Uzaktaki elektronik tablolardaki Çalışma Sayfası içeriğini hızla değiştirin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## Uzak Elektronik Tablo API'deki Çalışma Sayfasının İçeriğini SDK'larla Değiştirme Nasıl Kullanılır

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteWorksheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, çalışma sayfalarındaki içerikleri elektronik tablolardaki hücrelere minimum kodla kolayca değiştirmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:
