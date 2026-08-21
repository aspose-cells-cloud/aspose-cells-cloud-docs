---
title: "Aspose.Cells Cloud Web API – Yerel Excel Tablo Verilerini JSON Dosyasına Dönüştürme"
second_title: "Belge"
ArticleTitle: "Yerel Elektronik Tablo Tablo Verilerini JSON Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Tabloyu JSON'a Dönüştür"
type: docs
url: /tr/convert-table-to-json/
keywords: "Excel, API, JSON, dönüştürme, bulut, dosya, elektronik tablo"
description: "Aspose.Cells Cloud API'sini kullanarak yerel bir Excel tablosunu tek bir PUT isteğiyle JSON dosyasına dönüştürün. cURL örneği, parametreler ve C#, Java, Python ve diğerleri için SDK kod parçacıklarını içerir."
weight: 100
---

Aspose.Cells Cloud Web API ile yerel bir elektronik tabloyu/Excel tablosunu **JSON** dosyasına dönüştürün.

## **Tabloyu JSON'a Dönüştür API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/json
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür    | Konum     | Açıklama                                                                                      |
| ------------------ | ------ | --------- | ----------------------------------------------------------------------------------------------|
| **Spreadsheet**    | Dosya  | FormVerisi | Yüklenecek Excel dosyası.                                                                      |
| **worksheet**      | Dize   | Sorgu     | Tabloyu içeren çalışma sayfasının adı.                                                         |
| **tableName**      | Dize   | Sorgu     | Dönüştürülecek tablonun adı.                                                                    |
| **outPath**        | Dize   | Sorgu     | (İsteğe bağlı) Oluşan JSON dosyasının depolanacağı klasör yolu; varsayılan **null**.            |
| **outStorageName** | Dize   | Sorgu     | (İsteğe bağlı) Çıktı dosyasının yerleştirileceği depo adı.                                     |
| **fontsLocation**  | Dize   | Sorgu     | (İsteğe bağlı) Dönüştürme sırasında kullanılan özel yazı tiplerinin yolu.                       |
| **region**         | Dize   | Sorgu     | (İsteğe bağlı) Çalışma kitabının bölgesel ayarları.                                             |
| **password**       | Dize   | Sorgu     | (İsteğe bağlı) Korumalı bir çalışma kitabını açmak için parola.                                 |

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
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413  | İçerik Çok Büyük      | Yüklene dosya boyut sınırını aşıyor.                             |
| 500  | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                       |

## **Tabloyu JSON'a Dönüştür API Hangi Durumlarda Kullanılmalı?**

- **Canlı Kontrol Panelleri** – Canlı Excel verilerini Chart.js veya D3.js gibi grafik kütüphaneleri için JSON’a dönüştürün.
- **Elektronik Tablo Hizmeti Olarak Sunma** – Excel tablolarını diğer mikroservisler için JSON uç noktaları olarak sunun.
- **Webhook Yükleri** – Elektronik tablo verilerini webhook bildirimleri için JSON’a dönüştürün.
- **Hızlı Veri Prototipleme** – Temizlenmiş Excel verilerini Python veya R analizi için hızlıca JSON’a dönüştürün.
- **Makine Öğrenimi İşlem Hatları** – İşletme elektronik tablolarında depolanan eğitim verilerini önişleyin.
- **E-Ticaret İşlemleri** – Ürün kataloğlarını veya fiyat listelerini JSON üzerinden web sitelerine senkronize edin.
- **Raporlama Otomasyonu** – Otomatik raporlama için finansal modellerden JSON beslemeleri oluşturun.
- **Uygulama Yapılandırması** – Özellik bayraklarını, ayarları veya A/B test parametrelerini Excel → JSON olarak yönetin.
- **Çok Dilli Desteğ** – Yerelleştirme elektronik tablolarını i18n kütüphaneleri için JSON’a dönüştürün.
- **Dinamik Menüler/Navigasyon** – Web sitesi navigasyon yapılarını Excel'de saklayın ve JSON olarak dağıtın.

## **Neden Tabloyu JSON'a Dönüştür API Kullanmalısınız?**

- **Geliştirici Dostu** – Aspose.Cells Cloud, birçok dil için SDK sunar; böylece geliştirme çabasını azaltır ve kapsamlı belgeler sağlar.
- **Maliyet Etkin** – Çalışma kitabını önceden yüklemek zorunda kalmadan tablo verilerini dönüştürün; bu, depolama alanını tasarruf eder ve maliyetleri azaltır.
- **Modern Web ve Mobil Uyumluluk** – JSON, web'in yerel veri dili; API, karmaşık ayrıştırma gerektirmeden doğrudan React, Vue, Angular, mobil uygulamalar veya tek sayfalı uygulamalara canlı elektronik tablo verisi sağlar.
- **Geniş Dil Desteği** – JSON, neredeyse tüm programlama dili, veritabanı ve web hizmetleriyle çalışır.
- **Yapılandırılmış Veri Koruması**
  - **Akıllı Yapı Algılama** – Tablolu verileri otomatik olarak uygun JSON dizilerine/objelerine dönüştürür.
  - **Başlık Eşleme** – Temiz obje yapıları için ilk satırı JSON anahtarları olarak kullanır.
  - **Veri Türü Koruması** – Sayıları, tarihleri ve boolean değerlerini (yalnızca metin değil) korur.

_Sürüm Geçmişi:_ Tabloyu JSON'a Dönüştür uç noktası, API sürümü **v4.0** (2024) ile tanıtılmış olup mevcut kararlı sürüm olarak kalmaktadır. Eski v3.x uç noktaları kullanımdan kaldırılmıştır.

## **Tabloyu JSON'a Dönüştür API Nasıl SDK İle Kullanılır?**

### Tabloyu JSON'a Dönüştür API Spesifikasyonu

[Tabloyu JSON'a Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToJson){:target="\_blank" rel="noopener noreferrer"}, web tarayıcısından doğrudan REST etkileşimlerini mümkün kılan genel erişilebilir bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye isteklerde nasıl bulunulacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/json?worksheet=Sheet1&tableName=MyTable" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/your/file.xlsx" \
     -F "outPath=output/folder" \
     -F "outStorageName=MyStorage"
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

```
{
 "Code": 200,
 "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak bir elektronik tablo tablosunu JSON dosyasına minimal kodla dönüştürmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için resmi GitHub deposuna bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetleriyle nasıl etkileşim kurulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToJson.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToJson.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToJson.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToJson.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToJson.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToJson.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToJson.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToJson.go" >}}  
{{</tab>}}  
{{< /tabs >}}