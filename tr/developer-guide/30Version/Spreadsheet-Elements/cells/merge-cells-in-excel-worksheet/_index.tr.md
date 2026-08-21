---
title: "Excel Çalışma Sayfasında Hücreleri Nasıl Birleştirilir – Aspose.Cells Cloud API (v3.0)"
type: docs
url: /tr/merge-cells-in-excel-worksheet/
weight: 110
keywords: "hücre birleştirme, Aspose.Cells, Cloud API, Excel"
description: "Aspose.Cells Cloud REST API ile Excel çalışma sayfasında hücreleri birleştirmek için kılavuz; cURL ve SDK örnekleri ile."
ArticleTitle: "Excel Çalışma Sayfasında Hücreleri Nasıl Birleştirilir – Aspose.Cells Cloud API (v3.0)"
---

Aspose.Cells Cloud REST API, belirtilen satır ve sütunları kapsayan tek bir hücrede dikdörtgen bir hücre bloğunu birleştirir.

**Ön Gereksinimler**  
- Kimlik doğrulama için geçerli bir JWT jetonu.  
- Çalışma kitabının zaten belirtilen depo klasöründe bulunuyor olması.  
- Aspose.Cloud hesabınızda depo yapılandırmasının (klasör ve depo adı) yapılması gerekir.

## PostWorksheetMerge API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/merge
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Ad              | Tür      | Konum   | Açıklama                                              |
|-----------------|----------|---------|-------------------------------------------------------|
| name            | string   | path    | Çalışma kitabının adı.                                |
| sheetName       | string   | path    | Çalışma sayfasının adı.                               |
| startRow        | integer  | query   | İlk satırın sıfır tabanlı indeksi (0 = ilk satır).   |
| startColumn     | integer  | query   | İlk sütunun sıfır tabanlı indeksi (0 = ilk sütun).    |
| totalRows       | integer  | query   | Birleştirilecek satır sayısı.                         |
| totalColumns    | integer  | query   | Birleştirilecek sütun sayısı.                         |
| folder          | string   | query   | Çalışma kitabının bulunduğu klasör.                   |
| storageName     | string   | query   | Depo adı.                                             |

*Bu işlem için bir istek gövdesi gerekli değildir.*

## **Yanıt**

CellsCloudResponse döner.

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                |
|-----|-----------------------------|---------------------------------------------------------|
| 200 | OK (Tamam)                  | Süzgeç başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT jetonu.                         |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.              |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                         |

## SDK’larla PostWorksheetMerge API Nasıl Kullanılır

### PostWorksheetMerge API Specification (API Tanımı)

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetMerge), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL komut satırı** aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl atılır gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/merge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
  -X POST \
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

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları kendisi yönetir; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istek atılacağını gösterir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}