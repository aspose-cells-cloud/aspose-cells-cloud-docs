---
title: Aspose.Cells Bulut Web API - Uzak Elektronik Tabloda Çalışma Sayfası İçeriğini Ara
second_title: Documen
ArticleTitle: Search Worksheet Content in Remote Spreadshee
linktitle: Uzaktan Çalışma Sayfası İçeriğini Ara
type: docs
url: /tr/search-content-in-remote-worksheet/
keywords: Excel API, Search Remote Worksheet, Cloud Spreadsheet, REST API, Search Text, Aspose.Cells, Document Search, Spreadsheet AP
description: Bulutta depolanan uzak bir elektronik tablonun çalışma sayfasında metni verimli bir şekilde arayın
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel çalışma sayfasındaki tüm boş hücreleri eşleştir, Uzaktan Çalışma Sayfası Arama
---
Bulut depolama alanında saklanan uzak bir elektronik tablonun çalışma sayfasında belirtilen metni arayın.

## **Arayüz Ayrıntıları**

## **Uzaktan Çalışma Sayfasında İçerik Ara**

```
PUT http://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|Aranacak çalışma kitabı dosyasının adı.|
|çalışma sayfası|Sicim|Yol|Çalışma sayfasının adı.|
|aramaMetni|Sicim|Sorgu|Aranacak metin.|
|ignoringCase|Boolean|Sorgu|Arama sırasında büyük/küçük harf ayrımının dikkate alınıp alınmayacağını belirtir.|
|dosya|Sicim|Sorgu|Çalışma kitabının saklandığı klasör yolu.|
|depolamaAdı|Sicim|Sorgu|(İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama alanının adı. Belirtilmezse varsayılan depolama alanı kullanılır.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için şifre.|

### **Cevap**

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink",
        },
      }
    },
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

## API nolu E-Tablonun çalışma sayfasında Arama içeriğini nerede kullanmalıyız?

E-tablonun çalışma sayfasında içerik araması yapmanız gerektiğinde API numarasını kullanabilirsiniz.

## API numaralı E-Tablonun çalışma sayfasındaki Arama içeriğini neden kullanmalısınız?

- API ile uzaktan bir elektronik tablo çalışma sayfasındaki içeriği zahmetsizce arayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'lar ile API E-Tablosunun Çalışma Sayfasında Bozuk Bağlantıları Arama Özelliğinin Nasıl Kullanılacağı

### OpenAPI Spesifikasyonu

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimlerine olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, temel ayrıntıları ele alarak, minimum kodla hücreler için çalışma sayfalarındaki veya elektronik tablolardaki içerik aramalarını kolayca gerçekleştirmenize olanak tanır.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:
