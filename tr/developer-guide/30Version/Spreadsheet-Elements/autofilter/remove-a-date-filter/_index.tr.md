---
title: "Tarih Filtresi Sil – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Tarih filtresini sil"
type: docs
url: /tr/autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, tarih filtresi sil, Excel Otomatik Filtre, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından tarih filtresini nasıl sileceğinizi öğrenin.uç nokta, parametreler, HTTPS cURL örneği, yanıt yükü ve SDK kod örneklerini içerir."
ArticleTitle: "Tarih Filtresi Sil – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, bir Excel çalışma sayfasında bir tarih filtresini siler.

**Ön Gereksinimler:** Geçerli bir JWT belirtecinize sahip olduğunuzdan, çalışma kitabının Aspose Cloud deposunda depolandığından ve çalışma sayfasını değiştirme yetkinizin olduğundan emin olun.

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı        | Tür     | Konum  | Açıklama                                                                                      |
|----------------------|---------|--------|-----------------------------------------------------------------------------------------------|
| name                 | string  | path   | Excel dosyasının adı.                                                                         |
| sheetName            | string  | path   | Çalışma sayfası adı.                                                                          |
| fieldIndex           | integer | query  | Filtrenin uygulanacağı sütunun sıfır tabanlı dizini.                                          |
| dateTimeGroupingType | string  | query  | Tarih filtresi için gruplama türü (örn. Yıl, Ay, Gün).                                        |
| year                 | integer | query  | Filtrenin yıl bileşeni (varsayılan 0).                                                        |
| month                | integer | query  | Filtrenin ay bileşeni (varsayılan 0).                                                         |
| day                  | integer | query  | Filtrenin gün bileşeni (varsayılan 0).                                                        |
| hour                 | integer | query  | Filtrenin saat bileşeni (varsayılan 0).                                                       |
| minute               | integer | query  | Filtrenin dakika bileşeni (varsayılan 0).                                                     |
| second               | integer | query  | Filtrenin saniye bileşeni (varsayılan 0).                                                     |
| folder               | string  | query  | Dosyanın bulunduğu depodaki klasör yolu.                                                      |
| storageName          | string  | query  | Aspose Cloud deposunun adı.                                                                   |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

API, silme işleminin sonucunu belirten standart HTTP durum kodlarını döndürür.

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | OK | Tarih filtresi başarıyla silindi; yanıt işlem durumunu içerir. |
| 400 | Bad Request | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error | Beklenmeyen sunucu hatası. |

## SDK’lar ile DeleteWorksheetDateFilter API Nasıl Kullanılır

### DeleteWorksheetDateFilter API Belirtimi

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI Belirtimi</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
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

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yönetir, böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
---