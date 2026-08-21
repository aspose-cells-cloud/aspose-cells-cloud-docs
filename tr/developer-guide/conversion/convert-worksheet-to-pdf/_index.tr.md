---
title: "Aspose.Cells Cloud Web API – Yerel Excel Çalışma Sayfasını PDF Dosyasına Dönüştürme – Ücretsiz Çevrimiçi Araç"
second_title: "Belge"
ArticleTitle: "Yerel Elektronik Tablo Çalışma Sayfasını PDF Dosyasına Dönüştürme: Adım Adım Kılavuz"
linktype: "Çalışma Sayfasını PDF'ye Dönüştür"
type: docs
url: /tr/convert-worksheet-to-pdf/
keywords: "Aspose.Cells, Excel'den PDF'ye, çalışma sayfası dönüştürme, REST API, bulut dönüşümü, elektronik tablo PDF, API uç noktası, PDF oluşturma"
description: "Aspose.Cells Cloud API’sini kullanarak yerel bir Excel dosyasından bir çalışma sayfasını hızlı ve güvenli bir şekilde PDF belgesine dönüştürün."
weight: 100
---

Yerel bir Excel dosyasından bir [PDF](https://docs.fileformat.com/pdf/) dosyasına bir çalışma sayfasını Bulut API’si ile dışa aktarın.

## **Çalışma Sayfasını PDF'ye Dönüştürme API'si**

### Web API’si

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür    | Yol/Sorgu Dizesi/HTTPBody | Açıklama                                                         |
| -------------- | ------ | ------------------------- | ---------------------------------------------------------------- |
| ElektronikTablo | Dosya  | FormData                  | Elektronik tablo dosyasını yükleyin.                             |
| worksheet      | String | Sorgu                     | Elektronik tablodaki çalışma sayfasının adı.                      |
| outPath        | String | Sorgu                     | (İsteğe bağlı) Çalışma kitabının saklanacağı klasör yolu; varsayılan null’dir. |
| outStorageName | String | Sorgu                     | Çıktı dosyasının depo adı.                                        |
| fontsLocation  | String | Sorgu                     | PDF için özel yazı tiplerini kullanın.                           |
| region         | String | Sorgu                     | Elektronik tablo bölgesi ayarını tanımlayın.                     |
| password       | String | Sorgu                     | Elektronik tablo dosyasını açmak için gerekli şifre.             |

### **Yanıt**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream",
      "Name": "file"
    }
  }
]
```

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir.  |
| 400  | Hatalı İstek         | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz             | Geçersiz veya eksik JWT belirteci.                                |
| 413  | İçerik Çok Büyük      | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500  | Sunucu İçi Hata       | Beklenmeyen sunucu hatası.                                        |

## **Çalışma Sayfasını PDF'ye Dönüştürme API’sini Nerede Kullanmalısınız?**

- **Finansal Tablolar**: Bilanço, gelir tablosu (belirli tablolar) gibi raporları denetim için uygun belgeler olarak PDF’e dönüştürün.
- **Satış Raporları**: Satış panolarını veya komisyon hesaplamalarını dağıtıma hazır PDF’lere dönüştürün.
- **İşletme Göstergeleri**: KPI tablolarını ve performans metriklerini resmi PDF raporları olarak dışa aktarın.
- **Sözleşme Verileri**: Fiyatlandırma tablolarını ve hizmet düzeyi anlaşmalarını elektronik tablolardan PDF ekleri olarak dışa aktarın.
- **Denetim İzleme Kayıtları**: Finansal çalışma sayfalarını değiştirilemez PDF kanıtları olarak saklayın.
- **Portföy Özeti**: Yatırım performansı tablolarını müşteriye uygun PDF raporları olarak dışa aktarın.
- **Kalite Kontrol Raporları**: Gözetim çalışma sayfalarını uyumluluk kayıtları için PDF’e dışa aktarın.
- **Envanter Özeti**: Stok çalışma sayfalarını yönetim incelemesi için PDF’e dönüştürün.

## **Çalışma Sayfasını PDF'ye Dönüştürme API’sini Neden Kullanmalısınız?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı belgelerle birlikte gelir. Özel grafik oluşturma çözümleri oluşturmak yerine, geliştirme iş yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Çalışma kitabını önce buluta yüklemeksizin tablo verilerini dönüştürebilirsiniz; bu sayede depolama alanından tasarruf sağlayarak maliyetleri düşürürsünüz.
- **Biçimlendirme Koruması**: Karmaşık Excel biçimlendirmesini evrensel olarak erişilebilir bir PDF formatında korur.

## **Çalışma Sayfasını PDF'ye Dönüştürme API’sini SDK’larla Nasıl Kullanılır?**

### Çalışma Sayfasını PDF'ye Dönüştürme API’si Spesifikasyonu

[Çalışma Sayfasını PDF'ye Dönüştürme API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToPDF), herkese açık bir programlama arayüzü sağlar ve doğrudan bir web tarayıcısından REST etkileşimlerini mümkün kılar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/worksheet/json?worksheet=Sheet1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.json
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tablo tablo verilerini PDF dosyasına dönüştürmek için minimum kodla geliştirme yapmanın en hızlı yoludur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertWorksheetToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertWorksheetToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertWorksheetToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertWorksheetToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertWorksheetToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertWorksheetToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertWorksheetToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertWorksheetToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}