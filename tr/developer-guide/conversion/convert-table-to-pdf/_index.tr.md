---
title: "Aspose.Cells Cloud Web API - Yerel Excel Tablo Verilerini PDF Dosyasına Dönüştürme - Ücretsiz Çevrimiçi Araç"
second_title: "Belge"
ArticleTitle: "Yerel Elektronik Tablo Tablo Verilerini PDF Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktitle: "Tabloyu PDF'ye Dönüştür"
type: docs
url: /tr/convert-table-to-pdf/
keywords: "Aspose.Cells, Excel'den PDF'ye, Tablo dönüşümü, Bulut API"
description: "Aspose.Cells Cloud REST API kullanarak yerel bir Excel tablosunu hızlı bir şekilde PDF dosyasına dönüştürün."
weight: 100
---

Bulut API kullanarak yerel bir Excel dosyasından tablo verilerini bir PDF dosyasına dışa aktarın.

## **Tabloyu PDF'ye Dönüştürme API'si**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı  | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                       |
| :------------- | :----- | :------------------------- | :--------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya  | FormData                   | Dönüştürülecek elektronik tablo dosyasını yükleyin.                                            |
| worksheet      | Metin  | Sorgu                      | Elektronik tablonun çalışma sayfası adı.                                                       |
| tableName      | Metin  | Sorgu                      | Dönüştürülecek tablonun adı.                                                                    |
| outPath        | Metin  | Sorgu                      | (İsteğe bağlı) Dönüştürülen PDF'in saklanacağı klasör yolu. Varsayılan değer null'dır.          |
| outStorageName | Metin  | Sorgu                      | Çıktı dosyası depolama alanının adını belirtin.                                                 |
| fontsLocation  | Metin  | Sorgu                      | PDF için özel yazı tiplerini kullanın.                                                         |
| region         | Metin  | Sorgu                      | Elektronik tablo için bölge ayarını belirtir.                                                  |
| password       | Metin  | Sorgu                      | Elektronik tablo dosyasına erişim için parola.                                                 |

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

**Örnek yanıt başlıkları**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**HTTP Durum Kodları**

| Kod  | Anlamı                | Açıklama                                                             |
| ---- | --------------------- | -------------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.       |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                   |
| 413  | Yük Çok Büyük         | Yüklenecek dosya boyut limitini aşıyor.                             |
| 500  | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                           |

## **Tabloyu PDF'ye Dönüştür API'si Nerede Kullanılmalıdır?**

- **Finansal Tablolar**: Bilanço, gelir tablosu (belirli tablolar) gibi raporları denetim için uygun belgeler olarak PDF'e dönüştürün.
- **Satış Raporları**: Satış panolarını veya komisyon hesaplamalarını dağıtıma hazır PDF'lere dönüştürün.
- **İşletme Göstergeleri**: KPI tablolarını ve performans metriklerini resmi PDF raporları olarak dışa aktarın.
- **Sözleşme Verileri**: Fiyatlandırma tablolarını ve hizmet seviyesi anlaşmalarını elektronik tablolardan PDF ekleri olarak dışa aktarın.
- **Denetim Izgaları**: Finansal veri tablolarını düzenlenemez PDF kanıtları olarak kaydedin.
- **Portföy Özeti**: Yatırım performansı tablolarını müşteriye uygun PDF raporları olarak dışa aktarın.
- **Kalite Kontrol Raporları**: Gözetim veri tablolarını uyumluluk kayıtları için PDF'e dönüştürün.
- **Stok Özeti**: Stok düzeyi tablolarını yönetim incelemesi için PDF'e dönüştürün.

## **Neden Tabloyu PDF'ye Dönüştür API'si Kullanmalısınız?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı belgelerle birlikte gelir. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında, geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önce yüklemek zorunda kalmadan tablo verilerini dönüştürebilirsiniz; bu, depolama alanını tasarruf eder ve maliyetleri düşürür.
- **Karmaşık Excel Biçimlendirmesini Korur** evrensel olarak erişilebilir bir PDF formatında.

## **Tabloyu PDF'ye Dönüştür API'si Nasıl SDK'larla Kullanılır?**

### Tabloyu PDF'ye Dönüştür API Spesifikasyonu

[Tabloyu PDF'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF), REST etkileşimlerini doğrudan bir web tarayıcısından yürütmek için erişilebilir bir programlama arayüzü sağlar.
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
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

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak elektronik tablo tablo verilerini minimal kodla PDF dosyasına dönüştürmenizi sağlayan en hızlı geliştirme yöntemidir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}