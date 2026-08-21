---
title: "Aspose.Cells Cloud Web API – Çalışma Sayfasını HTML’ye Dönüştürme"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud API ile Çalışma Sayfasını HTML’ye Dönüştürme"
linktitle: "Çalışma Sayfasını HTML’ye Dönüştür"
type: docs
url: /tr/convert-worksheet-to-html/
description: "Aspose.Cells Cloud API kullanarak bir Excel çalışma sayfasını HTML’ye nasıl dönüştüreceğinizi öğrenin – yükleme gerektirmez, özel yazı tipleri, bölge desteği ve hata yönetimi."
keywords: "Aspose.Cells, Excel'den HTML’ye, çalışma sayfası dönüştürme, bulut API"
weight: 100
---

**ConvertWorksheetToHtml** uç noktası, bir Excel çalışma kitabını yerel dosya sisteminden okur, belirtilen çalışma sayfasını çıkarır ve içeriği bir HTML dosyası olarak döndürür. Dönüştürme işlemi tamamen Aspose’un bulut sunucularında gerçekleşir; bu nedenle ara yükleme veya depolama gerektirmez. Elektronik tablo verilerinin web için hazır görünümlerini oluşturmak için idealdir. API, isteğe bağlı çıktı yollarını, özel yazı tiplerini, bölge ayarlarını ve şifreli çalışma kitaplarını destekler.

## Çalışma sayfasını HTML’ye dönüştürme API’si

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı   | Tür     | Konum     | Gerekli / İsteğe Bağlı | Açıklama                                                                                                                                                                                                     |
| :-------------- | :------ | :-------- | :-------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Dosya   | Gerekli   | FormData              | İşlenecek ikili Excel dosyası. Geçerli bir .xlsx, .xls, .xlsb vb. olmalıdır. Örnek: `myWorkbook.xlsx`. Excel dosyası doğrudan istek gövdesinden okunur; önceden bulut depolama alanına yüklenmesine gerek yoktur. |
| worksheet       | Dize    | Gerekli   | Sorgu                 | Dönüştürülecek çalışma sayfasının adı (büyük/küçük harf duyarlı). Sağlanan çalışma kitabında mevcut olmalıdır. Örnek: `Sheet1`.                                                                               |
| outPath         | Dize    | İsteğe bağlı | Sorgu                 | Oluşturulan HTML dosyasının kaydedileceği hedef klasör yolu (bulut depolama içinde). Atlanırsa, dosya doğrudan yanıtta döndürülür. Örnek: `/output/html/`.                                                     |
| outStorageName  | Dize    | İsteğe bağlı | Sorgu                 | `outPath` için kullanılacak bulut depolama hizmetinin adı. `outPath` varsayılan olmayan bir depolamayı işaretlediğinde gereklidir.                                                                          |
| fontsLocation   | Dize    | İsteğe bağlı | Sorgu                 | Dönüştürme sırasında kullanılacak özel TrueType/OpenType yazı tiplerini içeren klasörün mutlak yolu. Standart olmayan karakterlerin doğru işlenmesini sağlar.                                                 |
| region          | Dize    | İsteğe bağlı | Sorgu                 | Sayı/tarih formatlamasını etkileyen yerel kimliği (örneğin, `tr-TR`, `fr-FR`). Varsayılan olarak çalışma kitabının iç bölge ayarını kullanır.                                                                |
| password        | Dize    | İsteğe bağlı | Sorgu                 | Korumalı bir çalışma kitabını açmak için gereken parola. Korumasız dosyalar için atlayın.                                                                                                                    |

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

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT belirteci.                                     |
| 413 | Payload Too Large (İçerik Çok Büyük) | Yüklü dosya boyut sınırını aşıyor.                                 |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                          |

## Çalışma sayfasını HTML’ye dönüştürme API’si nerede kullanılmalı?

- Canlı elektronik tablo verilerini bir web portalına gömün – Finansal rapor çalışma sayfasını HTML’ye dönüştürün ve Excel eklentilerine ihtiyaç duymadan doğrudan tarayıcılarda görüntüleyin.
- Excel şablonundan yazdırılabilir HTML fatura oluşturun – Önceden tanımlı bir çalışma sayfasından web için hazır fatura sayfalarının oluşturulmasını otomatikleştirin.
- Belge parçacıkları oluşturun – Tasarım spesifikasyonu sayfalarını HTML parçacıklarına dönüştürün ve bunları teknik kılavuzlara veya wiki’lere ekleyin.
- Düşük kodlu BI dashboard’ları geliştirin – Çalışma sayfası verilerini çekin, bunu HTML’ye dönüştürün ve özel dashboard widget’ları içinde görüntüleyin.

## Neden Çalışma sayfasını HTML’ye dönüştürme API’sini kullanmalısınız?

- **Yükleme gerektirmeyen iş akışı** – Yerel dosyaları doğrudan bulutta dönüştürün; büyük çalışma kitaplarını önce depolama alanına aktarmana gerek kalmadan.
- **Yüksek performanslı işleyiş** – Sunucu tarafı dönüştürme, Aspose’un optimize edilmiş motorundan yararlanır; hızlı ve doğru HTML çıktısı sağlar.
- **Çıktı üzerinde tam denetim** – İsteğe bağlı parametreler (özel yazı tipleri, bölge, parola) HTML’yi yerel ayar ve marka gereksinimlerinize uyacak şekilde özelleştirmenizi sağlar.
- **Kolay entegrasyon** – Multipart/form‑data ile basit PUT isteği, CI/CD pipeline’larına, mikroservislere veya sunucusuz işlevlere doğal olarak uyar.

## Çalışma sayfasını HTML’ye dönüştürme API’sini SDK’larla nasıl kullanabilirsiniz?

### Çalışma sayfasını HTML’ye dönüştürme API’si Başvurusu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtml" target="_blank" rel="noopener noreferrer">Çalışma Sayfasını HTML’ye Dönüştürme API’si Başvurusu</a>, REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için herkese açık bir programlama arayüzü sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.html
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 ile kodlanmış)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak çalışma sayfalarını kısa kodla birleştirmenize izin vererek geliştirmeyi en hızlı yoldur.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud/aspnet-sdk" target="_blank" rel="noopener noreferrer">Aspose.Cells Cloud GitHub deposuna</a> göz atın.  
Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetleriyle nasıl etkileşime girileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}