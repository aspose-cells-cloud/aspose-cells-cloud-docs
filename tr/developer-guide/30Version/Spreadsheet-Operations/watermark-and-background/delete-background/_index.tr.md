---
title: "Excel Çalışma Kitabından Arkaplanı Silme"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells arkaplan silme, Excel API arkaplan silme, Aspose.Cells Cloud, DELETE /cells background"
description: "Aspose.Cells Cloud API kullanarak bir Excel çalışma kitabından arkaplan görüntüsünü kaldırın. Gerekli parametreler, cURL örneği ve C#, Java, Python ve diğerleri için SDK kodu ile DELETE uç noktasını öğrenin."
weight: 170
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Kitabından Arkaplan Görüntüsünü Silme"
---

Bu REST API, bir Excel çalışma kitabının arkaplan görüntüsünü siler.

## DeleteWorkbookBackground API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **Sorgu Parametreleri**

| Parametre Adı | Tür   | Açıklama                                     | Gerekli |
| -------------- | ------ | ------------------------------------------- | -------- |
| folder         | string | Orijinal çalışma kitabının bulunduğu klasör. | Hayır    |
| storageName    | string | Kullanılacak depolama hizmetinin adı.       | Hayır    |

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Hatalı İstek (Bad Request)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT jetonu. |
| 413  | Yük Çok Büyük (Payload Too Large) | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası (Internal Server Error) | Beklenmeyen sunucu hatası. |

## SDK’lar ile DeleteWorkbookBackground API Nasıl Kullanılır?

### DeleteWorkbookBackground API Spesifikasyonu

<a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, gerekli kimlik doğrulama başlığıyla tam bir DELETE isteğini göstermektedir; istek gövdesine gerek yoktur.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, düşük seviye ayrıntıları işler ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}