---
title: "Depolama Kullanmadan Veri İçe Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Depolama kullanmadan veri içe aktar"
type: docs
url: /tr/import/without-using-storage/
aliases: [  /tr/import-data-in-excel-worksheet-without-using-storage/ ]
keywords: "Aspose.Cells, Cloud API, depolama kullanmadan veri içe aktar, Excel içe aktarma API’si, REST ile içe aktarma"
description: "Aspose.Cells Cloud API ile bir Excel çalışma kitabına depolama kullanmadan veri nasıl içe aktarılacağını öğrenin. İstek biçimi, parametreler, cURL örneği, SDK kodu ve hata yönetimi içerir."
weight: 10
ArticleTitle: "Depolama Kullanmadan Veri İçe Aktar – Aspose.Cells Cloud API"
---

Excel veri içe aktarma işlemi, sonuç üzerinde birçok faktörün etkili olabilmesi nedeniyle karmaşık olabilir. Bu faktörlerin tümü **içe aktarma** süreci sırasında dikkate alınmalıdır. Aspose.Cells Cloud, çeşitli formatları ve veri türlerini profesyonel kalitede bir Excel dosyasına içe aktarmayı kolaylaştırır.

Bu REST API, bir Excel dosyasına **veri** içe aktarır.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür            | Konum       | Açıklama                                                                                                                                      |
| -------------- | -------------- | ----------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| file           | dosya          | formData    | Yüklenecek Excel dosyası.                                                                                                                     |
| ImportOption   | ImportOption   | JSON gövdesi | İçe aktarılacak verileri, türlerini (örneğin `IntArray`, `DoubleArray`, `StringArray`) ve çalışma sayfasındaki yerleştirilme konumunu tanımlayan JSON nesnesi. |

**ImportOption** parametreleri, **ImportData seçeneği referansı** [/cells/import/#import-data-option-parameter](/cells/import/#import-data-option-parameter) kısmında açıklanmıştır.

**Ön Koşullar:**  
Geçerli bir JWT belirteci önceden oluşturulmuş olmalı ve dosya boyutu hizmet sınırını (genellikle 100 MB) aşmamalıdır. Desteklenen dosya formatları: XLS, XLSX, CSV ve ODS. Programlı erişimi tercih ediyorsanız uygun SDK’nın yüklü olduğundan emin olun.

### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                                 |
|-----|-----------------------------|--------------------------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.           |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü).   |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                                       |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyutu sınırı aşılmıştır.                             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                          |

**Notlar:**  
İsteği gönderirken `Content-Type: multipart/form-data` başlığı, `-F` bayrağı tarafından otomatik olarak ayarlanır. Büyük yükler için, içe aktarmadan önce verileri sıkıştırmayı düşünün ve geçici hatalar için yeniden deneme mantığı uygulayın.

## SDK’lar ile PostImportData API’sini Nasıl Kullanılır

### PostImportData API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostImport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/import" \
  -X POST \
  -H "Authorization: Bearer <jwt_token>" \
  -F "file=@file.xlsx" \
  -F "ImportOption={\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"ImportDataType\":\"IntArray\"}"
```

*`-F` bayrağı, `Content-Type: multipart/form-data` başlığını otomatik olarak ayarlar.*

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Status":"OK",
  "Code":200
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve size proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostImportData.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostImportData.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostImportData.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostImportData.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostImportData.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostImportData.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostImportData.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostImportData.go" >}}

{{< /tab >}}

{{< /tabs >}}