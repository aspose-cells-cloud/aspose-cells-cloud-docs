---
title: "Çalışma Sayfası Hücresi Yorumunu Güncelleme"
type: docs
url: /comments/update/
aliases: [/update-a-comment-in-excel-workbook/]
keywords: "Aspose.Cells Cloud, REST API, Excel, çalışma sayfası, hücre yorumu, çalışma sayfası yorumunu güncelle, yorum nesnesi"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir Excel defterindeki bir hücredeki çalışma sayfası yorumunu güncelleyin; istek detaylarını, yanıt kodlarını ve SDK örneklerini içerir."
weight: 30
ArticleTitle: "Çalışma Sayfası Hücresi Yorumunu Güncelle – Aspose.Cells Cloud API"
---

Bu REST API, bir çalışma sayfası hücresindeki bir yorumu günceller. Bu uç noktayı, bir Excel dosyasında **çalışma sayfası yorumunu güncellemek** için kullanın.

**Ön Gereksinimler:**  
- `Authorization` başlığında geçerli bir OAuth/JWT erişim belirteci bulunmalıdır.  
- Defter, desteklenen bulut depolama konumunda saklanmalıdır (`folder` ve isteğe bağlı olarak `storageName` belirtin).  

## PostWorksheetComment API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür     | Konum | Açıklama                                                                |
| ------------- | ------- | ----- | ----------------------------------------------------------------------- |
| name          | string  | path  | Excel belgesinin adı.                                                   |
| sheetName     | string  | path  | Hücreyi içeren çalışma sayfasının adı.                                  |
| cellName      | string  | path  | Hücrenin adresi (örneğin, **A1**).                                      |
| comment       | object  | body  | Eklenip güncellenecek yorumu tanımlayan bir **Comment** nesnesi.        |
| folder        | string  | query | Belgenin saklandığı klasör.                                             |
| storageName   | string  | query | Depolama hizmetinin adı.                                                |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetComment), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/a1" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "CellName": "a1",
        "Author": "test",
        "HtmlNote": "string",
        "Note": "this is a comment",
        "AutoSize": true,
        "IsVisible": true,
        "Width": 10,
        "Height": 10
      }'
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

Olası yanıt durum kodları:

| Kod  | Açıklama                                         |
|------|--------------------------------------------------|
| 200  | Yorum başarıyla güncellendi.                    |
| 400  | Hatalı istek – eksik veya geçersiz parametreler.|
| 401  | Yetkisiz – kimlik doğrulama başarısız oldu.     |
| 404  | Bulunamadı – defter, çalışma sayfası veya yorum mevcut değil. |
| 500  | İç sunucu hatası.                                |

**Notlar / İpuçları:**  
- Maksimum yorum uzunluğu 1024 karakterdir.  
- Desteklenen karakterler UTF‑8'dir; kontrol karakterlerinden kaçının.  

## Bulut SDK Ailesi

Aspose.Cells Cloud ile hızlıca geliştirme yapmanın en hızlı yolu bir SDK kullanmaktır. Bir SDK, düşük seviye detayları yöneterek size projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetComment.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetComment.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetComment.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetComment.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetComment.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetComment.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetComment.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetComment.go" >}}

{{< /tab >}}

{{< /tabs >}}

İlgili İşlemler:  
- [Çalışma Sayfası Yorumunu Al](/comments/get/)  
- [Çalışma Sayfası Yorumu Ekle](/comments/add/)  
- [Çalışma Sayfası Yorumunu Sil](/comments/delete/)