---
title: "Excel Çalışma Sayfasına En Yüksek 10 Filtresi Ekleme (Aspose.Cells Cloud)"
ArticleTitle: "Excel Çalışma Sayfasına En Yüksek 10 Filtresi Ekle – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "En yüksek 10 filtresi ekle"
type: docs
url: /tr/autofilter/add-top-10-filter/
aliases:
  [/tr/filter-the-top-10-items-in-the-list/, /tr/autofilter/add-a-top-10-filter/]
keywords: "Aspose.Cells, Otomatik Filtre, En yüksek 10 filtresi, Excel API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasına En Yüksek 10 Otomatik Filtresi nasıl uygulanacağını öğrenin. Uç nokta, parametreler, HTTPS cURL örneği, kimlik doğrulama ayrıntıları, hata işleme ve C#, Java, Python ve diğerleri için SDK kod parçacıklarını içerir."
weight: 65
---

Bu REST API, listedeki **En Yüksek 10** öğeyi filtreler.

> **Ön Gereksinimler**  
> • Aspose.Cells Cloud kimlik doğrulaması kullanarak geçerli bir JWT belirteci edinin.  
> • Excel çalışma kitabını Aspose Cloud depolarınıza yükleyin (veya bulunduğu depo/klasörü belirtin).  
> • Filtrelemek istediğiniz çalışma sayfası adını ve hücre aralığını bilin.

## PutWorksheetFilterTop10 API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filterTop10
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı   | Tür      | Konum   | Gerekli | Varsayılan | Açıklama                                                                 |
| ---------------- | -------- | ------- | ------- | --------- | -------------------------------------------------------------------------- |
| **name**         | string   | path    | Evet    | —         | Excel dosyasının adı.                                                     |
| **sheetName**    | string   | path    | Evet    | —         | Verileri içeren çalışma sayfasının adı.                                   |
| **range**        | string   | query   | Evet    | —         | Filtrenin uygulanacağı hücre aralığı (örn. `A1:B10`).                     |
| **fieldIndex**   | integer  | query   | Evet    | —         | Filtrenin uygulanacağı sütunun sıfır tabanlı dizini.                      |
| **isTop**        | boolean  | query   | Evet    | `true`    | Üst öğeleri filtrelemek için `true`; alt öğeler için `false`.             |
| **isPercent**    | boolean  | query   | Hayır   | `false`   | `itemCount` değerinin yüzde olarak değerlendirilmesi için `true`; mutlak sayı için `false`. |
| **itemCount**    | integer  | query   | Hayır   | `10`      | Filtrede yer alacak öğe sayısı.                                            |
| **matchBlanks**  | boolean  | query   | Hayır   | `false`   | Filtre sonuçlarına boş hücrelerin dahil edilmesi için `true`.             |
| **refresh**      | boolean  | query   | Hayır   | `false`   | Uygulamadan sonra filtre yenilemek için `true`.                           |
| **folder**       | string   | query   | Hayır   | —         | Excel dosyasının bulunduğu depo klasörü.                                  |
| **storageName**  | string   | query   | Hayır   | —         | Aspose Cloud deposunun adı.                                               |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**Olası hata yanıtları**

```json
{
    "Code":400,
    "Message":"Geçersiz İstek – eksik veya geçersiz parametreler."
}
```

```json
{
    "Code":401,
    "Message":"Yetkisiz – geçersiz veya eksik JWT belirteci."
}
```

```json
{
    "Code":413,
    "Message":"İstek Boyutu Çok Büyük – yüklenen dosya izin verilen boyutu aşıyor."
}
```

```json
{
    "Code":500,
    "Message":"Sunucu İç Hatası – beklenmeyen sunucu koşulu."
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                   |
| 413 | İstek Boyutu Çok Büyük      | Yüklenen dosya boyut limitini aşıyor.                |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                           |

## PutWorksheetFilterTop10 API’yi SDK’larla Nasıl Kullanılır?

### PutWorksheetFilterTop10 API Specification

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilterTop10), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filterTop10?range=A1:B10&fieldIndex=0&isTop=true&itemCount=10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak geliştirmenin en hızlı yoludur. SDK, düşük seviye ayrıntıları işler, böylece projenize odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilterTop10.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilterTop10.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilterTop10.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilterTop10.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilterTop10.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilterTop10.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilterTop10.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilterTop10.go" >}}

{{< /tab >}}

{{< /tabs >}}