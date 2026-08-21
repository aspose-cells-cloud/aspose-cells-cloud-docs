---
title: "Aspose.Cells Cloud Excel Ekle Çalışma Sayfası Web API'si - Tür ve Konum Kontrolü ile Yeni Sayfalar Ekleme"
second_title: "Doküman"
ArticleTitle: "Excel'e Çalışma Sayfası Nasıl Eklenir – Yeni Sayfaları Belirli Konumlara Ekleme"
linktitle: "Elektronik Tabloya Çalışma Sayfası Ekle"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "excel, çalışma sayfası ekle, aspose cells api, elektronik tablo, bulut api, sayfa türü, sayfa konumu"
description: "Aspose.Cells Cloud API kullanarak bir Excel çalışma kitabına programlı olarak yeni bir çalışma sayfası, grafik sayfası veya makro sayfası eklemeyi öğrenin. Tek bir REST çağrısıyla sayfa türünü, adını ve ekleme konumunu kontrol edin."
weight: 100
---

Programlı olarak Excel dosyalarına çalışma sayfaları ekleyin ve sayfa türü ile konumu tamamen kontrol edin. Standart çalışma sayfalarını, grafik sayfalarını veya makro sayfalarını çalışma kitabındaki herhangi bir konuma ekleyin. Bu RESTful işlem, otomatik Excel çalışma kitabı yönetimi ve organizasyonunu sağlar.

**Gereksinimler**

- Geçerli bir JWT erişim belirteci ile aktif bir Aspose.Cells Cloud hesabı.
- Çalışma kitabının kaydedileceği yapılandırılmış bir bulut depo adı (örneğin, `CompanyOneDrive`).
- Hedef çalışma kitabının belirtilen depoda erişilebilir olması gerekir; ayrıca korunmuşsa doğru şifre sağlanmalıdır.

| **Çalışma Sayfası Türü** | Açıklama                                           |
| :----------------------- | :------------------------------------------------- |
| **VB**                   | Visual Basic modülü                                |
| **Worksheet**            | Standart çalışma sayfası                           |
| **Chart**                | Grafik sayfası                                     |
| **BIFF4Macro**           | BIFF4 makro sayfası                                |
| **InternationalMacro**   | Uluslararası makro sayfası                         |
| **Other**                | Yukarıda listelenmeyen özel veya daha az yaygın sayfa türü |
| **Dialog**               | İletişim penceresi çalışma sayfası                 |

## **Elektronik Tabloya Çalışma Sayfası Ekleme API'si**

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür      | Konum     | Açıklama                                                                                                                                                                         |
| :----------------- | :------- | :-------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Dosya    | FormData  | **Gerekli.** Yeni bir çalışma sayfasının ekleneceği Excel çalışma kitabı (.xlsx, .xls, vb.).                                                                                      |
| **sheetType**      | Dize     | Sorgu     | **İsteğe bağlı.** Oluşturulacak sayfa türü. Geçerli değerler: `worksheet` (varsayılan), `chartsheet`, `macrosheet`, `vbmodule`, `dialog`.                                         |
| **position**       | Tamsayı  | Sorgu     | **İsteğe bağlı.** Yeni sayfanın ekleneği sıfır tabanlı indeks. `0` ilk sayfadan önce ekler; `2`, üçüncü sayfa olarak ekler. Sayfayı sona eklemek için atlayın.                    |
| **sheetName**      | Dize     | Sorgu     | **İsteğe bağlı.** Yeni çalışma sayfasının adı. Çalışma kitabında benzersiz olmalıdır. Atlanırsa, “SheetX” gibi varsayılan bir ad oluşturulur.                                     |
| **outPath**        | Dize     | Sorgu     | **İsteğe bağlı.** Değiştirilmiş çalışma kitabının kaydedileceği bulut depodaki hedef dizin. `null` veya atlanırsa, çalışma kitabı kaynak dosyanın bulunduğu konuma veya varsayılan bir yola kaydedilir. |
| **outStorageName** | Dize     | Sorgu     | **Gerekli.** Çıktı dosyasının yazılacağı yapılandırılmış bulut depo tanımlayıcısı (örneğin, `CompanyOneDrive`).                                                                   |
| **region**         | Dize     | Sorgu     | **İsteğe bağlı.** Yeni çalışma sayfasında biçimlendirme ve bölgesel kuralları etkileyebilen yerel ayar (örneğin, `tr-TR`).                                                         |
| **password**       | Dize     | Sorgu     | **İsteğe bağlı.** Şifreli bir çalışma kitabını şifresini çözmek ve değiştirmek için şifre. Dosya şifreli değilse atlayın.                                                         |

### Yanıt

Başarılı olursa API **HTTP 200 OK** (veya yeni bir dosya oluşturulursa **201 Created**) döndürür ve güncellenmiş çalışma kitabı dosyasını içerir.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                       |
| --- | --------------------- | -------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz) | Geçersiz veya eksik JWT belirteci.                             |
| 413 | Payload Too Large (İstek Gövdesi Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor.                        |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                     |

## Elektronik Tabloya Çalışma Sayfası Ekleme API'si Nerede Kullanılmalıdır?

- **Otomatik Rapor Oluşturma** – Finansal rapor oluşturma sırasında aylık çalışma sayfalarını (örneğin, `2024‑05`) dinamik olarak oluşturup ekleyin.
- **Toplu Şablon Başlatma** – Satış teklifleri veya önerilerini toplu olarak oluştururken her yeni müşteri veya proje için ayrı bir analiz sayfası ekleyin.
- **Dinamik Gösterge Paneli Genişletme** – Yeni veri boyutları mevcut olduğunda gerçek zamanlı olarak yeni grafik sayfaları ekleyin.
- **Uyumluluk ve Denetim Arşivleme** – Yıllık denetimler sırasında kanıt toplama sayfalarını otomatik olarak ekleyin; her denetim noktasını izole tutun.
- Bir sayfayı silmek için **[Çalışma Sayfasını Sil](/delete-worksheet/)** işlemine bakın.
- Bir sayfayı taşımak için **[Çalışma Sayfasını Taşı](/move-worksheet/)** işlemine bakın.

## Elektronik Tabloya Çalışma Sayfası Ekleme API'si Neden Kullanılmalıdır?

- **Geliştirici Dostu** – Aspose.Cells Cloud, birden fazla dil için SDK’lar sağlar; böylece geliştirme çabasını azaltır ve kapsamlı belgeler sunar.
- **Düşük İşgücü Maliyeti** – Elle çalışma sayfası oluşturma ve tekrarlayan kopyala-yapıştır görevlerine olan ihtiyacı ortadan kaldırır.
- **Kullanım Üzerine Ödeme** – Gerçekten yaptığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım** – Yönetilecek sunucu yok, yazılım güncellemesi yok ve uyumluluk sorunu yok.

## Elektronik Tabloya Çalışma Sayfası Ekleme API'si Nasıl SDK’larla Kullanılır?

### Elektronik Tabloya Çalışma Sayfası Ekleme API'si Spesifikasyonu

[Elektronik Tabloya Çalışma Sayfası Ekleme API'si Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 kodlu)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviyeli ayrıntıları soyutlayarak minimum kodla bir çalışma sayfası eklemenizi sağlar. SDK’ların tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’larla hizmeti çağırma yöntemlerini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}