---
title: "Aspose.Cells Cloud Web API – Yapay Zekâ ile Metin Dosyası Çevirisi"
second title: "Belge"
articleTitle: "Aspose.Cells Cloud AI Çeviri API'si ile Metin Dosyalarını Nasıl Çevirebilirsiniz?"
linkTitle: "Metin Dosyası Çevirisi"
type: docs
url: /translate-text-file/
keywords: "Aspose.Cells, Bulut API, Yapay zekâ ile çeviri, metin dosyası çevirisi, çok dilli dönüşüm, REST PUT, hedef dil kodu, dosya yükleme ile çeviri, ham metin çevirisi, elektronik tablo yapay zekâ"
description: "Aspose.Cells Cloud AI TranslateTextFile uç noktasını kullanarak metin dosyalarını desteklenen herhangi bir dile nasıl çevireceğinizi öğrenin. Hem multipart dosya yükleme hem de ham metin yüklemesini destekler, formatlamayı korur ve indirilebilir çevrilmiş dosya döndürür."
weight: 100
---

**TranslateTextFile** uç noktası, Aspose.Cells Cloud yapay zekâ hizmetlerinden yararlanarak bir metin dosyasının içeriğini belirli bir hedef dile çevirir. İki işlem modunu destekler: (1) **Dosya Yükleme Modu** – metin dosyasını multipart/form-data ile gönderir ve çevrilmiş dosyayı alırsınız; (2) **Doğrudan İçerik Modu** – istek gövdesine ham metni gönderir ve çevrilmiş metni doğrudan alırsınız. Hizmet, orijinal satır sonlarını ve formatlamayı korur; dosya adına otomatik olarak "_translated" ekini ekler ve sonucu indirilebilir bir akış olarak döndürür. Belgelerin toplu çevirisi, çok dilli iş akışlarına entegrasyon veya kullanıcı tarafından oluşturulan içeriklerin anlık çevriliş işlemleri için idealdir.

## **Metin Dosyası Çevirisi API'si**

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **İstek Parametreleri:**

| Parametre Adı  | Tür     | Konum      | Zorunlu / Opsiyonel | Açıklama                                                                                                                                                                                                 |
| :------------- | :------ | :--------- | :------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya   | Gerekli      | FormData            | Çevrilecek kaynak metin dosyası. Düz metin (.txt) veya desteklenen bir elektronik tablo formatında olmalıdır. Örnek: "file" adlı multipart/form-data alanı üzerinden `document.txt` dosyasını yükleyin.          |
| targetLanguage | Dize    | Gerekli      | Sorgu               | İstenilen çıktı dili için ISO-639-1 dil kodu (örneğin, İspanyolca için "es", Fransızca için "fr", Almanca için "de"). Kod büyük/küçük harfe duyarsızdır.                                                     |
| region         | Dize    | Opsiyonel    | Sorgu               | Tarih, sayı ve para birimi gibi yerel ayarla ilişkili formatlamayı etkileyen elektronik tablo bölge tanımlayıcısı. Yaygın değerler: "US", "EU", "CN". Atlanırsa, çalışma kitabının orijinal bölge ayarı kullanılır. |
| password       | Dize    | Opsiyonel    | Sorgu               | Şifrelenmiş elektronik tablo dosyalarını açmak için gereken şifre. Düz metin dosyaları için gerekli değildir.                                                                                              |

### **Yanıt**

Başarılı yanıt (200 OK)
Başlıklar:
Content-Type: application/octet-stream // Çevrilmiş dosyanın ikili akışı
Content-Disposition: attachment; filename="<orijinal_ad>\_translated.txt"
Content-Length: <bayt cinsinden boyut>

Gövde: Orijinal satır sonlarını ve formatlamayı koruyan çevrilmiş metni içeren ikili akış.

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                           |
| ---- | --------------------- | ------------------------------------------------------------------ |
| 200  | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.      |
| 400  | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü).      |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                                             |
| 413  | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor.                                 |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                          |

## Metin Dosyası Çevirisi API'si Nerede Kullanılmalıdır?

- **Çok Dilli Belge Portalı** – Kullanıcı kılavuzlarını veya yardım dosyalarını metin belgesi olarak yükleyerek otomatik olarak çevirir, istendiğinde yerelleştirilmiş sürümleri sunar.
- **İçerik Yönetim Sistemleri (CMS)** – Blog yazılarını veya makaleleri uluslararası kitlelere karşı yayınlamadan önce çevirmek için CMS iş akışına entegre edilir.
- **Kurumsal Veri Boru Hatları** – Büyük miktarda CSV veya TXT raporu işleyen toplu işlerde kullanılır; orijinal formatlamayı koruyarak bölgesel ofislerin diline çevirir.
- **Müşteri Desteği Platformları** – Farklı dillerde çalışan destek temsilcilerini desteklemek için gelen düz metin destek taleplerini veya sohbet kayıtlarını gerçek zamanlı olarak çevirir.

## Metin Dosyası Çevirisi API'si Neden Kullanılmalıdır?

- **Yapay Zekâ Tabanlı Doğruluk** – Doğal ve bağlama uyumlu çıktı için en gelişmiş sinirsel çeviri modellerinden yararlanır.
- **Çift Giriş Esnekliği** – Hem dosya yükleme hem de ham metin yüklemesini kabul eder; çeşitli istemci uygulamalarıyla entegrasyonu basitleştirir.
- **Orijinal Düzeni Korur** – Satır sonlarını, girintileri ve özel karakterleri korur; sonrası temizlik gereksinimini ortadan kaldırır.
- **Sorunsuz Dosya İşleme** – Otomatik oluşturulan "_translated" ekli indirilebilir dosyayı döndürür; istemci tarafı kod karmaşıklığını azaltır.

## SDK’larla Metin Dosyası Çevirisi API'sini Nasıl Kullanılır?

### Metin Dosyası Çevirisi API Spesifikasyonu

[Metin Dosyası Çevirisi API Spesifikasyonu](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile), web tarayıcısından doğrudan REST etkileşimlerini gerçekleştirmek için erişilebilir bir programlama arayüzü sağlar.

## Excel API SDK’sı

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanımı, düşük seviye detayları soyutlayarak, bir elektronik tabloyu başka bir elektronik tabloya birleştirmenin kısa kodla yapılmasını sağlayarak geliştirme yapmanın en hızlı yoludur.
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.
Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servisleriyle nasıl etkileşime geçileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}