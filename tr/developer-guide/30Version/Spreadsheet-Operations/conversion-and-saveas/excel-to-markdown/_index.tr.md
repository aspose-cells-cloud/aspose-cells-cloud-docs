---
title: "Excel Dosyasını Markdown'a Dönüştür"
second_title: "Belge"
linktitle: "Excel'den Markdown'a"
type: docs
url: /tr/convert-excel-file-to-markdown-file/
keywords: "Excel, Markdown, dönüştürme, Aspose.Cells Cloud, REST API, excel'den markdown'a dönüştürme, aspose cells markdown api, excel markdown dışa aktarımı"
description: "Aspose.Cells Cloud REST API ile Excel çalışma sayfalarını Markdown'a dönüştürün – cURL örneği, SDK snippet’leri, gerekli parametreler ve kimlik doğrulama ayrıntılarını içerir."
weight: 100
ArticleTitle: "Excel Dosyasını Markdown’a Dönüştür – Aspose.Cells Cloud API Dokümantasyonu"
---

Bu REST API, bir elektronik tablo dosyasını Markdown formatlı bir dosyaya dönüştürür.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/markdown
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Sorgu Parametreleri


| Parametre Adı         | Tür    | Konum   | Açıklama                                                                                          |
| --------------------- | ------ | ------- | ------------------------------------------------------------------------------------------------- |
| password              | string | query   | Excel dosyasını açmak için gerekli şifre.                                                         |
| storageName           | string | query   | Dosyanın bulunduğu depo adı.                                                                      |
| checkExcelRestriction | bool   | query   | Hücreleri veya ilgili nesneleri düzenlerken Excel'e özgü kısıtlamaların uygulanıp uygulanmayacağını belirtir. |
| datafile              | file   | body    | Çok parçalı içerikte ilk parça olarak yüklenmesi gereken Excel dosyası.                           |

### Yanıt

API, **FileInfo** türünde bir JSON nesnesi döndürür:

- **FileInfo** – Oluşturulan Markdown dosyasının adını, boyutunu ve base64 ile kodlanmış içeriğini içeren nesne.

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

### Hata Yanıtları

| HTTP Kodu | Açıklama                                          | Örnek JSON Gövdesi                              |
| --------- | ------------------------------------------------- | ----------------------------------------------- |
| 401       | Yetkisiz – eksik veya geçersiz belirteç.         | `{"error":"Invalid access token."}`             |
| 400       | Geçersiz İstek – gerekli parametre eksik veya dosya formatı geçersiz. | `{"error":"The 'datafile' field is required."}` |
| 500       | İç Sunucu Hatası – beklenmeyen sunucu sorunu.     | `{"error":"An unexpected error occurred."}`     |



## SDK’lar ile PostConvertWorkbookToMarkdown API Nasıl Kullanılır

### PostConvertWorkbookToMarkdown API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToMarkdown), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```shell
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/markdown" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "File=@your_excel_file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.md",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları ele aldığı için iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToMarkdown.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToMarkdown.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToMarkdown.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToMarkdown.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToMarkdown.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToMarkdown.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToMarkdown.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToMarkdown.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Bu İşlevi Gerçekleştiren Diğer API’ler

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Excel dosyasını ek ayarlarla HTML olarak kaydeder ve sonucu depolar.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel dosyasını ek seçeneklerle HTML’e dönüştürür ve sonucu yanıtta döndürür.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel dosyasını alır ve isteğe bağlı ayarlarla HTML’e dönüştürebilir.