---
title: "Aspose.Cells Cloud API – Disk Kullanımını Al | Gerçek Zamanlı Depolama Metrikleri"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Dosyası Yönetimi Çözümü – Bulutta disk kullanımını hızlı bir şekilde almak için arayüz."
linktype: "Disk Kullanımını Al"
type: docs
url: /tr/get-disk-usage/
keywords: "Aspose Cells, Bulut API, Disk Kullanımı, Depolama Metrikleri, Excel, REST"
description: "Aspose.Cells Cloud için gerçek zamanlı disk kullanımını alın. GET /v4.0/cells/storage/disk uç noktasını, gerekli kimlik doğrulamayı ve örnek yanıtı öğrenin."
weight: 100
---

**Disk Kullanımını Al** işlemi, Aspose.Cells Cloud hesabınız için gerçek zamanlı depolama metriklerini döndürür. Bu uç noktayı, harcanan ve toplam disk alanını izlemek için kullanın.

- Aspose Cloud ortamında Excel API'si için mevcut disk kullanımını alır.
- Geliştiricilerin uygulamalarının ne kadar depolama alanı tükettiğini izlemesine olanak tanır.
- Depolama sınırlarını ve maliyet kontrolünü önceden yönetmeyi sağlar.

## Excel API: GetDiskUsage

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/storage/disk
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama                                                     | Gerekli |
| -------------- | ------ | -------- | ------------------------------------------------------------ | -------- |
| storageName    | String | Sorgu    | Kullanımı alınacak depolamanın adı.                         | İsteğe Bağlı |

### **Yanıt**

```json
{
  "Name": "DiskUsage",
  "Description": ["Disk alanı bilgisi için sınıf."],
  "Type": "Sınıf",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "UsedSize",
      "Description": ["Uygulama tarafından kullanılan disk alanı miktarı."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    },
    {
      "Name": "TotalSize",
      "Description": ["Toplam kullanılabilir disk alanı."],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Long",
        "Name": "long"
      }
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                           |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Başarılı              | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500  | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                        |

## OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/StorageController/GetDiskUsage), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/disk?storageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "UsedSize": 12345678,
  "TotalSize": 10737418240
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerine çeşitli SDK’lar kullanılarak nasıl istek yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_GetDiskUsage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_GetDiskUsage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_GetDiskUsage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_GetDiskUsage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_GetDiskUsage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_GetDiskUsage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_GetDiskUsage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_GetDiskUsage.go" >}}
{{</tab>}}
{{< /tabs >}}