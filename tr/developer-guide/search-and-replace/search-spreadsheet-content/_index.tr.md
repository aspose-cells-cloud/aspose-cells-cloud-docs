---
title: "Excel Çalışma Kitapları İçeriğini Arama – Aspose.Cells Cloud API (Excel'de Metin Bul)"
second_title: "Belge"
ArticleTitle: "Yerel Excel Çalışma Kitaplarında Metin Arama – Belirli Verileri Bul"
linktype: "docs"
url: "/search-spreadsheet-content/"
keywords: "Aspose.Cells, Excel arama API'si, çalışma sayfası içeriği arama, bulut çalışma sayfası API'si, metin arama"
description: "Aspose.Cells Cloud API ile yerel Excel dosyalarında metin, sayı veya formül arayın. Büyük/küçük harf duyarsız sorguları, çalışma sayfası düzeyinde kapsamı ve güvenli kimlik doğrulamayı destekler."
weight: 100
---

## **Excel Çalışma Kitabı İçeriğini Arama API'si**

Aspose.Cells Cloud API ile programlı olarak herhangi bir Excel çalışma sayfasında belirli metni arayın. API, bulutta depolanan yerel dosyalarda metin, sayı veya formülleri bulabilir; otomatik veri keşfi, içerik analizi ve çalışma sayfası denetim süreçlerini mümkün kılar.


### **Web API'si**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

Daha düşük seviyeli HTTP kullanmayı tercih ediyorsanız, aşağıdaki cURL örneği aynı isteği gösterir:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Fatura&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri**

| Parametre     | Tür     | Konum     | Açıklama                                                                                  |
| ------------- | ------- | --------- | ----------------------------------------------------------------------------------------- |
| spreadsheet   | Dosya   | FormData  | Aranacak Excel dosyası.                                                                   |
| searchText    | Metin   | Sorgu     | Çalışma kitabında bulunacak metin (veya sayısal değer).                                  |
| ignoringCase  | Boolean | Sorgu     | Büyük/küçük harf duyarsız arama yapmak için `true` olarak ayarlayın.                     |
| worksheet     | Metin   | Sorgu     | Aramayı sınırlamak için çalışma sayfasının adı. Atlanırsa tüm çalışma sayfaları taranır. |
| cellArea      | Metin   | Sorgu     | Arama alanını sınırlayan A-1 stili aralık (örneğin, `A1:C10`).                            |
| region        | Metin   | Sorgu     | Hizmetin coğrafi bölgesi (örneğin, `us-east-1`).                                         |
| password      | Metin   | Sorgu     | Korumalı bir çalışma kitabını açmak için gerekli parola.                                  |


### **Yanıt**

API, eşleşen hücrelerin bir dizisini içeren bir `SearchResult` nesnesi döndürür. Her öğe, çalışma sayfası adını, hücre adresini ve eşleşen metni sağlar.

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Toplam",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Toplam",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

### Hata Kodları

- **400 Bad Request (Kötü İstek)** – İstek URI’si veya parametreleri geçersizdir.
- **401 Unauthorized (Yetkisiz)** – Eksik veya geçersiz erişim belirteci veya yanlış istemci kimlik bilgileri.
- **404 Not Found (Bulunamadı)** – Belirtilen çalışma sayfasına erişilemiyor.
- **500 Internal Server Error (İç Sunucu Hatası)** – Çalışma kitabını işlerken beklenmeyen bir sunucu hatası oluştu.

## Excel Çalışma Kitabı İçeriğini Arama API'si nerede kullanılmalı?

- **Kapsamlı Çalışma Kitabı Uyumluluk Denetimi** – Veri güvenliği ve uyumluluk kontrolleri için “Gizli Madde”, “İç Veri” gibi hassas terimleri içeren tüm çalışma kitabını tarayın.
- **Çapraz Sayfa Veri Bağlantı Sorgusu** – Birden fazla çalışma sayfasında görünen proje numarası veya müşteri adını bulun; böylece hızlı çapraz sayfa entegrasyonu sağlayın.
- **Toplu Şablon İçeriği Doğrulama** – Raporlar oluşturulduktan sonra `{{Tarih}}` gibi yer tutucuların bir Excel dosyası grubunda doğru şekilde değiştirildiğini doğrulayın.
- **Tarihsel Veri Arşivleme ve Madenciliği** – Veri arkeolojisi ve analizini hızlandırmak için eski Excel dosyalarında belirli olay kodlarını veya iş terimlerini arayın.

## Neden Excel Çalışma Kitabı İçeriğini Arama API'sini kullanmalısınız?

- **Geliştirici Dostu** – Birçok dil için SDK’lar mevcuttur; özel bir çözüm oluşturmak yerine geliştirme çabasını azaltır.
- **Düşük İşgücü Maliyeti** – Elle çalışma sayfası incelemesi gerektiren görevleri otomatikleştirir.
- **Kullanım Ücretli** – Gerçekten yaptığınız API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım** – Yönetilecek sunucu yoktur; yazılım güncellemesi veya uyumluluk sorunları da yoktur.
- **Karmaşık Biçimlendirmeyi Korur** – Sonuçlar, orijinal Excel düzeni korunarak PDF’e aktarılabilir.

## SDK’lar ile Excel Çalışma Kitabı İçeriğini Arama API'sini Nasıl Kullanılır

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, arama işlevselliğini entegre etmenin en hızlı yoludur. SDK, HTTP katmanını soyutlayarak API’yi minimum kodla çağırmanızı sağlar. SDK’ların tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’larla Excel Çalışma Kitabı İçeriğini Arama işlemini nasıl çağıracağınızı gösterir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}
---