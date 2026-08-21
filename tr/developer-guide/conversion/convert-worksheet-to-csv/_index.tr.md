---
title: "Çalışma Sayfasını CSV'ye Dönüştür – Aspose.Cells Cloud API Dokümantasyonu"
second_title: "Doküman"
ArticleTitle: "Aspose.Cells Cloud API Kullanarak Bir Elektronik Tablo Çalışma Sayfasını CSV'ye Nasıl Dönüştürülür"
linktype: "Çalışma Sayfasını CSV'ye Dönüştür"
type: docs
url: /convert-worksheet-to-csv/
keywords: "Aspose.Cells, CSV dönüşümü, çalışma sayfasından CSV'ye, REST API, bulut tablo, Excel'den CSV'ye"
description: "Aspose.Cells Cloud API'sini (v4.0) kullanarak bir Excel dosyasından belirli bir çalışma sayfasını CSV'ye nasıl dönüştüreceğinizi öğrenin. Endpoint, parametreler, örnek cURL, SDK kodu ve hata işleme içerir."
weight: 100
---

**ConvertWorksheetToCsv** uç noktası, yerel bir elektronik tablo dosyasının tek bir çalışma sayfasını tamamen Aspose.Cells Cloud sunucusunda CSV belgesine dönüştürür. Kaynak dosyayı yükleyip hedef çalışma sayfasını belirleyerek, geliştiriciler dosyayı bulut depolama alanına kaydetmeden doğrudan ikili CSV akışı alırlar. Bu API, veri çıkarma işlemlerini otomatikleştirmek, elektronik tablo verilerini alt sistemlere entegre etmek ve depolama maliyetlerini azaltmak için idealdir.

## Çalışma Sayfasını CSV'ye Dönüştür API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### İstek Parametreleri

| Parametre Adı   | Tür    | Konum     | Gerekli / Opsiyonel | Açıklama                                                                                                                                     |
| :-------------- | :----- | :-------- | :----------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | Dosya  | FormData  | **Gerekli**        | Kaynak elektronik tablonun ikili dosyası (örneğin `.xlsx`, `.xls`). Örnek: `myWorkbook.xlsx`.                                                |
| worksheet       | String | Query     | **Gerekli**        | Dönüştürülecek çalışma sayfasının adı (büyük/küçük harfe duyarlıdır). Atlanırsa ilk çalışma sayfası kullanılır. Örnek: `Sheet1`.               |
| outPath         | String | Query     | Opsiyonel          | Oluşturulan CSV'nin kaydedileceği bulut depolama alanındaki hedef klasör yolu. Atlanırsa, CSV doğrudan yanıt akışında döndürülür.              |
| outStorageName  | String | Query     | Opsiyonel          | Çıktı dosyasının yerleştirileceği depolama hizmetinin adı (örneğin Azure, AWS S3). Yalnızca `outPath` kullanıldığında gerekli.                 |
| fontsLocation   | String | Query     | Opsiyonel          | Sunucudaki özel yazı tipi klasörünün yolu; dönüşüm motorunun standart olmayan yazı tiplerini kullanmasına izin verir.                          |
| region          | String | Query     | Opsiyonel          | CSV'de sayı/tarih formatlamasını etkileyen yerel kimliği (örneğin `tr-TR`, `en-US`, `fr-FR`).                                                 |
| password        | String | Query     | Opsiyonel          | Korumalı bir elektronik tabloyu açmak için şifre. Kaynak dosyanın şifreleme şifresiyle eşleşmelidir.                                          |

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

| Kod | Anlam                  | Açıklama                                                     |
| --- | ---------------------- | ------------------------------------------------------------ |
| 200 | Tamam                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek         | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Yetkisiz               | Geçersiz veya eksik JWT belirteci.                           |
| 413 | Yük Çok Büyük          | Yüklenen dosya boyut sınırını aşıyor.                        |
| 500 | İç Sunucu Hatası       | Beklenmeyen sunucu hatası.                                   |

## Çalışma Sayfasını CSV'ye Dönüştür API Ne Zaman Kullanılmalı?

- **BI hattı için Veri Çıkarma** – Excel raporundan belirli bir çalışma sayfasını çekip sonuç CSV’yi ara dosya işlemesine gerek kalmadan doğrudan Power BI veya Tableau’ya besleyin.
- **Otomatik Fatura İşleme** – Fatura satırlarını içeren çalışma sayfasını hızla muhasebe sistemlerine içe aktarmak için CSV’ye dönüştürün.
- **Eski Sistem Entegrasyonu** – Yalnızca sınırlayıcı metin dosyalarını kabul eden eski uygulamalar için çalışma sayfası verilerini CSV olarak dışa aktarın.
- **Anlık Raporlama** – Canlı elektronik tablo verilerinin CSV anlık görüntülerini bir web servisi içinde oluşturun ve dosyayı istemci tarayıcısına anında döndürün.

## Çalışma Sayfasını CSV'ye Dönüştür API Neden Kullanılmalı?

- **Kalıcı bulut depolama gerekmez** – Dosya doğrudan dönüşüm motoruna akışlanır ve dönüşümden sonra silinir; bant genişliği ve depolama maliyetlerini azaltır.
- **Yüksek Performanslı Bulut Çalıştırma** – Dönüşüm, Aspose’un optimize edilmiş sunucularında çalışır ve genellikle 100 MB’a kadar olan dosyalar için 2 saniye içinde tamamlanır.
- **İnce Ayarlı Kontrol** – Tek bir istekte tek bir çalışma sayfasını seçin, özel yazı tipleri, bölgesel formatlama ve şifre korumasını uygulayın.
- **Tutarlı Çapraz Platform Çıktısı** – Aynı REST endpoint’ini kullanan .NET, Java, Python ve diğer SDK’lar arasında aynı CSV çıktısını garantiler.

## SDK’lar ile Çalışma Sayfasını CSV'ye Dönüştür API Nasıl Kullanılır?

### Çalışma Sayfasını CSV'ye Dönüştür API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToCsv" target="_blank" rel="noopener noreferrer">Çalışma Sayfasını CSV'ye Dönüştür API Spesifikasyonu</a>, REST etkileşimlerini doğrudan bir web tarayıcısından çalıştırmak için herkese açık bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/image?format=png&worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.png
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 kodlanmış)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviye detayları soyutlayarak gelişmeyi basitleştirir ve bir elektronik tabloyu başka bir elektronik tabloya birleştirmenizi kolay kodla yapmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetleriyle nasıl etkileşim kurulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToCsv.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToCsv.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToCsv.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToCsv.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToCsv.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToCsv.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToCsv.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToCsv.go" >}}  
{{</tab>}}  
{{< /tabs >}}