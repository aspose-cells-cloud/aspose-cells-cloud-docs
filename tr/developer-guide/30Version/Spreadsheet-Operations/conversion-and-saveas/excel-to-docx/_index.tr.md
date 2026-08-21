---
title: "Excel'den Docx'e"
second_title: "Belge"
linktitle: "Excel'den Docx'e"
type: docs
url: /tr/trconvert-excel-file-to-docx-file/
keywords: "Excel'den Docx'e dönüştürme, Aspose.Cells Cloud, REST API, elektronik tablo dönüştürme, belge oluşturma"
description: "Aspose.Cells Cloud REST API ile Excel elektronik tablolarını DOCX belgelerine dönüştürün. Kolay entegrasyon için birden fazla SDK ve programlama dilini destekler."
weight: 90
---

Bu REST API, bir elektronik tablo dosyasını DOCX formatındaki bir dosyaya dönüştürür.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/docx
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.



**Sorgu Parametreleri**

| Parametre Adı         | Tür   | Açıklama                                                                                              |
| --------------------- | ----- | ----------------------------------------------------------------------------------------------------- |
| password              | string | Excel dosyasını açmak için gereken şifre.                                                             |
| storageName           | string | Dosyanın bulunduğu depo adı.                                                                          |
| checkExcelRestriction | bool   | Kullanıcı hücreyle ilgili nesneleri düzenlediğinde Excel dosyası kısıtlamalarının denetlenip denetlenmeyeceğini belirtir. |

**İstek Gövdesi Parametresi**

| Parametre Adı | Tür        | Açıklama                                                       |
| ------------- | ---------- | -------------------------------------------------------------- |
| datafile      | veri dosyası | Çok parçalı istek gövdesinin ilk kısmında kaydedilen veri dosyası. |

**Yanıt**

API, oluşturulan Word dosyasını içeren bir **FileInfo** nesnesi döndürür.

| Alan            | Tür   | Açıklama                                       |
| --------------- | ----- | ---------------------------------------------- |
| **Filename**    | string | Word dosyasının adı (örn., `örnek.docx`).      |
| **FileSize**    | int   | Dosyanın bayt cinsinden boyutu.                |
| **FileContent** | string | Word dosyasının Base64 ile kodlanmış içeriği.  |


[FileInfo](/cells/file-info/)

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                     |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşıyor.                |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                            |
## SDK’lar ile PostConvertWorkbookToDocx API Nasıl Kullanılır

### PostConvertWorkbookToDocx API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToDocx), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istekte bulunulacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/docx" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "örnek.docx",
  "FileSize": 12345,
  "FileContent": "Dosya İçeriği: base64_kodlu_dize"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToDocx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToDocx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToDocx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToDocx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToDocx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToDocx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToDocx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToDocx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Bu İşlevi Uygulayan Diğer API’ler

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Excel dosyasını ek ayarlarla DOCX dosyası olarak kaydeder ve sonucu belirtilen depoda tutar.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Excel dosyasını isteğe bağlı ayarlarla DOCX dosyasına dönüştürür ve sonucu yanıtta döndürür.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Excel çalışma kitabını alır ve isteğe bağlı parametrelerle DOCX dosyasına dönüştürür.