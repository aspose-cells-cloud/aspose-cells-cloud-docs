---
title: Aspose.Cells Cloud Web API - Uzak Elektronik Tablodaki İçeriği Değiştir
second_title: Documen
ArticleTitle: Replace Content in Remote a Spreadshee
linktitle: Uzak Elektronik Tablo İçeriğini Değiştir
type: docs
url: /tr/replace-content-in-remote-spreadsheet/
keywords: Replace content, remote spreadsheet, Excel API, REST API, cloud storage, text replacemen
description: Excel API'i kullanarak uzak elektronik tablolardaki metni verimli bir şekilde değiştirin
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel'deki içeriği değiştir, Bulut tabanlı metin değiştirme, Uzak elektronik tablodaki metni değiştir
---
Uzak bir elektronik tablo dosyasında belirtilen metni verimli bir şekilde değiştirin.

## **Uzak Elektronik Tablodaki İçeriği Değiştir API**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| isim| Sicim| Yol| Değiştirilecek çalışma kitabı dosyasının adı.|
| aramaMetni| Sicim| Sorgu| E-tabloda aranacak metin.|
| Metni değiştir| Sicim| Sorgu| Bulunan örneklerin yerine geçecek metin.|
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

## Uzaktan E-Tablo API'de İçeriği Değiştir'i nerede kullanmalıyız?

Uzaktaki bir elektronik tabloda içeriği değiştirmeniz gerektiğinde API'i kullanabilirsiniz.

## Uzaktan E-Tablo API'deki İçeriği Değiştir özelliğini neden kullanmalısınız?

- Uzaktaki elektronik tablolardaki içeriği hızla değiştirin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## Uzak E-Tablo API'deki İçeriği Değiştir özelliğinin SDK'larla nasıl kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/ReplaceContentInRemoteSpreadsheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, hücrelerdeki içerikleri elektronik tablolarda minimum kodla kolayca değiştirmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
