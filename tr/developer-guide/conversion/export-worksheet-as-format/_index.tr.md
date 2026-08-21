---
title: "Çalışma Sayfasını Dışa Aktar – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Belge"
ArticleTitle: "Uzak Bir Elektronik Tablo Çalışma Sayfasını Başka Bir Formata Dışa Aktarma: Adım Adım Kılavuz"
linktitle: "Çalışma Sayfasını Dışa Aktar"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, çalışma sayfası dışa aktar, bulut API, PDF, PNG, CSV, Excel dönüştürme"
description: "Aspose.Cells Bulut'ta depolanan bir çalışma sayfasını tek bir GET isteğiyle PDF, PNG, SVG, CSV veya diğer formatlara dönüştürün. C#, Java, Python ve daha fazlası için kod örneklerini içerir."
weight: 100
---

Aspose.Cells Cloud Web API’sini kullanarak bir bulut elektronik tablosunu/Excel çalışma sayfasını başka bir format dosyasına dışa aktarın.

## **Çalışma Sayfasını Formata Dışa Aktar API’si**

### Web API’si

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri**

| Parametre Adı      | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                          |
| :----------------- | :------ | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| **name**           | Dize    | Yol                         | (Gerekli) Getirilecek çalışma kitabının dosya adı.                                                                                               |
| **worksheet**      | Dize    | Yol                         | (Gerekli) Dönüştürülecek belirli çalışma sayfası.                                                                                                |
| **format**         | Dize    | Sorgu                       | (Gerekli) İstenen çıktı formatı (örn. `png`, `pdf`, `svg`).                                                                                      |
| **folder**         | Dize    | Sorgu                       | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer `null`’dır.                                                            |
| **storageName**    | Dize    | Sorgu                       | (İsteğe bağlı) Özel bulut depolama adı. Atlanırsa varsayılan depolama kullanılır.                                                                 |
| **outPath**        | Dize    | Sorgu                       | (İsteğe bağlı) Çıktı klasör yolu. Varsayılan değer `null`’dır.                                                                                    |
| **outStorageName** | Dize    | Sorgu                       | (İsteğe bağlı) Çıktı dosyasının depolandığı depolama adı.                                                                                         |
| **fontsLocation**  | Dize    | Sorgu                       | (İsteğe bağlı) Gerekirse özel yazı tiplerini belirtin.                                                                                            |
| **region**         | Dize    | Sorgu                       | (İsteğe bağlı) Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). SayıBiçimlendirme, tarih ayrıştırma ve yerel ayar özelindeki davranışları etkiler. |
| **password**       | Dize    | Sorgu                       | (İsteğe bağlı) Elektronik tablo dosyasına erişmek için gerekli şifre.                                                                             |

### **Yanıt**

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

| Kod | Anlamı               | Açıklama                                                        |
| ---- | -------------------- | --------------------------------------------------------------- |
| 200  | Tamam                | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.  |
| 400  | Geçersiz İstek       | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Yetkisiz             | Geçersiz veya eksik JWT belirteci.                              |
| 413  | Yük Çok Büyük        | Yüklenecek dosya boyut sınırını aşıyor.                         |
| 500  | İç Sunucu Hatası     | Beklenmeyen sunucu hatası.                                      |

## **Çalışma Sayfasını Başka Bir Formata Dışa Aktar API’si Nerede Kullanılmalıdır?**

- **Eski Sistemlerden Geçiş** – Binlerce eski XLS dosyasını modern sistemler için XLSX’e dönüştürün.
- **Arşiv Standartlaştırma** – Çeşitli elektronik tablo formatlarını (XLS, XLSM, ODS, CSV) arşivleme için tek bir formata dönüştürün.
- **Ofis Uygulamaları Arası Uyumluluk** – LibreOffice, Google Sheets veya Apple Numbers ile uyumlu formatlara Excel dosyaları dönüştürün.
- **Veri Kaynağı Standardizasyonu** – Veritabanına aktarım için çeşitli elektronik tablo formatlarını CSV veya JSON’a dönüştürün.
- **Web Yayıncılığı** – Finansal modelleri web gösterimi için HTML’e dönüştürün.

## **Çalışma Sayfasını Başka Bir Formata Dışa Aktar API’si Neden Kullanılmalı?**

- **Çoklu dil SDK desteği** – Birden fazla programlama dili için istemci kitaplıkları sunar; geliştiricilerin tercih ettikleri ortamdan doğrudan API’yi çağırmalarını sağlar.
- **Ortaya çıkan dosyayı tekrar yüklemeye gerek kalmadan doğrudan dönüştürme** – Bulut depolamada depolanan bir çalışma sayfasını, dosyayı indirip yeniden yüklemeye gerek kalmadan istenen forma dönüştürür.
- **Sadece veri çıkarma** – Görsel stillendirmeyi korumadan seçilen formatta çalışma sayfası içeriğini döndürür.

## **Çalışma Sayfasını Format Olarak Dışa Aktar API’si Nasıl SDK’larla Kullanılır?**

### Çalışma Sayfasını Format Olarak Dışa Aktar API’si Spesifikasyonu

[Çalışma Sayfasını Format Olarak Dışa Aktar API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat), doğrudan bir web tarayıcısından REST etkileşimleri gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tablo çalışma sayfasını format dosyasına dönüştürmeyi kısa kodla yapmanızı sağlayan en hızlı gelişim yöntemidir.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}