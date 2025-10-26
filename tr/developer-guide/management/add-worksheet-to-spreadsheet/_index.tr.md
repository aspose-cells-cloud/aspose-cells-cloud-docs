---
title: Aspose.Cells Cloud Webb API - Bir Çalışma Sayfasını Elektronik Tabloya Ekleme
second_title: Documen
ArticleTitle: Add a Worksheet to a Spreadshee
linktitle: Çalışma Sayfasını Elektronik Tabloya Ekle
type: docs
url: /tr/add-worksheet-to-spreadsheet/
keywords: Aspose.Cells Cloud Web API, Add Worksheet, Spreadsheet Management, RES
description: Aspose.Cells Cloud Web API, geliştiricilerin bir çalışma kitabına yeni bir çalışma sayfasını verimli bir şekilde eklemelerine olanak tanır ve çalışma sayfasının türü, konumu ve adı üzerinde kontrol sağlar. Bu işlevsellik, çalışma kitabı yönetimini ve esnekliğini artırır.
weight: 100
kwords: Excel, Office Bulut, REST, Elektronik Tablo, PDF, CSV, JSON, Markdown, Excel Çalışma Sayfalarını Yönetme, Dinamik Elektronik Tablo Oluşturma
---
Çalışma sayfasının türünü ve yerini belirterek elektronik tabloya çalışma sayfası ekleme.

|**Çalışma Sayfası Türü** | Tanım|
|:- |:- |
|**VB** | Visual Basic modülü|
|**Çalışma sayfası** | Çalışma sayfası|
|**Çizelge** | Grafik sayfası|
|**BIFF4Makro** | BIFF4 Makro sayfası|
|**UluslararasıMakro** | Uluslararası Makro sayfası|
|**Diğer** | Uluslararası Makro sayfası|
|**Diyalog** | Diyalog çalışma sayfası|

## **Çalışma Sayfasını Elektronik Tabloya Ekle API**

```http
PUT http://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
|Elektronik tablo|Dosya|FormVerileri|E-tablo dosyasını yükleyin.|
|sayfa türü|Sicim|Sorgu|Yeni çalışma sayfasının adını belirtir. Belirtilmezse, varsayılan bir ad atanacaktır.|
|konum|Tam sayı|Sorgu|Yeni çalışma sayfasının ekleneceği konumu belirtir. Belirtilmezse, çalışma sayfası çalışma kitabının sonuna eklenir.|
|sayfaAdı|Sicim|Sorgu|Eklenecek çalışma sayfası türünü belirtir. Belirtilmezse, varsayılan çalışma sayfası türü kullanılır.|
|çıkış yolu|Sicim|Sorgu|(İsteğe bağlı) Çalışma kitabının saklandığı klasör yolu. Varsayılan değer null'dır.|
|outStorageName|Sicim|Sorgu|Çıktı dosyası depolama adı.|
|bölge|Sicim|Sorgu|E-tablo bölge ayarı.|
|şifre|Sicim|Sorgu|E-tablo dosyasını açmak için şifre.|

### **Cevap**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Çalışma Sayfasını Elektronik Tabloya Ekle API'i nerede kullanmalıyız?

Bir elektronik tabloya çalışma sayfası eklemeniz gerektiğinde API numarasını kullanabilirsiniz.

## API Çalışma Sayfasını Elektronik Tabloya Ekleme özelliğini neden kullanmalısınız?

- Çalışma sayfasının türünü ve konumunu belirterek elektronik tabloya bir çalışma sayfası ekleyin.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Çalışma Sayfasını Elektronik Tabloya Ekleme API Nasıl Kullanılır

### Çalışma Sayfasını Elektronik Tabloya Ekleme API Spesifikasyonu

 The[Çalışma Sayfasını Elektronik Tabloya Ekleme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, kısa kodla bir çalışma sayfasını bir elektronik tabloya eklemenize olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerine API çağrılarının nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
