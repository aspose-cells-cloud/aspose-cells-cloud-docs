---
title: "Excel'den JSON'a"
second_title: "Belge"
linktitle: "Excel'den JSON'a"
type: docs
url: /tr/convert-excel-file-to-json-file/
keywords: "Aspose.Cells, Excel'den JSON'a, Bulut API'si, elektronik tablo dönüştürme, REST API"
description: "Aspose.Cells Cloud REST API ile Excel elektronik tablolarını JSON dosyalarına nasıl dönüştüreceğinizi öğrenin. cURL örneği, SDK kod parçacıkları (C#, Java, Python), gerekli parametreler, kimlik doğrulama ve yanıt formatı içerir."
weight: 100
ArticleTitle: "Excel Dosyasını Aspose.Cells Cloud API ile JSON'a Dönüştürme – Hızlı Kılavuz"
---


## REST API

Bu REST API, bir elektronik tablo dosyasını JSON formatlı bir dosyaya dönüştürür.


```http
POST https://api.aspose.cloud/v3.0/cells/convert/json
```

### Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT token tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

### İstek

**Sorgu Parametreleri**

| Parametre Adı         | Tür   | Açıklama                                                           |
| ----------------------- | ------ | --------------------------------------------------------------------- |
| `password`              | string | Excel dosyasını açmak için gereken şifre (isteğe bağlı).                  |
| `storageName`           | string | Dosyanın bulunduğu depo adı (isteğe bağlı).             |
| `checkExcelRestriction` | bool   | Hücreleri düzenlerken Excel’e özel kısıtlamaları zorunlu kılar (isteğe bağlı). |

**İstek Gövdesi Parametresi**

| Parametre Adı | Tür | Açıklama                                                                                       |
| -------------- | ---- | ------------------------------------------------------------------------------------------------- |
| `datafile`     | file | Yüklenecek Excel dosyası. `multipart/form-data` isteğiyle ilk parça olarak gönderilmelidir. |

#### Örnek cURL Çağrısı

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

### Yanıt

Hizmet, bir **FileInfo** nesnesi döndürür. Önemli alanlar aşağıda açıklanmıştır:

| Alan          | Tür    | Açıklama                                                                  |
| ------------- | ------- | ---------------------------------------------------------------------------- |
| `Filename`    | string  | Oluşturulan JSON dosyasının adı (örneğin, `myWorkbook.json`).                   |
| `FileSize`    | integer | Oluşturulan dosyanın bayt cinsinden boyutu.                                         |
| `FileContent` | string  | JSON dosyasının Base64 ile kodlanmış içeriği. Gerçek JSON içeriğini almak için kodunu çözün. |

**Örnek yanıt**

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH ... (base64 string) ..."
}
```

#### Hata Yönetimi

İstek başarısız olursa, API aşağıdaki yapıya sahip bir hata nesnesi döndürür:

| Alan      | Tür   | Açıklama                              |
| --------- | ------ | ---------------------------------------- |
| `Code`    | string | Makine tarafından okunabilir hata tanımlayıcısı.       |
| `Message` | string | Hatanın insan tarafından okunabilir açıklaması. |

Yaygın HTTP durum kodları:

- **400** – Geçersiz istek (örneğin, eksik dosya, geçersiz parametreler).
- **401** – Yetkisiz erişim (geçersiz veya eksik erişim belirteci).
- **500** – İç sunucu hatası.

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam                        | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek               | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz Erişim              | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük                | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası             | Beklenmeyen sunucu hatası. |
## SDK ile PostConvertWorkbookToJson API Nasıl Kullanılır

### PostConvertWorkbookToJson API Tanımı

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToJson" rel="noopener noreferrer" title="Aspose.Cells OpenAPI Tanımı – Çalışma Kitabını JSON'a Dönüştür">OpenAPI Tanımı</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/json" \
     -H "Authorization: Bearer $ACCESS_TOKEN" \
     -H "accept: application/json" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "myWorkbook.json",
  "FileSize": 8423,
  "FileContent": "eyJmb3JtYXR0ZWRfZGF0YSI6IH... (base64 string)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye ayrıntıları yöneterek size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer" title="GitHub'da Aspose.Cells Cloud SDK'ları">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToJson.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToJson.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToJson.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToJson.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToJson.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToJson.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToJson.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToJson.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Benzer işlevselliği uygulayan diğer API’ler

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Excel dosyasını ek ayarlarla HTML dosyası olarak kaydeder ve sonucu belirtilen depoya saklar.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel dosyasını ek ayarlarla HTML dosyasına dönüştürür ve sonucu yanıtta döndürür.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel dosyasını alır; dosyayı HTML formatında almak için sorgu parametreleriyle birlikte kullanılabilir.
---