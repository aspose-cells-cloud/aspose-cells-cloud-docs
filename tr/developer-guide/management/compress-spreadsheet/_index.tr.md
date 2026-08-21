---
title: "Aspose.Cells Cloud Excel Sıkıştırma Web API'si – Elektronik Tablo Boyutunu Programlı Olarak Azaltın"
second_title: "Belge"
ArticleTitle: "Excel Dosyalarını Nasıl Sıkıştırılır – Elektronik Tablo Boyutunu Azaltın ve Performansı Eniyileyin"
linktitle: "Elektronik Tabloyu Sıkıştır"
type: docs
url: /tr/compress-spreadsheet/
keywords: "Excel sıkıştırma, Aspose.Cells Cloud, elektronik tablo boyutu azaltma, API, çalışma kitabını optimize etme"
description: "Aspose.Cells Cloud API ile Excel çalışma kitaplarını nasıl sıkıştıracağınızı öğrenin. Adım adım örnekler, parametreler, kimlik doğrulama ve en iyi uygulamaları edinin."
weight: 100
---

Aspose.Cells Cloud API ile Excel elektronik tablolarını programlı olarak sıkıştırın ve dosya boyutunu azaltın. Kullanılmayan verileri kaldırarak, gömülü nesneleri sıkıştırarak ve formatlamayı temizleyerek çalışma kitabının performansını optimize edin. Bu RESTful API, otomatik Excel dosyası sıkıştırma ve optimize etme iş akışlarını mümkün kılar.

## **Elektronik Tabloyu Sıkıştırma API'si**

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/compress
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### İstek Parametreleri

| Parametre Adı  | Tür      | Yol/Sorgu/Dizgi/HTTP Gövdesi | Açıklama                                                                                                                             |
| ---------------- | -------- | ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet      | Dosya    | FormData                     | **Zorunlu.** Sıkıştırılacak kaynak Excel çalışma kitap dosyası (`.xlsx`, `.xls`, vb.).                                              |
| level            | Tamsayı  | Sorgu                        | **İsteğe bağlı.** Sıkıştırma yoğunluğu (0 = en hızlı/düşük, 9 = en yavaş/yüksek). Atlanırsa, dengeli varsayılan (5) uygulanır.         |
| outPath          | Dizgi    | Sorgu                        | **İsteğe bağlı.** Bulut depolama alanındaki hedef klasör yolu. Atlanırsa, dosya kaynak çalışma kitabının bulunduğu klasöre kaydedilir. |
| outStorageName   | Dizgi    | Sorgu                        | **Zorunlu.** Yapılandırılmış bulut depolama hizmetinin tanımlayıcısı (örneğin, `CorporateDrive`).                                    |
| region           | Dizgi    | Sorgu                        | **İsteğe bağlı.** Bölgeye özel veri işleme üzerinde etkisi olabilecek yerel ayar (örneğin, `de-DE`).                                  |
| password         | Dizgi    | Sorgu                        | **İsteğe bağlı.** Korumalı bir elektronik tabloyu çözmek için şifre. Dosya şifrelenmemişse boş bırakın.                                |

### Yanıt

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                           |
| --- | --------------------- | ------------------------------------------------------------------ |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.     |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                 |
| 413 | Yük Çok Büyük         | Yüklenecek dosya boyut limitini aşıyor.                            |
| 500 | Sunucu İçi Hata       | Beklenmeyen sunucu hatası.                                         |

## Elektronik Tabloyu Sıkıştırma API’si Nerede Kullanılmalıdır?

- **Otomatik rapor dağıtımı** – E-posta ile gönderilmeden önce aylık mali raporları sıkıştırarak başarıyla teslimatı sağlayın ve alıcının deneyimini iyileştirin.
- **Kullanıcı dosya yükleme optimizasyonu** – Bulut depolama alanını tasarruf ettirmek ve depolama maliyetlerini azaltmak için arka planda yüklenen Excel dosyalarını sıkıştırın.
- **Veri hattı işleme ve taşıma** – ETL süreçleri sırasında oluşturulan ara Excel dosyalarını sıkıştırarak ağ aktarımını hızlandırın ve geçici depolama baskısını azaltın.

## Elektronik Tabloyu Sıkıştırma API’sini Neden Kullanmalısınız?

- **Geliştirici dostu** – Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve kapsamlı belgelerle hızlı geliştirme imkânı verir.
- **Düşük iş gücü maliyeti** – Belgeleri manuel olarak birleştirmek için özel personel gerekmez.
- **Kullanım başına ödeme fiyatlandırma** – Ön ödeme gerektirmez; yalnızca gerçekleştirdiğiniz API çağrıları için ödeme yaparsınız.
- **Sunucu bakımı gerekmez** – Bakımlı sunucu yoktur, yazılım güncellemesi yoktur ve uyumluluk sorunu yoktur.

## SDK’larla Elektronik Tabloyu Sıkıştırma API’sini Nasıl Kullanılır?

### Elektronik Tabloyu Sıkıştırma API’si Spesifikasyonu

[Elektronik Tabloyu Sıkıştırma API Spesifikasyonu](https://reference.aspose.cloud/cells/#/ManagementController/CompressSpreadsheet), REST etkileşimleri için herkese açık bir arayüz sağlar ve doğrudan bir web tarayıcısından API çağrıları yapılmasını mümkün kılar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/compress?level=5&outStorageName=MyStorage" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/input.xlsx"
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak bir elektronik tabloyu yalnızca birkaç satır kodla sıkıştırmanızı sağlayan en hızlı gelişim yoludur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetleriyle nasıl etkileşime girileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CompressSpreadsheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CompressSpreadsheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CompressSpreadsheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CompressSpreadsheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CompressSpreadsheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CompressSpreadsheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CompressSpreadsheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CompressSpreadsheet.go" >}}
{{</tab>}}
{{< /tabs >}}