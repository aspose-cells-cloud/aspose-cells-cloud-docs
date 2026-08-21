---
title: "Excel Raporu Oluşturma İçin Veri Birleştirme"
second_title: "Belge"
linktype: "Veri Birleştirme"
type: docs
url: /tr/assembly-data-for-the-creation-of-an-excel-report/
aliases: [  /tr/assembly/ ]
keywords: "Aspose.Cells, Excel raporu, veri birleştirme, Bulut API, REST, SDK, cURL, PDF, ODS"
description: "Aspose.Cells Cloud’un Assembly API’sini kullanarak Excel (XLSX, PDF, ODS) raporlarına veri nasıl birleştireceğinizi öğrenin. Endpoint, parametreler, cURL örneği, SDK kodu, kimlik doğrulama kılavuzu ve hata işleme içerir."
weight: 40
---

Bu REST API, veriyi bir Excel dosyasına **birleştirir**.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/assembly
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri


| Parametre Adı | Tür   | Konum                      | Açıklama                                                          |
| -------------- | ------ | ------------------------- | ----------------------------------------------------------------- |
| file           | dosya  | formData (multipart body) | Yüklenecek elektronik tablo dosyası.                              |
| DataSource     | string | sorgu dizisi               | Birleştirmek için gerekli verileri sağlayan veri kaynağının tanımlayıcısı. |
| format         | string | sorgu dizisi               | İstenen çıktı formatı (örn., `xlsx`, `pdf`).                      |

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[dosya2 adı]",
    "Filesize" : [dosya boyutu],
    "FileContent" : "[Base64Dize]"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|------|-----------------------------|----------------------------------------------------|
| 200  | Tamam (OK)                  | Süzgeç başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                 |
| 413  | İçerik Çok Büyük            | Yüklenen dosya boyut sınırını aşıyor.              |
| 500  | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                         |

## SDK’larla PostAssemble API’sini Nasıl Kullanılır

### PostAssemble API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostAssemble), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca ulaşmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/assembly?DataSource=ds&format=pdf" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'template=@template.xlsx' \
  -F 'data=@data.json'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "rapor1",
      "FileSize": 274022,
      "FileContent": "-----Base64Dize--------"
    },
    {
      "Filename": "rapor2",
      "FileSize": 274022,
      "FileContent": "-----Base64Dize--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, API’ye karşı geliştirme yapmanın en hızlı yoludur. SDK, düşük seviyeli detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAssemble.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAssemble.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAssemble.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAssemble.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAssemble.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAssemble.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAssemble.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAssemble.go" >}}

{{< /tab >}}

{{< /tabs >}}