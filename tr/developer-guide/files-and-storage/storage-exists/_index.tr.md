---
title: "Bir Depolamanın Var olup Olmadığını Kontrol Edin – Aspose.Cells Cloud API (v4.0)"
second_title: "Belge"
ArticleTitle: "Bulut Tabanlı Excel Dosyası Yönetimi – Depolama Varlığını Kontrol Etme"
linktitle: "Depolama Var"
type: docs
url: /tr/storage-exists/
keywords: "Aspose.Cells, depolama var, bulut depolama API'si, REST, Excel"
description: "Aspose.Cells Cloud'da bir depolama kapsayıcısının varlığını doğrulayın. GET /v4.0/cells/storage/{storageName}/exist uç noktasını, gerekli parametreleri, yanıt formatını öğrenin ve C#, Java, Python ve diğerleri için SDK örneklerini görün."
weight: 100
---

`storageExists` API'si, belirtilen bir depolamanın Aspose.Cells bulut hizmetinde olup olmadığını kontrol eder. Bu işlevsellik, depolamaya bağlı tüm işlemlerin hata olmadan yürütülmesini sağlamak açısından kritik öneme sahiptir.
**Özet** – `storageExists` uç noktası, Aspose.Cells Cloud'da belirli bir depolama kapsayıcısının mevcut olup olmadığını doğrulamanızı sağlar. Çalışma zamanı hatalarını önlemek için dosya ile ilgili işlemlerden önce kullanın.

## Depolama Varlığını Kontrol Etme (storageExists)

### Web API'si

```
GET https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama                                           |
| ------------- | ----- | ----- | -------------------------------------------------- |
| storageName   | String | Yol   | Varlığı kontrol edilecek depolamanın adı.         |

### **Yanıt**

```json
{
  "Name": "StorageExist",
  "Description": ["Belirtilen depolamanın var olup olmadığını gösterir."],
  "Type": "Class",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "Exists",
      "Description": [
        "Depolamanın var olup olmadığını gösterir.",
        "Bu özellik, depolama mevcutsa true; aksi takdirde false değerini döndürür."
      ],
      "Nullable": true,
      "ReadOnly": false,
      "IsInherit": false,
      "DataType": {
        "Identifier": "Boolean",
        "Name": "boolean"
      }
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413 | İçerik Çok Büyük      | Yüklenecek dosya boyut sınırını aşar.                             |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                       |

## storage exists API'sini SDK’larla Nasıl Kullanılır?

### OpenAPI Specification

<a href="https://reference.aspose.cloud/cells/#/StorageController/StorageExists" rel="nofollow noopener noreferrer">OpenAPI Specification</a>, geliştiricilerin REST API ile doğrudan web tarayıcısından sorunsuz şekilde etkileşime geçmesini sağlayacak şekilde tanımlanmış herkese açık bir programlama arayüzüdür.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istek yapmayı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/{storageName}/exist" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Exists": true
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanımı, geliştirme sürecini hızlandırmak için en verimli yaklaşımdır. Bir SDK, düşük seviyeli uygulama detaylarını soyutlayarak geliştiricilerin proje görevlerine odaklanmasını sağlar. Mevcut Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="nofollow noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerine API istekleri yapmayı göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_StorageExists.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_StorageExists.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_StorageExists.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_StorageExists.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_StorageExists.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_StorageExists.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_StorageExists.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_StorageExists.go" >}}
{{</tab>}}
{{< /tabs >}}