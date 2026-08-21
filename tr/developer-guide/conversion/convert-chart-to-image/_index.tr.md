---
title: "Aspose.Cells Cloud Web API - Excel Grafiğini Görüntüye Dönüştür - Ücretsiz Çevrimiçi Araç"
second_title: "Belge"
ArticleTitle: "Elektronik Tablo Grafiğini Görüntüye Nasıl Dönüştürürsünüz: Adım Adım Kılavuz"
linktitle: "Grafiği Görüntüye Dönüştür"
type: docs
url: /tr/convert-chart-to-image/
keywords: "grafiği görüntüye dönüştür, Aspose.Cells, Excel grafik dışa aktarımı, PNG, SVG, JPEG, BMP, TIFF"
description: "Aspose.Cells Cloud Web API’yi kullanarak bir Excel grafiğini doğrudan bir elektronik tablo dosyasından PNG, SVG, TIFF, JPEG veya BMP görüntülerine dönüştürün."
weight: 100
---

Excel grafikleri, çalışma sayfalarına gömülü olabilen verilerin görsel temsilidir. Bu grafikleri görüntü formatlarına dönüştürmek, Excel’e ihtiyaç duymadan belgeler, web sayfaları ve raporlar arasında kolayca yeniden kullanılabilmesini sağlar.

Yerel bir elektronik tablo veya Excel dosyasından bir grafiği bir görüntü dosyasına dönüştürün. Desteklenen **GÖRÜNTÜ FORMATLARI:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>, <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>, <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>, <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>, <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **Grafiği Görüntüye Dönüştür API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür      | Yol/Sorgu Dizesi/HTTPBody | Açıklama                                                                              | Gerekli  |
| :------------ | :------- | :------------------------ | :------------------------------------------------------------------------------------ | :------- |
| Spreadsheet   | Dosya    | FormData                  | Grafiği içeren elektronik tablo dosyasını yükleyin.                                   | Evet     |
| worksheet     | Dize     | Sorgu                     | Uygulanabilirse çalışma sayfası adını belirtin.                                        | Hayır    |
| chartIndex    | Tamsayı  | Sorgu                     | Dönüştürülecek grafiğin dizini.                                                        | Evet     |
| format        | Dize     | Sorgu                     | (Gerekli) İstenen görüntü türü (örn. svg, png, jpg).                                 | Evet     |
| outPath       | Dize     | Sorgu                     | (İsteğe bağlı) Çıktı dosyasının kaydedileceği klasör yolu; varsayılan değer null’dır. | Hayır    |
| outStorageName| Dize     | Sorgu                     | Çıktı dosyası için depo adı.                                                           | Hayır    |
| fontsLocation | Dize     | Sorgu                     | Gerekirse özel yazı tiplerini belirtin.                                               | Hayır    |
| region        | Dize     | Sorgu                     | Elektronik tablo bölgesini ayarlayın.                                                  | Hayır    |
| password      | Dize     | Sorgu                     | Elektronik tablo dosyasını açmak için parola.                                         | Hayır    |

## **Yanıt**

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

| Kod | Anlamı                | Açıklama                                                           |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.     |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü).|
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                 |
| 413  | İçerik Çok Büyük      | Yüklenen dosya boyut limitini aşıyor.                              |
| 500  | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                         |

## Grafiği Görüntüye Dönüştür API’yi Nerede Kullanmalısınız?

- **Rapor Oluşturma ve Gösterge Tabloları**: Excel verilerinden grafikleri otomatik olarak görüntülere (PNG, JPEG vb.) dönüştürün ve bunları PDF raporlarında, web gösterge tablolarında veya PowerPoint sunumlarında gömün.
- **Web/E-posta Uygulamaları**: Kullanıcıların Excel dosyalarını indirmesini veya açmasını gerektirmeden doğrudan web sayfalarında veya e-postalarda grafik görüntülerini sunun. Dinamik raporlama araçları, haber bültenleri veya otomatik bildirimler için faydalıdır.
- **Belge İşleme İş Akışları**: Excel'den gelen grafiklerin diğer formatlara (Word, PDF, HTML) eklenmesini gerektiren otomatik süreçlere (örn. fatura, analiz) entegre edin.
- **Mobil/Masaüstü Uygulamaları**: Tam elektronik tabloyu işlemek gereksiz veya mümkün olmayan uygulamalarda Excel grafiklerini gösterin.
- **Arşivleme ve Görselleştirme**: Excel bağımlılığı olmadan uzun süreli depolama, küçük resimler veya hızlı ön izlemeler için grafikleri bağımsız görüntü olarak kaydedin.

## Grafiği Görüntüye Dönüştür API’yi Neden Kullanmalısınız?

- **Görsel Sadakati Koruma**: Excel’de görünenle aynı renk, etiket ve ölçekleme dahil tam grafik formatını korur, profesyonel kaliteli çıktı sağlar.
- **Platformdan Bağımsız**: Excel kurulumuna ihtiyaç yoktur. REST API üzerinden çapraz platform (Windows, Linux, macOS) çalışır; bulut tabanlı veya sunucu tarafı uygulamalar için uygundur.
- **Otomasyon ve Ölçeklenebilirlik**: Birden fazla grafiği veya dosyayı programlı olarak toplu olarak dönüştürün; manuel dışa aktarmaya göre zaman tasarrufu sağlar. Bulutta büyük hacimleri verimli şekilde işler.
- **Esnek Çıktı Formatları**: Popüler görüntü formatlarını (PNG, JPG, BMP, SVG vb.) destekler; çeşitli sistemler ve medya ile entegrasyonu sağlar.
- **Güvenli ve Güvenilir**: Dosyaları Aspose’un bulut ortamında işler; hassas verileri istemci tarafı araçlarına açmaz. Yüksek kullanılabilirlik ve tutarlı performans.
- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; hızlı geliştirme sağlar ve kapsamlı belgelerle birlikte gelir. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında, geliştirme yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önce yüklemek zorunda kalmadan grafikleri dönüştürebilirsiniz; bu, depolama alanından tasarruf sağlar ve maliyetleri düşürür.

## Grafiği Görüntüye Dönüştür API’yi SDK’larla Nasıl Kullanırsınız?

### Grafiği Görüntüye Dönüştür API Belirtimi

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">Grafiği Görüntüye Dönüştür API Belirtimi</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak grafiği görüntüye dönüştürmek için kısa kodla geliştirme yapmanın en hızlı yoludur.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}