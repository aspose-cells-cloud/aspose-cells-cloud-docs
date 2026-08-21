---
title: "Excel Çalışma Sayfasında Satırları Gruplama"
second_title: "Belge"
linktitle: "Grupla"
type: docs
url: /rows/group/
aliases: [/group-rows-in-excel-worksheet/]
keywords: "satırları gruplama, Excel, Aspose.Cells Cloud, REST API, SDK, çalışma sayfası, Excel API"
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasında satırları gruplayın. Kolay entegrasyon için birden fazla SDK’yı (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) destekler."
weight: 60
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Sayfasında Satırları Gruplama"
---

Bu REST API, bir Excel çalışma sayfasında satırları gruplar.

**Önkoşullar:**  
- Geçerli bir OAuth 2.0 erişim belirteci (Bearer JWT), `Authorization` başlığına eklenmelidir.  
- İstek gönderilmeden önce çalışma kitabının, seçilen `storageName` (veya varsayılan depo) içinde belirtilen `folder` klasöründe zaten bulunuyor olması gerekir.

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı | Tür      | Konum  | Açıklama                                                                    |
| ------------- | -------- | ------ | --------------------------------------------------------------------------- |
| name          | string   | path   | Çalışma kitabının dosya adı.                                                 |
| sheetName     | string   | path   | Çalışma sayfasının adı.                                                      |
| firstIndex    | integer  | query  | Gruplandırılacak ilk satırın sıfır tabanlı indeksi.                         |
| lastIndex     | integer  | query  | Gruplandırılacak son satırın sıfır tabanlı indeksi.                         |
| hide          | boolean  | query  | Gruplanan satırların gizlenip gizlenmeyeceğini belirtir (`true` veya `false`). |
| folder        | string   | query  | Çalışma kitabını içeren klasörün yolu.                                        |
| storageName   | string   | query  | Çalışma kitabının bulunduğu depo adı.                                         |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows), genel olarak erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod  | Anlamı                    | Açıklama                                               |
|------|---------------------------|--------------------------------------------------------|
| 200  | OK (Tamam)                | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)| Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT belirteci.                     |
| 413  | Payload Too Large (Çok Büyük Yük)| Yüklenecek dosya boyut sınırını aşıyor.            |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                  |

Yaygın hata yanıtları:

- **400 Bad Request (Hatalı İstek)** – `firstIndex` ve `lastIndex` değerlerinin geçerli tam sayılar olduğunu ve `firstIndex` ≤ `lastIndex` koşulunu sağladığını kontrol edin.  
- **401 Unauthorized (Yetkisiz)** – `Authorization` başlığının güncel bir JWT belirteci içerdiğini doğrulayın.  
- **404 Not Found (Bulunamadı)** – Çalışma kitabının (`name`) ve çalışma sayfasının (`sheetName`) belirtilen `folder`/`storageName` içinde mevcut olduğundan emin olun.

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız:** [Excel çalışma sayfasında satırların gruplamasını kaldırma](../rows/ungroup/ "Excel çalışma sayfasında satırların gruplamasını kaldırma"), [Excel çalışma sayfasında satırları gizleme](../rows/hide/ "Excel çalışma sayfasında satırları gizleme"), [Excel çalışma sayfasında satırların gizliliğini kaldırma](../rows/unhide/ "Excel çalışma sayfasında satırların gizliliğini kaldırma").

## Bulut SDK Geliştirme Paketi

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviyeli ayrıntıları yöneterek size proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}