---
title: "Bir Excel Çalışma Sayfasına Tarih Filtresi Ekle"
second_title: "Belge"
linktitle: "Tarih filtresi ekle"
type: docs
url: /tr/autofilter/add-date-filter/
aliases:
  - /tr/add-date-filter-in-a-worksheet/
  - /tr/autofilter/add-a-date-filter/
description: "Aspose.Cells Cloud REST API’si (v3.0) ile bir Excel çalışma sayfasına tarih filtresi nasıl ekleyeceğinizi öğrenin. cURL örneği, SDK kod parçacıkları (C#, Java, Python vb.), parametreler ve hata işleme içerir."
weight: 65
ArticleTitle: "Bir Excel Çalışma Sayfasına Tarih Filtresi Ekle | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel tarih filtresi, AutoFilter API, REST API, bulut SDK, cURL, elektronik tablo otomasyonu"
---

Bu REST API, bir Excel çalışma sayfasına bir **tarih filtresi** ekler.

**Önkoşullar:** Geçerli bir JWT belirteciniz olmalı ve hedef çalışma kitabının zaten belirtilen depolama konumunda bulunuyor olması gerekir. İstek, JSON gövdesi gerektirmez.

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri


| Parametre Adı            | Tür      | Konum   | Açıklama                                                                                                                                                             |
| ------------------------ | -------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string   | Yol     | Çalışma kitabının adı.                                                                                                                                                |
| **sheetName**            | string   | Yol     | Çalışma sayfasının adı.                                                                                                                                               |
| **range**                | string   | Sorgu   | Filtrenin uygulanacağı Excel aralığı (örn., `A1:B1`).                                                                                                                |
| **fieldIndex**           | integer  | Sorgu   | Filtrelenecek sütunun sıfır tabanlı indeksi.                                                                                                                         |
| **dateTimeGroupingType** | string   | Sorgu   | Tarih/saat filtresi için gruplandırma türü. İzin verilen değerler: `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Değerler büyük/küçük harfe duyarlıdır; varsayılan: `Day`. |
| **year**                 | integer  | Sorgu   | Filtre değeri için yıl bileşeni.                                                                                                                                      |
| **month**                | integer  | Sorgu   | Filtre değeri için ay bileşeni.                                                                                                                                       |
| **day**                  | integer  | Sorgu   | Filtre değeri için gün bileşeni.                                                                                                                                      |
| **hour**                 | integer  | Sorgu   | Filtre değeri için saat bileşeni.                                                                                                                                     |
| **minute**               | integer  | Sorgu   | Filtre değeri için dakika bileşeni.                                                                                                                                   |
| **second**               | integer  | Sorgu   | Filtre değeri için saniye bileşeni.                                                                                                                                   |
| **matchBlanks**          | boolean  | Sorgu   | Boş hücrelerin dahil edilip edilmeyeceği (`true` veya `false`).                                                                                                      |
| **refresh**              | boolean  | Sorgu   | Uygulamadan sonra filtre yenilensin mi? (`true` veya `false`).                                                                                                       |
| **folder**               | string   | Sorgu   | Orijinal çalışma kitabının bulunduğu klasör yolu.                                                                                                                     |
| **storageName**          | string   | Sorgu   | Depolama hizmetinin adı.                                                                                                                                             |

*PUT isteği, istek gövdesi gerektirmez; tüm parametreler sorgu dizgisinde sağlanır.*

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.          |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü).     |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                                       |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                                  |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                           |

## PutWorksheetDateFilter API’yi SDK’lar ile Nasıl Kullanılır

### PutWorksheetDateFilter API Spesifikasyonu


<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
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



### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkânı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}