---
title: "Excel'i PDF'ye Dönüştür – Aspose.Cells Cloud API"
ArticleTitle: "Excel'i PDF'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Excel'i PDF'ye Dönüştür"
type: docs
url: /tr/convert-excel-file-to-pdf-file/
aliases: [/convert-excel-file-to-pdf-in-cloud/, /convert/excel-to-pdf/]
keywords: "Aspose, Cells, Excel, PDF, dönüştürme, Bulut API"
description: "Aspose.Cells Cloud REST API ile Excel çalışma kitaplarını PDF'ye nasıl dönüştüreceğinizi öğrenin. cURL, SDK örnekleri (C#, Java, Python) ve kimlik doğrulama kılavuzunu içerir."
weight: 80
---

Bu REST API, bir hesap tablosu dosyasını PDF formatlı bir dosyaya dönüştürür. **Önkoşullar:** Geçerli bir JWT erişim belirteci edinin, kaynak Excel dosyasının desteklenen bir depoda saklandığından emin olun ve dönüştürme uç noktasını çağırmak için gerekli izinlere sahip olun.

## PostConvertWorkbookToPDF API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **Sorgu Parametresi**

| Parametre Adı         | Tür   | Açıklama                                                                        |
| :-------------------- | :----- | :------------------------------------------------------------------------------ |
| password              | string | Excel dosyasını açmak için şifre.                                                |
| storageName           | string | Dosyanın bulunduğu deponun adı.                                                  |
| checkExcelRestriction | bool   | Hücreyle ilgili nesneleri değiştirirken Excel dosyası kısıtlamalarının uygulanıp uygulanmayacağını belirtir. |

`checkExcelRestriction` değeri atlanırsa varsayılan olarak `false` olur.

### **İstek Gövdesi Parametresi**

| Parametre Adı | Tür  | Açıklama                                                        |
| :------------ | :--- | :-------------------------------------------------------------- |
| datafile      | file | Çok parçalı içerikin ilk parçası olarak kaydedilen veri dosyası. |

### **Yanıt**

[FileInfo](/tr/cells/file-info/)

Yanıt, dosya meta verilerini içeren bir JSON nesnesi döndürür. PDF dosyası kendisi sağlanan `FileContent` (base64) kullanılarak veya `FileInfo` bağlantısı aracılığıyla indirilebilir. API, **FileInfo** türünde bir JSON nesnesi döndürür:

- **FileInfo** – Oluşturulan **PDF** dosyasının adını, boyutunu ve base64 ile kodlanmış içeriğini içeren nesne.

```json
{
  "Filename": "example.pdf",
  "FileSize": 12345,
  "FileContent": "base64_encoded_string"
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

## PostConvertWorkbookToPDF API’sini SDK’larla Nasıl Kullanılır

### PostConvertWorkbookToPDF API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPDF), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

**İstek Başlıkları**

| Başlık         | Tür   | Açıklama                                              |
| :------------- | :----- | :----------------------------------------------------- |
| Authorization  | string | JWT kimlik doğrulamasıyla elde edilen Bearer belirteci. |
| Content-Type   | string | Dosya yüklemesi için `multipart/form-data` olmalıdır. |
| Accept         | string | Yanıt meta verilerini almak için `application/json`.  |

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. `Authorization` başlığına bir erişim belirteci ekleyin ve ardından aşağıdaki isteği çalıştırın.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pdf" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <access_token>" \
     -F "datafile=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.pdf",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}


### Aspose.Cells Cloud SDK’larını Kullanma


Bir SDK kullanmak, düşük seviye ayrıntıları ele alarak geliştirme sürecini basitleştirebilir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Bu işlevi uygulayan Diğer API’ler

| **API**        | **Tür** | **Açıklama**                                                     | **Swagger Bağlantısı**                                                                            |
| :------------- | :------ | :--------------------------------------------------------------- | :------------------------------------------------------------------------------------------------ |
| /cells/convert | PUT     | Bir çalışma kitabını istek içeriğinden belirli bir forma dönüştürür. | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |

[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API, bir MS Excel dosyasını ek ayarlarla PDF olarak kaydetmenize ve sonucu depoya kaydetmenize olanak tanır.

Bu REST API, bir Excel dosyasını PDF'ye dönüştürür.

[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API, bir MS Excel dosyasını ek ayarlarla PDF'ye dönüştürmenize ve sonucu yanıtta döndürmenize olanak tanır.

[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) API, bir MS Excel dosyasını ek ayarlarla PDF'ye dönüştürmenize ve sonucu yanıtta döndürmenize olanak tanır.

Bu [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook), [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook) ve [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API’leri, genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Ek dönüşüm seçenekleri için [Kaydetme Seçenekleri](/tr/cells/save-options/) sayfasına bakın.
---