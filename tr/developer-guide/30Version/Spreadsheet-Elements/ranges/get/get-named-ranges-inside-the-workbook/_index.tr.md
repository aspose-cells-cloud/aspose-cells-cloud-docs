---
title: "Excel Çalışma Kitabından Adlandırılmış Aralıkları Alın"
second_title: "Belge"
linktype: "Ad"
type: docs
url: /ranges/get/name/
aliases: [/get-named-ranges-inside-the-workbook/]
keywords: "adlandırılmış aralıklar, Excel, Aspose.Cells, Bulut API, çalışma sayfaları"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabından adlandırılmış aralıkları alın. İsteği oluşturma detayları, örnek cURL komutları ve birden fazla programlama dilinde SDK örnekleri içerir."
ArticleTitle: "Excel Çalışma Kitabından Adlandırılmış Aralıkları Alın – Aspose.Cells Cloud API"
weight: 10
---

Bu REST API, çalışma sayfaları içinde tanımlanmış adlandırılmış aralıklarla ilgili bilgileri döndürür.

**Arka Plan** – *Adlandırılmış aralık*, bir çalışma sayfasında belirli bir hücreyi veya hücre bloğunu belirten kullanıcı tanımlı bir tanımlayıcıdır. Adlandırılmış aralıklar formül oluşturma işlemini basitleştirir, okunabilirliği artırır ve bir çalışma kitabında sık kullanılan bölgelere programlı erişimi sağlar.

**Gereksinimler** – Aspose.Cells Cloud API'ye erişmek için geçerli bir JWT erişim jetonuna ihtiyaç vardır. Bu jetonu, Aspose Cloud istemci kimliğinizi ve istemci gizli anahtarınızı kullanarak OAuth 2.0 jeton uç noktasından kimlik doğrulaması yaparak edinin. Her istekte bu jetonu `Authorization: Bearer <jwt token>` başlığına ekleyin.

## GetNamedRanges API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/ranges
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamaya</a> ihtiyaç duyar.

### İstek parametreleri

| Parametre Adı | Tür   | Konum         | Açıklama                                       |
| -------------- | ------ | ------------ | -------------------------------------------- |
| name           | string | Yol (Path)   | Excel belgesinin adı.                         |
| folder         | string | Sorgu dizesi | Belgenin bulunduğu klasör.                    |
| storageName    | string | Sorgu dizesi | Belgenin bulunduğu depo adı.                  |

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|------|-----------------------------|--------------------------------------------------|
| 200  | Başarılı (OK)               | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Hatalı İstek (Bad Request)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT jetonu. |
| 413  | Yük Çok Büyük (Payload Too Large) | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | Sunucu İç Hatası (Internal Server Error) | Beklenmeyen sunucu hatası. |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Worksheets/GetNamedRanges), web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlayan herkese açık bir programlama arayüzü tanımlar.

Aspose.Cells web hizmetlerini çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL kullanarak adlandırılmış aralıkları nasıl alacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/ranges" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Ranges": {
    "RangeList": [
      {
        "ColumnCount": 7,
        "ColumnWidth": 8.428571428571429,
        "FirstColumn": 1,
        "FirstRow": 9,
        "Name": "data",
        "RefersTo": "=Sheet1!$B$10:$H$10",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Yanıt Modeli**

| Alan           | Tür     | Açıklama                                             |
|----------------|---------|------------------------------------------------------|
| `ColumnCount`  | tamsayı | Aralıktaki sütun sayısı.                             |
| `ColumnWidth`  | sayı    | Her sütunun genişliği (nokta cinsinden).             |
| `FirstColumn`  | tamsayı | Aralıktaki ilk sütunun sıfır tabanlı indeksi.        |
| `FirstRow`     | tamsayı | Aralıktaki ilk satırın sıfır tabanlı indeksi.        |
| `Name`         | string  | Aralığın kullanıcı tanımlı adı.                      |
| `RefersTo`     | string  | Hücre referansını tanımlayan formül (örneğin, `=Sheet1!$B$10:$H$10`). |
| `RowCount`     | tamsayı | Aralıktaki satır sayısı.                             |
| `RowHeight`    | sayı    | Her satırın yüksekliği (nokta cinsinden).            |
| `Worksheet`    | string  | Aralığı içeren çalışma sayfasının adı.               |

## Bulut SDK Ailesi

Bu işlevselliği entegre etmenin en hızlı yolu, bir SDK kullanmaktır. SDK’lar düşük seviye detayları ele aldığı için iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetNamedRanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetNamedRanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetNamedRanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetNamedRanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetNamedRanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetNamedRanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetNamedRanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetNamedRanges.go" >}}

{{< /tab >}}

{{< /tabs >}}
---