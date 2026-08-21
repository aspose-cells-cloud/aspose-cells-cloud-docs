---
title: "Excel dosyalarından meta veri alın"
second_title: "Belge"
linktitle: "Depolama kullanmadan alın"
type: docs
url: /tr/metadata/get/
keywords: "Aspose.Cells, Excel, meta veri, REST API, bulut SDK"
description: "Aspose.Cells Cloud REST API ile Excel çalışma kitaplarından yerleşik veya özel meta verileri alın. İstek formatını, parametreleri, örnek SDK kodunu ve hata işleme içerir."
weight: 23
ArticleTitle: "Excel dosyalarından meta veri alın - Aspose.Cells Cloud API"
---

Bu REST API, bir veya daha fazla Excel dosyasından **meta veri** alır.  
İstek, OAuth 2.0 istemci kimlik bilgileri akışı aracılığıyla elde edilen `Authorization: Bearer <access_token>` başlığını içermelidir.

**Önkoşullar**: Bu uç noktayı çağırmak için Aspose Cloud OAuth 2.0 belirteç uç noktasından alınan geçerli bir erişim belirteciniz olmalıdır. Belirteç almak için örnek curl isteği:

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
     -H "Content-Type: application/x-www-form-urlencoded" \
     -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>"
```

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/get
```

### Sorgu Parametresi

| Parametre Adı | Tür   | Açıklama                                                                |
| ------------- | ----- | ----------------------------------------------------------------------- |
| type          | string | `ALL` / `BuiltIn` / `Custom` – Hangi meta veri gruplarının döndürüleceğini belirtir. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür       | Açıklama                                                       |
| ------------- | --------- | -------------------------------------------------------------- |
| Excel dosyası | veri dosyası | İsteğin çok parçalı kısmının ilk parçası olarak verilen Excel dosyası. |

### Yanıt

```json
[
  {
    "Name": "Author",
    "Value": "John Doe",
    "BuiltIn": true,
    "IsReadOnly": false
  },
  {
    "Name": "CustomProp1",
    "Value": "Custom Value",
    "BuiltIn": false,
    "IsReadOnly": false
  }
]
```

| Kod | Anlam                   | Durum                                |
|-----|-------------------------|--------------------------------------|
| 200 | Başarılı                | Meta veri döndürüldü.                |
| 400 | Hatalı İstek            | Dosya eksik veya sorgu geçersiz.     |
| 401 | Yetkisiz                | Geçersiz veya eksik belirteç.        |
| 404 | Bulunamadı              | Belirtilen dosya bulunamadı.         |
| 500 | İç Sunucu Hatası        | Beklenmeyen sunucu hatası.           |

API, uygun durumlarda bu standart HTTP durum kodlarını ve bir hata yanıt JSON nesnesini birlikte döndürür.

### Bulut SDK Ailesi

Bir SDK kullanmak, düşük seviye ayrıntıları işleyerek geliştirme sürecini hızlandırır. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’larla Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}