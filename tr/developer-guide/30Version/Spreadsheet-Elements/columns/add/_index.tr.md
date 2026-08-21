---
title: "Excel Çalışma Sayfasına Boş Bir Sütun Ekleyin - Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Ekle"
type: docs
url: /tr/columns/add/
aliases:
  - /add-an-empty-column-in-an-excel-worksheet/
  - /add-an-empty-column-in-a-worksheet/
keywords: "ekle, sütun, Excel, API, Aspose.Cells, Bulut, REST, ekleme"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel sayfasına yeni bir sütun eklemeyi öğrenin. İstek sözdizimi, cURL örneği ve SDK kod örneklerini içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API Kullanarak Excel Çalışma Sayfasına Boş Sütun Ekleyin"
---

Bu REST API, bir çalışma sayfasına bir veya daha fazla sütun ekler.

**Önkoşullar**  
Bu uç noktayı çağırmadan önce aşağıdaki adımları tamamladığınızdan emin olun:

- Geçerli bir OAuth 2.0 erişim belirteci edinin ve bunu `Authorization` başlığında belirtin.  
- Hedef çalışma kitabını seçili depolama alanına (varsayılan = “Default”) kaydedin veya uygun `folder` ve `storageName` parametrelerini belirtin.  
- `sheetName` içinde belirtilen çalışma sayfası adının çalışma kitabında mevcut olduğunu doğrulayın.

## PutInsertWorksheetColumns API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/{columnIndex}?totalColumns=1
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı       | Tür      | Konum  | Açıklama                                                          |
| ------------------- | -------- | ------ | ----------------------------------------------------------------- |
| **name**            | string   | path   | Çalışma kitabının dosya adı.                                       |
| **sheetName**       | string   | path   | Çalışma sayfasının adı.                                            |
| **columnIndex**     | integer  | path   | Eklemenin başlayacağı sütunun sıfır tabanlı indeksi.              |
| **totalColumns**    | integer  | query  | Eklenecek sütun sayısı.                                            |
| **updateReference** | boolean  | query  | **true** ise, hücre referansları ekleme işlemine göre güncellenir. |
| **folder**          | string   | query  | Çalışma kitabının bulunduğu klasörün yolu.                         |
| **storageName**     | string   | query  | Depolama hizmetinin adı.                                           |

**Notlar**

- `columnIndex`, çalışma sayfasındaki mevcut sütun sayısının 0 ile aralığında olmalıdır. Mevcut aralığın dışına ekleme yapmak, sayfanın otomatik olarak genişlemesine neden olur.  
- Birden fazla sütun ekleme (`totalColumns` > 1), mevcut sütunları sağa kaydırır.  
- `updateReference` bayrağının varsayılan değeri `false`tır; formülleri ve adlandırılmış aralıkları güncellemek için `true` olarak ayarlayın.

[OpenAPI Specifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetColumns), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerini çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, kimlik doğrulama ve doğru yol parametresini içeren tam bir isteği göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/1?totalColumns=1&updateReference=true" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: application/json"
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

**Yanıt kodları**

| Kod  | Açıklama                                      |
|------|-----------------------------------------------|
| 200  | Sütun(lar) başarıyla eklendi.                 |
| 400  | Geçersiz istek – eksik veya geçersiz parametreler. |
| 401  | Yetkisiz – geçersiz veya eksik belirteç.      |
| 404  | Çalışma kitabı veya çalışma sayfası bulunamadı. |
| 500  | İç sunucu hatası.                             |

**Örnek hata yanıtları**

```json
// 400 Bad Request – eksik veya geçersiz parametreler
{
  "Code": 400,
  "Message": "Geçersiz parametre: totalColumns pozitif bir tamsayı olmalıdır."
}

// 401 Unauthorized – geçersiz veya eksik belirteç
{
  "Code": 401,
  "Message": "Kimlik doğrulama başarısız. Erişim belirteci eksik veya geçersiz."
}

// 404 Not Found – çalışma kitabı veya çalışma sayfası mevcut değil
{
  "Code": 404,
  "Message": "'test.xlsx' adlı çalışma kitabı bulunamadı."
}

// 500 Internal Server Error
{
  "Code": 500,
  "Message": "Sunucuda beklenmeyen bir hata oluştu."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirmenin en hızlı yoludur. Bir SDK, düşük seviye detayları yöneterek size proje mantığına odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub Deposu</a>'na bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini farklı SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}