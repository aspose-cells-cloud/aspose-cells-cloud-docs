---
title: "Excel Çalışma Sayfasına Filtre Ekleyin"
second_title: "Belge"
linktitle: "Filtre ekle"
type: docs
url: /tr/autofilter/add-filter/
aliases: [  /tr/add-a-filter-for-a-filter-column/ ]
keywords: "Aspose.Cells, Bulut, Excel, Otomatik Filtre, Filtre Ekle, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki bir sütuna otomatik filtre nasıl ekleneceğini öğrenin. cURL, SDK örnekleri ve parametre kılavuzu içerir."
weight: 60
ArticleTitle: "Aspose.Cells Cloud Kullanarak Excel Çalışma Sayfasına Filtre Ekleyin"
---

**Ön Gereksinimler:** Bu API'yi çağırmadan önce geçerli bir JWT belirteci edinmelisiniz, hedef çalışma kitabının belirtilen depoya yüklü olduğundan emin olmalısınız ve dosyaya erişim için gerekli izinlere sahip olmalısınız. Komut satırı örnekleri için cURL'in son sürümünü (7.68 veya üzeri) kullanmanız önerilir.

Bu REST API, bir Excel çalışma sayfasındaki belirli bir sütun için bir filtre ekler.

## PutWorksheetFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Güvenlik ve Yetkilendirme**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür     | Konum   | Açıklama |
|----------------|---------|---------|----------|
| name           | string  | Yol     | Çalışma kitabının adı. |
| sheetName      | string  | Yol     | Çalışma sayfasının adı. |
| range          | string  | Sorgu   | Filtreyi içeren hücre aralığı (örneğin, `A1:B1`). |
| fieldIndex     | integer | Sorgu   | Filtrenin uygulanacağı sütunun sıfır tabanlı indeksi. |
| criteria       | string  | Sorgu   | Filtre kriteri (örneğin, bir değer veya ifade). |
| matchBlanks    | boolean | Sorgu   | Filtrede boş hücreleri dahil etmek için `true`, aksi takdirde `false`. |
| refresh        | boolean | Sorgu   | Uygulamadan sonra filtreyi yenilemek için `true`, aksi takdirde `false`. |
| folder         | string  | Sorgu   | Orijinal çalışma kitabının bulunduğu klasör. |
| storageName    | string  | Sorgu   | Depolama hizmetinin adı. |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırnı aşıyor. |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |

## PutWorksheetFilter API’sini SDK’lar ile Nasıl Kullanılır

### PutWorksheetFilter API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetFilter" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?range=A1:B1&fieldIndex=0&criteria=Year" \
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

Bir SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK düşük seviye detayları ele aldığı için siz projenize odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}