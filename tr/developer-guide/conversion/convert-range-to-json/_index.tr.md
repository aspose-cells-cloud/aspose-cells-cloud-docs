---
title: "Aspose.Cells Cloud Web API - Yerel Excel Aralık Verisini JSON Dosyasına Dönüştür - Ücretsiz Çevrimİçi Araç"
secondtitle: "Belge"
ArticleTitle: "Yerel Elektronik Tablo Aralık Verisini JSON Dosyasına Nasıl Dönüştürülür: Adım Adım Kılavuz"
linktype: "Dökümanlar"
url: /tr/convert-range-to-json/
keywords: "aralığı json'a dönüştür, Aspose.Cells Cloud, Excel'den JSON'a, elektronik tablo dönüştürme, API"
description: "Aspose.Cells Cloud API kullanarak yerel bir Excel elektronik tablosundan belirli bir aralığı JSON'a dönüştürün."
weight: 100
---

Yerel bir Excel dosyasından aralık verisini bir JSON dosyasına Cloud API kullanarak dışa aktarın.

## **Aralığı JSON'a Dönüştür API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                   |
| ------------- | ------- | ---------------------------- | -------------------------------------------------------------------------- |
| Spreadsheet   | Dosya   | FormData                     | Elektronik tablo dosyasını yükleyin.                                        |
| worksheet     | Dize    | Sorgu                        | Elektronik tablodaki Çalışma Sayfası adı.                                   |
| range         | Dize    | Sorgu                        | Dönüştürülecek hücre alanı, örneğin A1:C10.                                 |
| outPath       | Dize    | Sorgu                        | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu; varsayılan null. |
| outStorageName| Dize    | Sorgu                        | Çıkış dosyası deposunun adı.                                                |
| fontsLocation | Dize    | Sorgu                        | Kişisel kullanım için özel yazı tiplerinin depolanacağı konum.              |
| region        | Dize    | Sorgu                        | Elektronik tablo bölge ayarı.                                               |
| password      | Dize    | Sorgu                        | Elektronik tablo dosyasını açmak için şifre.                                |

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

| Kod | Anlamı                | Açıklama                                                        |
| --- | --------------------- | --------------------------------------------------------------- |
| 200 | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                              |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                           |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                      |

## **Aralığı JSON'a Dönüştür API’yi Nerede Kullanmalısınız?**

- Gerçek zamanlı dashboard’lar: Chart.js veya D3.js gibi çizim kütüphaneleri için canlı Excel verilerini JSON’a dönüştürün.
- Elektronik tablo-hizmet-olarak (Spreadsheet-as-a-Service): Diğer servisler için Excel aralıklarını JSON uç noktaları olarak açın.
- Webhook yükleri: Webhook bildirimleri için elektronik tablo verilerini JSON’a dönüştürün.
- Hızlı veri prototipleme: Temizlenmiş Excel verilerini Python veya R analizi için hızlıca JSON’a dönüştürün.
- Makine öğrenimi süreçleri: İşletme tarafından yönetilen elektronik tablolardan eğitim verilerini ön işleme tabi tutun.
- E-ticaret operasyonları: Ürün kataloglarını veya fiyat listelerini JSON aracılığıyla web siteleriyle senkronize edin.
- Raporlama otomasyonu: Finansal modellerden otomatik raporlama için JSON veri beslemeleri oluşturun.
- Uygulama yapılandırması: Özellik bayraklarını, ayarları veya A/B test parametrelerini Excel’den JSON’a yönetin.
- Çok dilli destek: Yerelleştirme elektronik tablolarını i18n kütüphaneleri için JSON’a dönüştürün.
- Dinamik menüler/navigasyon: Web sitesi navigasyon yapılarını Excel’de depolayın ve JSON olarak dağıtın.

_Diğer dönüştürme seçenekleri için [Aralığı CSV'ye Dönüştür](/convert-range-to-csv/) kılavuzuna bakın._

## **Aralığı JSON'a Dönüştür API’yi Neden Kullanmalısınız?**

- **SDK desteği**: Aspose.Cells Cloud, birden fazla dil için kütüphaneler sunar; böylece özel kod miktarı azalır.
- **Depolama maliyetlerini azaltma**: Tüm çalışma kitabının önceden yüklenmesine gerek kalmadan aralık dönüştürülebilir; bu da depolama alanını tasarruf ettirir.
- **Web ve mobil uygulamalarla uyumluluk**: JSON, React, Vue ve Angular gibi modern JavaScript çerçeveleri için yerel veri formatıdır.
- **Geniş dil desteği**: Neredeyse tüm programlama dilleri ve veritabanları JSON consumption yapabilir.
- **Yapılandırılmış veri koruma**
  - **Akıllı yapı algılama**: Tablolama verilerini otomatik olarak uygun JSON dizilerine veya nesnelerine dönüştürür.
  - **Başlık eşleme**: İlk satırı temiz nesne yapıları için JSON anahtarları olarak kullanır.
  - **Veri türü koruması**: Düz metin yerine sayı, tarih ve boolean türlerini korur.

## **SDK’lerle Aralığı JSON’a Dönüştür API Nasıl Kullanılır?**

### **Aralığı JSON’a Dönüştür API Özellikleri**

[Aralığı JSON’a Dönüştür API Özellikleri](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/yolunuz/dosyanız.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **Aspose.Cells Cloud SDK’lerini Kullanın**

SDK kullanmak, düşük seviye detayları soyutlayarak aralık verisini JSON dosyasına dönüştürmek için kısa ve net kodla geliştirme yapmanın en hızlı yoludur.  
Aspose.Cells Cloud SDK’lerinin tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’ler kullanarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}