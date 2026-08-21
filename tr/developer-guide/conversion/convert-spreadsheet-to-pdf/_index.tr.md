---
title: "Aspose.Cells Cloud Web API – Elektronik Tabloyu PDF'ye Dönüştürme"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud API Kullanılarak Yerel Bir Elektronik Tablonun PDF'ye Dönüştürülme Yöntemi"
linktitle: "Elektronik Tabloyu PDF'ye Dönüştür"
type: docs
url: /tr/convert-spreadsheet-to-pdf/
keywords: "Aspose.Cells Cloud, elektronik tablo PDF'ye, Excel dönüştürme, bulut API, PDF oluşturma, REST API, v4.0"
description: "Aspose.Cells Cloud API kullanılarak yerel bir elektronik tablonun PDF'ye dönüştürülmesi için adım adım kılavuz. İstek sözdizimi, parametreler, yanıt detayları, hata yönetimi ve pratik kullanım örneklerini içerir."
weight: 100
---

**ConvertSpreadsheetToPdf** uç noktası, yerel bir sürücüden yüklenen bir elektronik tablo dosyasını okur, Aspose.Cells Cloud sunucusunda işler ve oluşturulan PDF belgesini ikili akış olarak döndürür. Bu bulut tabanlı dönüştürme işlemi, kaynak dosyanın depoya yüklenmesini gerektirmez, kaynak tüketimini azaltır ve PDF’yi doğrudan istemciye ileterek iş akışlarını basitleştirir. Desteklenen formatlar temel kütüphanelere bağlıdır; API, dosya varlığını, izinlerini ve dönüştürme bütünlüğünü doğrular ve geçersiz girdi veya işlem hataları durumunda uygun HTTP hatalarını verir.

## **Elektronik Tabloyu PDF'ye Dönüştür API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür    | Konum     | Gerekli / Opsiyonel | Açıklama                                                                                                                                                                                         |
| :------------- | :----- | :-------- | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya  | FormData  | Gerekli           | Dönüştürülecek kaynak elektronik tablo dosyası (XLS, XLSX, CSV vb.). Geçerli ve okunabilir bir dosya olmalıdır; maksimum boyut 100 MB’dir. Örnek: `myWorkbook.xlsx`.                               |
| outPath        | Dize   | Sorgu     | Opsiyonel         | Dönüştürülmüş PDF’in sunucuda depolanacağı hedef klasör yolu (eğer kaydetmek isterseniz). Atlanırsa, dosya doğrudan yanıtta döndürülür. Örnek: `/output/reports/`.                                    |
| outStorageName | Dize   | Sorgu     | Opsiyonel         | Hedef depolama hizmetinin adı (örneğin `MyCloudStorage`). `outPath` kullanıldığında ve depolama varsayılan değilse gereklidir.                                                                      |
| fontsLocation  | Dize   | Sorgu     | Opsiyonel         | PDF’de doğru metin gösterimi için sunucuda özel yazı tipi klasörünün yolu. Örnek: `/fonts/custom/`.                                                                                               |
| region         | Dize   | Sorgu     | Opsiyonel         | Elektronik tablo bölgesi/dil ayarı (örneğin `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler.                                            |
| password       | Dize   | Sorgu     | Opsiyonel         | Korumalı bir elektronik tabloyu açmak için gerekli şifre. Dosya şifrelenmemişse atlanır.                                                                                                         |

### **Yanıt**

Başarılı yanıt (200 OK)  
Content-Type: application/pdf  
Content‑Disposition: attachment; filename="converted.pdf"  
Content‑Length: `<bayt cinsinden boyut>`

Gövde: Oluşturulan PDF dosyasının ikili akışı

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                         |
| --- | --------------------- | ---------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.      |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                               |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                       |

## Elektronik Tabloyu PDF'ye Dönüştür API nerede kullanılmalıdır?

- **Otomatik raporlama iş akışları** – Günlük olarak oluşturulan Excel raporlarını, manuel adımlar olmadan arşivleme veya e-posta ile dağıtım için PDF’e dönüştürün.
- **Belge yönetim sistemleri** – Dönüştürme sonrası PDF’leri doğrudan DMS’ye kaydedin; orijinal elektronik tabloyu yalnızca istemci tarafında tutun.
- **Anlık dışa aktarma sağlayan web uygulamaları** – Kullanıcıların tarayıcıda düzenledikleri elektronik tablonun PDF sürümünü, bulut tabanlı dönüştürme ile düzen korunarak indirebilmelerini sağlayın.
- **Düzenleyici uyumluluk** – Denetim izleri için finansal elektronik tabloların değiştirilemez PDF anlık görüntülerini oluşturun; kaynak dosyanın asla istemci ortamından çıkmamasını sağlayın.
- **Çoklu format dönüştürme iş akışları** – [Elektronik Tabloyu CSV’ye Dönüştür](/tr/convert-spreadsheet-to-csv/) API’si gibi diğer dönüştürme uç noktalariyle birleştirerek çoklu formatlı arşivler oluşturun.

## Elektronik Tabloyu PDF'ye Dönüştür API’yi neden kullanmalısınız?

- **Sıfır yükleme iş akışı** – Kaynak dosyanın bulut depolama alanına yüklenmesine gerek yoktur; dönüştürme doğrudan yüklenen akıştan yapılır, bant genişliği ve depolama maliyetlerini tasarruf sağlar.
- **Yüksek kaliteli oluşturma** – Aspose.Cells, dönüştürme sırasında karmaşık formülleri, grafikleri ve formatlamayı korur; masaüstü Excel çıktısını eşleştirir.
- **Ölçeklenebilir bulut işlemi** – İstemci donanımından bağımsız olarak hızlı ve güvenilir dönüştürme için Aspose’un bulut altyapısını kullanır.
- **Basit REST arayüzü** – İsteğe bağlı sorgu parametreleriyle tek bir `PUT` isteği; indirmeye hazır PDF akışı döndürür, bu da entegrasyonu herhangi bir dilde kolaylaştırır.

## Elektronik Tabloyu PDF'ye Dönüştür API’yi SDK’lar ile Nasıl Kullanılır?

### Elektronik Tabloyu PDF'ye Dönüştür API Spesifikasyonu

[Elektronik Tabloyu PDF'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/ConversionController/ConvertSpreadsheetToPdf), web tarayıcısından doğrudan REST etkileşimlerini gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/pdf" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

SDK kullanmak, düşük seviye detayları soyutlayarak, elektronik tabloyu başka bir elektronik tabloyla birleştirmek gibi işlemleri kısa kodla hızlıca geliştirmenin en hızlı yoludur. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın. Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetleriyle nasıl etkileşime geçileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToPdf.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToPdf.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToPdf.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToPdf.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToPdf.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToPdf.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToPdf.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToPdf.go" >}}
{{</tab>}}
{{< /tabs >}}