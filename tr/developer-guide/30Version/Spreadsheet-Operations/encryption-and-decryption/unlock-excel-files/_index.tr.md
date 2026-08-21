---
title: "Excel Dosyalarını Kilidini Açın"
second_title: "Belge"
linktitle: "Excel Dosyalarını Kilidini Açın"
type: docs
url: /unlock-excel-files/
aliases: [/unlock/without-storage/, /unlock/, /unlock/without-using-storage/]
keywords: "Excel Kilidini Aç, Aspose.Cells Cloud, REST API, Excel kilidini açma, şifreli çalışma kitaplığı, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Aspose.Cells Cloud REST API, şifre korumalı Excel dosyalarının kilidini açmak için bir uç nokta sağlar. SDK’lar, Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift dahil olmak üzere birden fazla programlama dili için mevcuttur."
ArticleTitle: "Aspose.Cells Cloud REST API ile Excel Dosyalarını Kilidini Açın"
weight: 70
---

Bu REST API, Excel dosyalarının kilidini açar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

### İstek parametreleri

| Parametre Adı | Tür     | Konum                  | Açıklama                                       |
|---------------|---------|------------------------|------------------------------------------------|
| file          | dosya   | formData (HTTP gövdesi) | Yüklenecek dosya                               |
| password      | string  | sorgu dizisi           | Dosyanın kilidini açmak için şifre (korumalıysa) |

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklü dosya boyut limitini aşıyor. |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |

## SDK’lar ile PostUnlock API’sini Nasıl Kullanılır?

### PostUnlock API Belirtimi

[OpenAPI Belirtimi](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)’nu inceleyin.

**Notlar**  
- API, tek bir istekte birden fazla Excel dosyasının kilidini açabilir; her dosya yanıtın `Files` dizisinde döndürülür.  
- Uyumluluk sorunlarını önlemek için SDK sürümünüzün API sürümüyle (`v3.0`) eşleştiğinden emin olun.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}