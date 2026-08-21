---
title: "Bir Excel Çalışma Sayfasından Bir Filtre Silme – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Filtreyi sil"
type: docs
url: /delete-filter/
aliases: [/delete-a-filter-for-a-filter-column/, /delete-auto-filter/]
keywords: "Aspose.Cells Cloud filtre silme, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API, cURL ve SDK’lar (C#, Java, Python vb.) kullanarak bir Excel çalışma sayfasından Otomatik Filtre’yi nasıl sileceğinizi öğrenin.uç nokta, parametreler, kimlik doğrulama ve örnek kod içerir."
weight: 100
---

## REST API

Bu REST API, bir Excel çalışma sayfasındaki bir **Otomatik Filtre**'yi siler.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı          | Tür      | Konum | Gerekli mi? | Açıklama                                                                                 |
| ---------------------- | -------- | ----- | ----------- | ---------------------------------------------------------------------------------------- |
| **name**               | string   | Yol   | Evet        | Çalışma kitabının adı.                                                                   |
| **sheetName**          | string   | Yol   | Evet        | Çalışma sayfasının adı.                                                                  |
| **range**              | string   | Sorgu | Hayır       | Filtrenin uygulanacağı hücre aralığı (örneğin, `A1:C10`).                               |
| **fieldIndex**         | integer  | Sorgu | Evet        | Filtrenin uygulandığı sütunun sıfır tabanlı indeksi.                                    |
| **dateTimeGroupingType** | string | Sorgu | Hayır       | Tarih/saat değerlerinin nasıl gruplandığı: `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. |
| **year**               | integer  | Sorgu | Hayır       | Tarih gruplaması için yıl bileşeni.                                                      |
| **month**              | integer  | Sorgu | Hayır       | Tarih gruplaması için ay bileşeni.                                                       |
| **day**                | integer  | Sorgu | Hayır       | Tarih gruplaması için gün bileşeni.                                                      |
| **hour**               | integer  | Sorgu | Hayır       | Tarih gruplaması için saat bileşeni.                                                     |
| **minute**             | integer  | Sorgu | Hayır       | Tarih gruplaması için dakika bileşeni.                                                   |
| **second**             | integer  | Sorgu | Hayır       | Tarih gruplaması için saniye bileşeni.                                                   |
| **matchBlanks**        | boolean  | Sorgu | Hayır       | `true` / `false` – Boş hücrelerin filtrede dahil edilip edilmeyeceği.                   |
| **refresh**            | boolean  | Sorgu | Hayır       | `true` / `false` – Silme işleminden sonra çalışma sayfasının yenilenip yenilenmeyeceği. |
| **folder**             | string   | Sorgu | Hayır       | Orijinal çalışma kitabının klasörü.                                                      |
| **storageName**        | string   | Sorgu | Hayır       | Depo adı.                                                                                |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                           |

## SDK’larla DeleteWorksheetFilter API’yi Nasıl Kullanılır

### DeleteWorksheetFilter API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL kullanarak Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
  -X DELETE \
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

SDK kullanmak, geliştirmeyi hızlandırmanın en etkili yoludur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkânı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerine çeşitli SDK’lar kullanarak nasıl istekte bulunulacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}