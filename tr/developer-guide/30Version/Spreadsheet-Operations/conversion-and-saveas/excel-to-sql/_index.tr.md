---
title: "Excel'den SQL'e"
second_title: "Belge"
linktitle: "Excel'den SQL'e"
type: docs
url: /tr/convert-excel-file-to-sql-file/
keywords: "Aspose.Cells, Excel'den SQL'e, bulut API'si, elektronik tablo dönüştürme, REST"
description: "Aspose.Cells Cloud REST API'sini kullanarak Excel elektronik tablo dosyalarını SQL dosyalarına dönüştürün. Uygulamalarınıza sorunsuz entegrasyon için birden fazla SDK ve programlama dilini destekler."
weight: 100
ArticleTitle: "Excel Dosyasını SQL'e Dönüştür – Aspose.Cells Cloud API'si"
---

Bu REST API'si, bir elektronik tablo dosyasını SQL formatlı bir dosyaya dönüştürür.

**Ön Gereksinimler**  
Bu uç noktayı kullanmak için, <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteç tabanlı kimlik doğrulama</a> kılavuzunda açıklandığı şekilde geçerli bir JWT belirteci oluşturmanız gerekir. API, hizmet dokümantasyonunda tanımlanan boyut sınırları dahilinde Excel dosyalarını işler ve `password` sorgu parametresi sağlandığında şifreli çalışma kitaplarını da işleyebilir.

## PostConvertWorkbookToSQL API'si

```http
POST https://api.aspose.cloud/v3.0/cells/convert/sql
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteç tabanlı kimlik doğrulama</a> gerektirir.

### **Sorgu Parametresi**

| Parametre Adı         | Tür    | Açıklama                                                                                 |
| --------------------- | ------ | ----------------------------------------------------------------------------------------- |
| password              | string | Excel dosyasını açmak için gerekli şifre.                                                  |
| storageName           | string | Dosyanın depolandığı deponun adı.                                                          |
| checkExcelRestriction | bool   | Hücreyle ilgili nesneleri değiştirirken Excel dosyası kısıtlamalarının denetlenip denetlenmeyeceğini belirtir. |

### **İstek Gövdesi Parametresi**

| Parametre Adı | Tür        | Açıklama                                                                  |
| ------------- | ---------- | ------------------------------------------------------------------------- |
| datafile      | data file  | Dönüştürülecek elektronik tablo dosyası; isteğin ilk bölümü olarak eklenir. |

### Yanıt

API, oluşturulmuş SQL dosyasını içeren bir **FileInfo** nesnesi döndürür.

| Alan            | Tür    | Açıklama                                      |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | SQL dosyasının adı (örneğin, `example.sql`). |
| **FileSize**    | int    | Dosyanın bayt cinsinden boyutu.               |
| **FileContent** | string | SQL dosyasının Base64 ile kodlanmış içeriği.  |

[FileInfo](/cells/file-info/)

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                               |
|-----|-----------------------------|--------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz İstek              | Geçersiz veya eksik JWT belirteci.                      |
| 413 | İstek Gövdesi Çok Büyük     | Yüklenen dosya boyut sınırını aşıyor.                   |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                             |

## SDK’larla PostConvertWorkbookToSQL API’sini Nasıl Kullanılır

### PostConvertWorkbookToSQL API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istekte bulunmayı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.sql",
  "FileSize": 1024,
  "FileContent": "base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub depomuzu</a> inceleyin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracığınızı göstermektedir:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Bu İşlevi Uygulayan Diğer API’ler

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Bir çalışma kitabını farklı bir formatta kaydeder ve sonucu belirtilen depoda saklar.

- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Bir çalışma kitabını isteğe bağlı ayarlarla birlikte başka bir formata dönüştürür ve sonucu yanıtta döndürür.

- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – İsteğe bağlı dönüştürme ayarlarıyla birlikte bir çalışma kitabını alır.

**Notlar**  
- Şifreli Excel dosyalarını dönüştürürken `password` sorgu parametresinin sağlandığından emin olun; aksi takdirde dönüştürme işlemi 400 hatasıyla başarısız olur.  
- Hizmet SQL dosyası içeriğini Base64 olarak döndürür; `.sql` dosyasına kaydetmeden önce bunu kod çözmeniz gerekir.  

**Örnek Dosyalar**  
API'yi hızlıca test etmek için örnek bir Excel çalışma kitabını [buradan](https://example.com/sample.xlsx) ve önceden oluşturulmuş bir SQL sonucunu [buradan](https://example.com/sample.sql) indirin.