---
title: "Aspose.Cells Cloud Web API - Bir Elektronik Tablo Tablosunun Verilerini CSV Dosyasına Dönüştür - Ücretsiz Çevrimiçi Araç"
secondtitle: "Belge"
ArticleTitle: "Elektronik Tablo Tablo Verilerini CSV Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Tabloyu CSV'ye Dönüştür"
type: docs
url: /tr/convert-table-to-csv/
keywords: "Aspose.Cells Cloud, tablo'dan csv'ye, elektronik tablo dönüştürme, Excel'den csv'ye, API, REST, veri dışa aktarımı"
description: "Aspose.Cells Cloud API kullanarak bir Excel elektronik tablodan bir tabloyu hızlıca bir CSV dosyasına dönüştürün."
weight: 100
---

Yerel bir Excel dosyasından bir tablonun verilerini Cloud API kullanarak bir CSV dosyasına dışa aktarın.

## **Tabloyu CSV'ye Dönüştürme API'si**

### Web API'si

```http
PUT http://api.aspose.cloud/v4.0/cells/convert/table/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                             |
| -------------- | ------ | --------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya  | FormData                    | Elektronik tablo dosyasını yükleyin.                                                                                                            |
| worksheet      | Dize   | Sorgu                       | Elektronik tablodaki çalışma sayfasının adı.                                                                                               |
| tableName      | Dize   | Sorgu                       | Dönüştürülecek tablonun adı.                                                                                                      |
| outPath        | Dize   | Sorgu                       | (İsteğe bağlı) Elektronik tablonun depolandığı klasör yolu; varsayılan değer null'dır.                                                                  |
| outStorageName | Dize   | Sorgu                       | Çıktı dosyası için depo adı.                                                                                                |
| fontsLocation  | Dize   | Sorgu                       | Özel yazı tiplerinin kullanılacağı yol.                                                                                                            |
| region         | Dize   | Sorgu                       | Elektronik tablonun bölge/dil ayarı (örn., `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmayı ve yerel ayara özgü davranışı etkiler. |
| password       | Dize   | Sorgu                       | Elektronik tablo dosyasını açmak için şifre.                                                                                              |

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

| Kod | Anlamı               | Açıklama                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Tamam                | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Hatalı İstek           | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü).      |
| 401  | Yetkisiz          | Geçersiz veya eksik JWT belirteci.                                     |
| 413  | Yük Çok Büyük     | Yüklenen dosya boyut sınırını aşıyor.                                 |
| 500  | İç Sunucu Hatası | Beklenmeyen sunucu hatası.                                          |

## **Tabloyu CSV'ye Dönüştürme API'si Nerede Kullanılmalıdır?**

- **Veritabanı Göçü**: SQL veritabanlarına (MySQL, PostgreSQL, SQL Server) toplu içe aktarma için Excel tablolarını CSV'ye dönüştürün.
- **Veri Ambarı Yüklemesi**: Snowflake, Redshift veya BigQuery’ye yüklemek için Excel tabanlı raporlama tablolarını CSV’ye dönüştürün.
- **Toplu API Yükleri**: REST servislerine toplu API yüklemeleri için Excel tablo verilerini CSV’ye dönüştürün.
- **Hizmetten Hizmete İletişim**: Mikroservisler arasında hafif bir veri değişimi formatı olarak CSV kullanın.
- **Makine Öğrenimi Veri Hazırlığı**: Python/R makine öğrenimi kütüphaneleri için Excel'den özellik tablolarını CSV'ye dönüştürün.
- **İstatistiksel Analiz**: SPSS, SAS veya Stata içe aktarması için araştırma verisi tablolarını CSV'ye dönüştürün.
- **İçerik Göçü**: CSV üzerinden yapılandırılmış içeriği CMS sistemlerine taşıyın.

## **Neden Tabloyu CSV'ye Dönüştürme API'sini Kullanmalısınız?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar, hızlı geliştirme sağlar ve kapsamlı belgeler içerir. Özel çözümler oluşturmakla karşılaştırıldığında, geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önce yüklemek zorunda kalmadan tablo verilerini dönüştürebilirsiniz; bu, depolama alanından tasarruf sağlar ve maliyetleri düşürür.
- **Biçimlendirme olmadan saf veri çıkarma**.
- **CSV, neredeyse tüm sistemler tarafından desteklenir**:
  - Veritabanları (tüm büyük ilişkisel veritabanları)
  - Programlama dilleri (tümünde yerel ayrıştırıcılar mevcuttur)
  - İş zekâsı araçları (Tableau, Power BI, Looker)
  - Elektronik tablo yazılımları (Excel, Google Sheets, LibreOffice)
  - Komut satırı araçları (awk, sed, grep)

## **Tabloyu CSV'ye Dönüştürme API'si SDK'lar ile Nasıl Kullanılır?**

### Tabloyu CSV'ye Dönüştürme API Spesifikasyonu

[Tabloyu CSV'ye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToCSV), doğrudan bir web tarayıcısından REST etkileşimlerine izin veren herkese açık bir programlama arayüzü sağlar.
cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/csv?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.csv
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

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak minimal kodla elektronik tablo tablo verilerini bir CSV dosyasına dönüştürmenizi sağlayan en hızlı gelişim yoludur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapılacağını göstermektedir:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}

---