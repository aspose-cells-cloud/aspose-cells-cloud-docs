---
title: "Aspose.Cells Cloud Web API – Elektronik Tabloyu Hedef dile Çevir"
second title: "Belge"
ArticleTitle: "Aspose.Cells Cloud AI Çeviri API’si ile Tam Bir Elektronik Tabloyu Nasıl Çevirebilirsiniz"
linktitle: "Elektronik Tabloyu Çevir"
type: docs
url: /translate-spreadsheet/
keywords: "Aspose.Cells Cloud, Elektronik Tabloyu Çevir API’si, AI çevirisi, elektronik tablo çevirisi, targetLanguage, çok sayfalı çevirme, bulut elektronik tablo işleme, Aspose.Cells Cloud çevirisi"
description: "Aspose.Cells Cloud AI ile tüm bir Excel defterini çevirin. Formülleri, grafikleri ve formatlamayı korurken metni desteklenen herhangi bir dile dönüştürün. Uç nokta, parametreler, SDK örnekleri, sınırlar ve hata işleme hakkında bilgi edinin."
weight: 100
---

**TranslateSpreadsheet** uç noktası, **Translate Spreadsheet API**’sinin bir parçası olarak, bir defterdeki her metin öğesini okur, içeriği AI destekli bir çeviri hizmetine gönderir ve tüm metinsel verilerin belirtilen **targetLanguage** dilinde sunulduğu yeni bir elektronik tablo dosyası döndürür. İşlem, orijinal düzeni, hücre stillerini, formülleri ve **çok sayfalı** yapıyı aynen korur; bu da raporları, kontrol panellerini ve veri odaklı belgeleri küreselleştirme amacıyla ideal hale getirir. Desteklenen dosya formatları şunlardır: XLS, XLSX, XLSM, CSV ve ODS. Geçersiz dil kodları, kimlik doğrulama hataları veya çeviri hizmeti kesintileri durumunda hatalar döndürülür.

## **Translate Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **İstek Parametreleri:**

| Parametre Adı   | Tür     | Konum     | Gerekli / Opsiyonel | Açıklama                                                                                                                                                                                                 |
| :-------------- | :------ | :-------- | :------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Dosya   | Gerekli   | FormData            | Çevrilecek Excel defteri. Kabul edilen uzantılar: .xls, .xlsx, .xlsm, .csv, .ods. Maksimum dosya boyutu: 50 MB. Örnek: `budget.xlsx`.                                                                   |
| targetLanguage  | string  | Gerekli   | Sorgu               | İstenen çıktı dili için ISO 639-1 dil kodu (örn., İspanyolca için "es", Fransızca için "fr", Almanca için "de"). Temel altyapıdaki AI hizmetinin desteklediği bir dil olmalıdır.                           |
| region          | string  | Opsiyonel | Sorgu               | Tarih, sayı ve para birimi gibi yerel ayarla ilişkili formatlamayı etkileyen elektronik tablo bölgesi tanımlayıcısı. Yaygın değerler: "US", "EU", "CN". Atlanırsa, defterin orijinal bölge ayarı kullanılır. |
| password        | string  | Opsiyonel | Sorgu               | Korumalı bir defteri açmak için şifre. Dosya şifre korumalı değilse boş bırakın.                                                                                                                         |

### **Yanıt**

Başarılı yanıt (200 OK)  
Başlıklar:  
Content-Type: application/octet-stream // veya CSV çıktısı istenirse text/csv  
Content-Disposition: attachment; filename="translated.xlsx"  
Content-Length: <bayt cinsinden boyut>

Gövde:  
<çevrilmiş elektronik tablo dosyasını içeren ikili akış>

Hatalı yanıtlar, `code`, `message` ve isteğe bağlı `details` alanlarını içeren standart Aspose.Cells Cloud hata modeline (application/json) uyar.

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)    | Geçersiz veya eksik JWT jetonu.                                   |
| 413 | Payload Too Large (Aşırı Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.                            |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                       |

## **Translate Spreadsheet API** nerede kullanılmalıdır?

- **Uluslararası Finansal Raporlama** – Çeyreklik Excel raporlarını formülleri ve grafik düzenini koruyarak bölgesel ofisler için birden fazla dile çevirin.
- **Çok Dilli Pazarlama Kontrol Panelleri** – Küresel ekipler için satış performansı kontrol panellerinin yerelleştirilmiş sürümlerini otomatik olarak oluşturun.
- **Eğitim İçerik Dağıtımı** – Farklı ülkelerdeki öğrenciler için manuel kopyalama-yapıştırma yapmadan not defterlerini, ödev sayfalarını veya müfredata yönelik elektronik tabloları çevirin.
- **Düzenleyici Uyumluluk** – Doğrulama kurallarını ve veri doğrulama listelerini koruyan, dil özgünlüğüne uygun uyumluluk elektronik tabloları oluşturun.

## **Translate Spreadsheet API**’yi neden kullanmalısınız?

- **AI destekli doğruluk** – Bağlamı anlayan, yüksek kaliteli dil dönüşümü için en gelişmiş nöral çeviri modellerini kullanır.
- **Düzen bozulması yok** – Hücre formüllerini, koşullu formatlamayı, grafikleri ve sayfa sıralamasını kaynaktakiyle tamamen aynı şekilde korur.
- **Tek istekle çok sayfalı işleme** – Sayfa başına döngü gerektirmeden tek bir istekte tüm çalışma sayfalarını çevirir.
- **Kolay bulut entegrasyonu** – Aspose.Cells Cloud kimlik doğrulama ile uyumlu çalışır; CI/CD, sunucusuz işlevler veya kurumsal arka uçlarda otomatik akışlar oluşturmanıza olanak tanır.

## SDK ile **Translate Spreadsheet API** Nasıl Kullanılır?

### **Translate Spreadsheet API** Spesifikasyonu

[Translate Spreadsheet API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet), doğrudan bir web tarayıcısından REST etkileşimlerini gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

## Excel API SDK

### **Aspose.Cells Cloud SDK** Kullanın

SDK kullanmak, düşük seviye detayları ortadan kaldırarak, elektronik tabloyu başka bir elektronik tabloyla birleştirmek gibi işlemleri kısa kodla hızlıca geliştirmenin en hızlı yoludur.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.  
Aşağıdaki kod örnekleri, çeşitli SDK’larla Aspose.Cells web hizmetlerinin nasıl kullanılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}