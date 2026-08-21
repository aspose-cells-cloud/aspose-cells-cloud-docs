---
title: "Şekilleri Dışa Aktar"
second_title: "Belge"
linktitle: "Şekil"
type: docs
url: /tr/export-excel-shape-to-different-formats/
aliases: [  /tr/export/excel-shape-to-different-formats/ ]
keywords: "Şekilleri Dışa Aktar, Aspose.Cells Cloud, Excel şekil dışa aktarma, Görüntü formatları, REST API, SDK"
description: "Aspose.Cells Cloud REST API'sini ve SDK'larını kullanarak Excel şekillerini çeşitli görüntü formatlarına (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) nasıl dışa aktaracağınızı öğrenin."
weight: 20
ArticleTitle: "Şekilleri Dışa Aktar – Aspose.Cells Cloud"
---

Excel'den şekilleri dışa aktarmak, diyagram içeriğinin platformlar ve uygulamalar arasında yeniden kullanılmasını sağlar. **Önkoşullar:** Geçerli bir JWT erişim jetonu ve yüklenecek kaynak Excel dosyası.

Şekilleri aşağıdaki formatlara dışa aktarabilirsiniz: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Gerekli | Açıklama |
|----------------|--------|-----------------------------|----------|-------------|
| file           | dosya  | formData                    | Evet     | Yüklenecek dosya |
| objectType     | string | sorgu                       | Evet     | Dışa aktarılacak nesne türü. Grafik dışa aktarmak için `chart` kullanın. Geçerli değerler şunları içerir: `shape`, `worksheet`, `picture`, vb. |
| format         | string | sorgu                       | Evet     | İstenen çıktı formatı. Desteklenen değerler: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **İstek Örneği**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Yanıt

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... ek dosya nesneleri ...
  ]
}
```

*Tipik Base64 ile kodlanmış dosya yükleri, görüntü boyutlarına ve formatına bağlı olarak birkaç yondan birkaç megabayta kadar değişebilir.*

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama |
|------|-----------------------|-------------|
| 200  | Tamam                 | Şekiller başarıyla dışa aktarıldı; yanıt dosya listesini içerir. |
| 400  | Hatalı İstek          | Eksik veya geçersiz parametreler. |
| 401  | Yetkisiz              | Geçersiz veya eksik erişim jetonu. |
| 413  | Gövde Çok Büyük       | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası      | Beklenmeyen sunucu hatası. |


## SDK Kullanarak PostExport API Nasıl Kullanılır

### PostExport API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL kullanarak Cloud API'yi nasıl çağıracağınızı göstermektedir.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, Aspose.Cells Cloud ile geliştirmenin en hızlı yoludur. Bir SDK düşük seviyeli ayrıntıları soyutlar ve iş mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}
---