---
title: "Aspose.Cells Cloud API – Excel Grafiğini PDF'ye Dönüştürme"
second_title: "Doküman"
ArticleTitle: "Yerel Bir Elektronik Tablo Grafiğini PDF Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Grafiği PDF'ye Dönüştür"
type: docs
url: /tr/convert-chart-to-pdf/
keywords: "Aspose Cells, grafik, PDF, Excel, dönüştürme, bulut API"
description: "Aspose.Cells Cloud REST API kullanarak yerel Excel dosyalarındaki grafikleri PDF formatına dışa aktarın. XLSX ve XLS dosyalarını destekler."
weight: 100
---

Bulut API kullanarak yerel bir Excel dosyasındaki grafikleri [PDF](https://docs.fileformat.com/pdf/) formatına dönüştürün.

## **Grafiği PDF'ye Dönüştürme Web API'si**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı    | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                |
| ---------------- | ------- | ---------------------------- | --------------------------------------------------------------------------------------- |
| Spreadsheet      | Dosya   | FormData                     | Elektronik tablo dosyasını yükleyin.                                                    |
| worksheet        | Metin   | Sorgu                        | Grafiğin bulunduğu çalışma sayfasının adı.                                              |
| chartIndex       | Tamsayı | Sorgu                        | Dönüştürülecek grafiğin indeksi.                                                        |
| outPath          | Metin   | Sorgu                        | (İsteğe bağlı) Dönüştürülen dosyanın saklandığı klasör yolu. Varsayılan değer null’dır. |
| outStorageName   | Metin   | Sorgu                        | Çıktı dosyasının depo adı.                                                              |
| fontsLocation    | Metin   | Sorgu                        | Gerekiyorsa özel yazı tiplerini kullanın.                                              |
| region           | Metin   | Sorgu                        | Elektronik tablonun bölge ayarı.                                                        |
| password         | Metin   | Sorgu                        | Elektronik tablo dosyasını açmak için parola.                                          |

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

| Kod | Anlamı               | Açıklama                                                         |
| --- | -------------------- | ---------------------------------------------------------------- |
| 200 | Tamam                | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.  |
| 400 | Geçersiz İstek       | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz İstek       | Geçersiz veya eksik JWT belirteci.                              |
| 413 | Yük Çok Büyük        | Yüklenen dosya boyut sınırını aşıyor.                           |
| 500 | İç Sunucu Hatası     | Beklenmeyen sunucu hatası.                                      |

## Grafiği PDF'ye Dönüştürme API'si nerede kullanılmalıdır?

### **1. İş Raporlama ve Otomasyonu**

- **Finans Departmanları**: Aylık finansal rapor grafikleri → PDF arşivleme  
- **Satış Takımları**: Performans eğilim grafikleri → PDF müşteri raporları  
- **Pazarlama Analitikleri**: Kampanya performans grafikleri → PDF yöneticilere sunumlar  
- **Operasyon Yönetimi**: Üretim izleme grafikleri → PDF uyumluluk belgeleri  

### **2. Yazılım Geliştirme ve Entegrasyonu**

- **SaaS Uygulamaları**: Kullanıcı tarafından oluşturulan grafik verileri → indirilebilir PDF raporları  
- **Kurumsal Sistemler**: ERP/CRM sistemleri grafikleri → PDF denetim belgeleri  
- **Mobil Uygulamalar**: Uygulama içi analitik grafikleri → paylaşılabilir PDF dosyaları  
- **Web Uygulamaları**: Gösterge paneli grafikleri → PDF dışa aktarma işlevselliği  

### **3. Doküman İşleme İş Akışları**

- **Toplu İşlem**: Birden fazla Excel dosyası grafiği aynı anda PDF’ye dönüştürülür  
- **Zamanlanmış Görevler**: Günlük/haftalık grafik raporlarının otomatik oluşturulması  
- **Şablon Tabanlı Çıktılar**: Standart grafik formatları → PDF dokümanları  
- **Doküman Birleştirme**: Grafikleri diğer içeriklerle birlikte PDF formatında birleştirme  

### **4. Sektöre Özel Uygulamalar**

- **Araştırma Kurumları**: Deneysel veri grafikleri → PDF araştırma makalesi çizelgeleri  
- **Eğitim Sektörü**: Eğitim materyali grafikleri → PDF ders materyalleri  
- **Danışmanlık Firmaları**: Analiz grafikleri → PDF müşteri teslimatları  
- **Üretim**: Kalite kontrol grafikleri → PDF muayene raporları  
- **Sağlık Hizmetleri**: Hasta verisi grafikleri → PDF tıbbi kayıtlar  
- **Devlet Kurumları**: İstatistiksel grafikler → PDF resmi yayınlar  

### **5. İçerik Yönetimi ve Dağıtımı**

- **Dijital Varlık Yönetimi**: Grafiklerin standartlaştırılmış PDF formatında arşivlenmesi  
- **Bilgi Tabanları**: Gömülü PDF grafikli teknik dokümantasyon  
- **Müşteri Portalleri**: İlgili taraflara güvenli PDF rapor teslimi  
- **Düzenleyici Uyumluluk**: Denetim için hazır PDF dokümantasyon oluşturma  

## Grafiği PDF'ye Dönüştürme API'si neden kullanılmalıdır?

- Çalışma kitabını önceden yüklemeksizin grafikleri dönüştürebilirsiniz; bu, depolama alanından tasarruf sağlar ve maliyetleri düşürür.  
- Geliştirme, mevcut Aspose.Cells Cloud SDK’ları aracılığıyla hızlıca tamamlanabilir.  
- **Basit Entegrasyon**: Açık dokümantasyonlu REST API.  
- **Ölçeklenebilir Mimari**: Küçük ölçekli işlerden kurumsal ölçekli işlemlere kadar tüm iş yüklerini işleyebilir.  

## Grafiği PDF'ye Dönüştürme API'si SDK ile nasıl kullanılır?

### Grafiği PDF'ye Dönüştürme API Spesifikasyonu

[Grafiği PDF'ye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

## Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviye detaylardan kurtularak minimum kodla bir grafiği PDF dosyasına dönüştürmenizi sağlayan en hızlı geliştirme yöntemidir.  
Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web servislerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}