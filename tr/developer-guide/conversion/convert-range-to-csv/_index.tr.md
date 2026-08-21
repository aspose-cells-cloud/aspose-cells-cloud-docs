---
title: "Excel Aralığını CSV'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
ArticleTitle: "Yerel Bir Elektronik Tablo Aralığını CSV Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Aralığı CSV'ye Dönüştür"
type: docs
url: /tr/convert-range-to-csv/
keywords: "Aspose Cells, Aralığı CSV'ye Dönüştür, Excel'den CSV'ye, Excel API, Bulut Elektronik Tablo, Dönüştür, Excel, CSV, Aspose.Cells, Bulut API"
description: "Aspose.Cells Cloud REST API kullanarak yerel bir Excel çalışma kitabından (XLSX veya XLS) belirli bir aralığı CSV'ye dönüştürmeyi öğrenin. İsteğin sözdizimi, parametreleri, hata yönetimi ve SDK örneklerini içerir."
---

Aspose.Cells Cloud API kullanarak yerel bir Excel dosyasından belirli bir aralığı CSV'ye dışa aktarın.

## **Aralığı CSV'ye Dönüştür API'si**

**Ön Koşullar**  
Bu uç noktayı çağırmak için geçerli bir Aspose Cloud **istemci Kimliği** ve **istemci gizli anahtarı**nızın olması, bir **JWT erişim jetonu** almanız ve kaynak elektronik tablonun **XLSX** veya **XLS** formatında olması gerekir.

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**cURL Örneği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Sayfa1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@sample.xlsx"
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür     | Yol/Sorgu Dizisi/HTTPBody | Açıklama                                                                       |
| :------------- | :------ | :------------------------- | :----------------------------------------------------------------------------- |
| Spreadsheet    | Dosya   | FormData                   | Elektronik tablo dosyasını yükleyin.                                           |
| worksheet      | Dize    | Sorgu                      | Elektronik tablonun çalışma sayfası adı.                                       |
| range          | Dize    | Sorgu                      | Hücre alanını belirtin (örneğin, A1:C10).                                      |
| outPath        | Dize    | Sorgu                      | Çalışma kitabının depolanacağı klasör yolu (isteğe bağlı). Varsayılan değer null'dır. |
| outStorageName | Dize    | Sorgu                      | Çıkış depolama adı.                                                            |
| fontsLocation  | Dize    | Sorgu                      | Gerekirse özel yazı tiplerini belirtin.                                        |
| region         | Dize    | Sorgu                      | Elektronik tablo bölge ayarını tanımlar.                                       |
| password       | Dize    | Sorgu                      | Elektronik tablo dosyasını açmak için gerekli şifre.                           |

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

_Döndürülen CSV içeriğinin örneği (ilk birkaç satır):_

```csv
Ad,Soyad,Tarih,Miktar
Ahmet Yılmaz,2023-01-15,1250.00
Ayşe Demir,2023-01-16,980.50
```

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                         |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.   |
| 400  | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT jetonu.                                   |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                            |
| 500  | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                       |

## Aralığı CSV'ye Dönüştür API'si nerede kullanılmalıdır?

### **1. Veri Dışa Aktarma ve Taşıma Senaryoları**

- **Veritabanı Entegrasyonu**: Belirli Excel aralıklarını doğrudan veritabanı sistemlerine dışa aktarın.
- **Uygulama Entegrasyonu**: Seçili elektronik tablo verilerini SaaS uygulamalarına besleyin.
- **Sistem Geçişi**: Belirli veri aralıklarını eski ve modern sistemler arasında taşıyın.
- **Çapraz Platform Paylaşımı**: Farklı platformlar arasında odaklanmış veri alt kümelerini paylaşın.

### **2. Raporlama ve Analitik**

- **Hedefli Raporlama**: Odaklı analiz için belirli rapor bölümlerini CSV'ye dışa aktarın.
- **Gösterge Paneli Veri Beslemeleri**: Belirli veri aralıklarını BI gösterge paneli araçlarına sağlayın.
- **Performans Metrikleri**: Performans izleme sistemleri için KPI aralıklarını çıkarın.
- **Finansal Raporlama**: Dış denetim için finansal tablo bölümlerini dışa aktarın.

### **3. Geliştirme ve Test**

- **Test Verisi Yönetimi**: Test amaçlarıyla belirli veri aralıklarını dışa aktarın.
- **Geliştirme Ortamları**: Örnek veri aralıklarını geliştirme ekiplerine paylaşın.
- **API Testi**: Belirli elektronik tablo bölümlerinden CSV test verileri oluşturun.
- **Prototip Geliştirme**: Uygulama prototipleri için odaklı veri setleri sağlayın.

### **4. İş Operasyonları**

- **Seçici Veri Paylaşımı**: Belirli veri aralıklarını dışarıdaki ortaklarla paylaşın.
- **Kısmi Veri Yedekleme**: Kritik veri aralıklarını CSV formatında yedekleyin.
- **Bölüm Veri Aktarımı**: Belirli verileri bölümler arasında paylaşın.
- **Uyumluluk Raporlama**: Uyumluluk gönderimleri için düzenleyici veri aralıklarını dışa aktarın.

### **5. Otomasyon İş Akışları**

- **Zamanlanmış Aralık Dışa Aktarmaları**: Belirli aralıkları zamanlanmış şekilde otomatik olarak dışa aktarın.
- **Tetikleyici Tabanlı Çıkarma**: İş olaylarına veya tetikleyicilere göre aralıkları dışa aktarın.
- **İş Akışı Entegrasyonu**: Aralık dışa aktarmalarını iş süreçleri iş akışlarına entegre edin.
- **Toplu Aralık İşleme**: Birden fazla belirli aralığı toplu işlemelerde işleyin.

## Aralığı CSV'ye Dönüştür API'si neden kullanılmalıdır?

- Çalışma kitabını önce yüklemek zorunda kalmadan bir elektronik tablo aralığını dönüştürebilirsiniz; bu, depolama alanından tasarruf sağlar ve maliyetleri düşürür.
- Mevcut Aspose.Cells Cloud SDK'larını kullanarak geliştirme hızlı bir şekilde tamamlanabilir.
- **Basit Entegrasyon**: Net belgelenmiş REST API.
- **Ölçeklenebilir Mimari**: Küçük işletmelerden kurumsal ölçekli işlemlere kadar her şeyi işler.

## Aralığı CSV'ye Dönüştür API'si SDK'larla Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV), web tarayıcısından doğrudan REST etkileşimlerini mümkün kılan genel erişimli bir API'yi tanımlar.

## Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak minimal kodla bir veri aralığını CSV dosyasına dönüştürmenizi sağlayan en hızlı geliştirme yoludur.  
Aspose.Cells Cloud SDK'larının tam listesini [GitHub depomuzda](https://github.com/aspose-cells-cloud) keşfedin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir. Gist'ten yükleme engellenirse, örnekleri doğrudan depodan indirebilirsiniz.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}