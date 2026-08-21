---
title: "Aspose.Cells Cloud Klasör Kopyalama API'si – Bulutta Klasörlerin Hızlı Kopyalanması"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Dosyası Yönetimi Çözümü – Aspose.Cells Klasör Kopyalama API'sinin Toplu Kopyalama Özelliklerinin Detaylı Açıklaması"
linktitle: "Klasör Kopyala"
type: docs
url: /copy-folder/
keywords: "Klasör Kopyala, Aspose.Cells Cloud, REST API, Bulut Depolama, Elektronik Tablo Yönetimi"
description: "Aspose.Cells Cloud deposunda tek bir REST çağrısıyla klasörlerin nasıl kopyalanacağını öğrenin.uç nokta, parametreler, örnek istekler, hata kodları ve SDK örneklerini içerir."
weight: 100
---

**CopyFolder** API'si, Aspose.Cells Cloud deposunda mevcut bir klasörü kopyalar. Bu işlem, manuel dosya taşıma yapmadan yedekler oluşturma, verileri yeniden düzenleme veya ileri işlem için bir klasör hiyerarşisi hazırlama amacıyla faydalıdır.

## **Excel API: Klasör Kopyala**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### CopyFolder API'si aşağıdaki parametreleri kabul eder

| Parametre Adı     | Gerekli  | Tür    | Konum (Yol/Sorgu) | Açıklama                                                             |
| ----------------- | -------- | ------ | ----------------- | -------------------------------------------------------------------- |
| `srcPath`         | Evet     | Dize   | Yol               | Kopyalanacak kaynak klasörün yolu.                                   |
| `destPath`        | Evet     | Dize   | Sorgu             | Yeni klasörün oluşturulacağı yol.                                    |
| `srcStorageName`  | Hayır    | Dize   | Sorgu             | Kaynak klasörü içeren depo adı.                                      |
| `destStorageName` | Hayır    | Dize   | Sorgu             | Klasörün kopyalanacağı hedef depo adı.                               |

### Örnek Yanıt

Başarılı bir çağrı, boş JSON gövdesiyle **HTTP 200** döndürür:

```json
{}
```

**Örnek cURL isteği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                        |
| ---- | --------------------- | --------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.   |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                              |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                            |
| 500  | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                      |

## OpenAPI Specification (OpenAPI Spesifikasyonu)

[OpenAPI Specification](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istek nasıl atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}
SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları yöneterek proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web servislerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}