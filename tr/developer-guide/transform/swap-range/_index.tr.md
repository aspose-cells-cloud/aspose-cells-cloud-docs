---
title: "Aspose.Cells Cloud – Sütunları, Satırları ve Aralıkları Değiştirme (v4.0)"
second_title: "Belge"
ArticleTitle: "Excel Dosyalarında Sütunlar, Satırlar ve Hücreler Arasında Veri Değiştirme"
linktitle: "Aralık Değiştir"
type: docs
url: /swap-range/
keywords: "Aspose Cells, Excel API, Aralık Değiştir, Bulut Elektronik Tablo"
description: "Aspose.Cells Cloud API ile Excel dosyalarındaki sütunları, satırları veya aralıkları değiştirin. Tek bir istekte formatları, formülleri ve hücre referanslarını koruyun."
weight: 100
---

Aspose.Cells Cloud API kullanarak Excel dosyalarındaki herhangi iki sütunu, satırı, aralığı veya hücreyi otomatik olarak birbiriyle değiştirin. Aralık Değiştir API'si, tüm formatları, formülleri ve hücre referanslarını koruyarak kesin veri değiştirme işlemi yapmanızı sağlar. Kurumsal iş akışları için karmaşık veri yeniden organizasyonunu, toplu işlemi ve sorunsuz bulut entegrasyonunu destekler.

## **Aralık Değiştir API'si**

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri**

| Parametre Adı      | Tür    | Konum    | Açıklama                                                                                                                                   |
| ------------------ | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Dosya  | FormData | **Zorunludur.** Kaynak Excel çalışma kitapğı dosyası (`.xlsx`, `.xls`).                                                                     |
| **worksheet1**     | Metin  | Sorgu    | **Zorunludur.** İlk veri alanını içeren çalışma sayfasının adı.                                                                             |
| **range1**         | Metin  | Sorgu    | **Zorunludur.** Değiştirilecek `worksheet1` içindeki hücre aralığı (örneğin, `A1:D10`).                                                     |
| **worksheet2**     | Metin  | Sorgu    | **Zorunludur.** İkinci veri alanını içeren çalışma sayfasının adı (`worksheet1` ile aynı olabilir).                                         |
| **range2**         | Metin  | Sorgu    | **Zorunludur.** Değiştirilecek `worksheet2` içindeki hücre aralığı (örneğin, `F1:I10`). **Önemli:** `range1` ve `range2` aynı boyuta sahip olmalıdır. |
| **outPath**        | Metin  | Sorgu    | **İsteğe bağlı.** Değiştirilmiş çalışma kitabının kaydedileceği bulut depolama klasörü.                                                    |
| **outStorageName** | Metin  | Sorgu    | **Zorunludur.** Yapılandırılmış bulut depolama hizmetinin adı (örneğin, `MyCompanyStorage`).                                               |
| **region**         | Metin  | Sorgu    | **İsteğe bağlı.** Biçimlendirmeyi etkileyebilir yerel ayar (örneğin, `tr-TR`, `en-US`, `ja-JP`).                                             |
| **password**       | Metin  | Sorgu    | **İsteğe bağlı.** Korumalı bir elektronik tabloyu açmak için şifre. Şifrelenmemişse bırakılabilir.                                          |

**Örnek İstek (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

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

**Notlar:**  
- API, değiştirilmiş çalışma kitabını bir dosya akışı olarak döndürür. `outPath` belirtilirse, dosya belirtilen bulut depolama konumuna da kaydedilir.  
- Aralık boyutlarının eşleşmemesi **400 Bad Request** hatalarına neden olur.

### Hata Kodları

| Kod                  | Açıklama                                                           |
| -------------------- | ------------------------------------------------------------------ |
| **400 Bad Request**  | Geçersiz istek URI’si veya eşleşmeyen aralık boyutları.             |
| **401 Unauthorized** | Geçersiz veya süresi dolmuş erişim belirteci; istemci kimliği veya gizli anahtar hatalı. |
| **404 Not Found**    | Belirtilen elektronik tablo dosyasına erişilemiyor.                |
| **500 Server Error** | Çalışma kitabı işlenirken iç bir hata oluştu.                       |

## Aralık Değiştir API'si Nerede Kullanılmalı?

- **Finansal Model Yeniden Yapılandırma** – Formülleri ve koşullu biçimlendirmeyi koruyarak veri bloklarını yeniden düzenleyin (örneğin, Q3 tahminini Q4’e taşıyın).
- **Veri Borusu ve ETL Süreçleri** – Nihai çıktıdan önce hazırlama çalışma sayfasında ham veri aralıklarını temizlenmiş aralıklarla değiştirin.
- **Hata Düzeltme ve Veri Kurtarma** – Elle kopyalama-yapıştırma yapmadan hatalı konumlanan verileri hızlıca düzeltin.

## Aralık Değiştir API'si Neden Kullanılmalı?

- **Geliştirici Dostu** – Birden fazla dil için SDK’lar mevcuttur; özel çözümler geliştirmeye göre geliştirme çabasını azaltır.
- **İş Gücü Maliyetlerini Azaltır** – Veri yeniden karıştırma işlemini otomatikleştirerek manuel birleştirme ihtiyacını azaltır.
- **Kullanım Ücretli** – Sadece gerçek olarak yaptığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım** – Yönetilecek sunucu yok, yazılım güncellemesi yok ve uyumluluk sorunu yok.

## Aralık Değiştir API'si SDK’ları ile Nasıl Kullanılır?

### Aralık Değiştir API Spesifikasyonu

[Aralık Değiştir API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange), herkese açık bir programlama arayüzü tanımlar ve doğrudan bir web tarayıcısından REST etkileşimlerinin gerçekleştirilmesini sağlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak kısa kodla aralık değiştirmenizi sağlayan en hızlı geliştirme yöntemidir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerine istek nasıl yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}