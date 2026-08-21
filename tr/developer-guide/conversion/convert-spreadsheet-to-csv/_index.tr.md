---
title: "Aspose.Cells Cloud Web API – Elektronik Tabloyu CSV'ye Dönüştürme"
second_title: "Belge"
ArticleTitle: "Aspose.Cells Cloud API Kullanılarak Elektronik Tablonun CSV'ye Dönüştürülmesi"
linktitle: "Elektronik Tabloyu CSV'ye Dönüştür"
type: docs
url: /tr/convert-spreadsheet-to-csv/
keywords: "Aspose Cells, CSV dönüştürme, Excel API, bulut tabanlı dönüştürme"
description: "Aspose.Cells Cloud API kullanarak Excel dosyalarını (XLS, XLSX, XLSM vb.) CSV formatına nasıl dönüştüreceğinizi öğrenin. Kimlik doğrulama adımlarını, cURL örneğini, SDK kod parçacıklarını ve hata işleme yöntemlerini içerir."
weight: 100
---

**ConvertSpreadsheetToCsv** uç noktası, yerel bir sürücüden yüklenen bir elektronik tablo dosyasını okur, dönüşümü tamamen Aspose.Cells Cloud sunucularında işler ve sonuç CSV dosyasını ikili akış olarak döndürür. Bu bulut tabanlı işlem, kaynak dosyanın bulut depolama alanına yüklenmesini gerektirmez, depolama maliyetlerini azaltır ve hızlı elektronik tablo‑to‑CSV dönüşümü gerektiren geliştiricilerin iş akışını basitleştirir. Desteklenen formatlar temel kütüphanelere bağlıdır ve kaynak dosyayı okumak için uygun izinler gereklidir. Eksik dosyalar, geçersiz istekler veya dönüşüm hataları gibi hatalar standart HTTP durum kodlarıyla döndürülür.

## **Elektronik Tabloyu CSV'ye Dönüştür API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı  | Tür     | Konum      | Gereklilik | Açıklama                                                                                                                                                         |
| :------------- | :------ | :--------- | :--------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya   | FormData   | Gerekli    | Dönüştürülecek elektronik tablo dosyası. .xls, .xlsx, .xlsm gibi yaygın formatları destekler. multipart/form‑data olarak sağlanmalıdır. Örnek: `myWorkbook.xlsx`. |
| outPath        | Dize    | Sorgu      | İsteğe Bağlı | Dönüştürülmüş CSV’nin kaydedileceği hedef klasör yolu. Belirtilmezse CSV doğrudan yanıt gövdesinde döndürülür. Örnek: `/output/reports/`.                          |
| outStorageName | Dize    | Sorgu      | İsteğe Bağlı | Çıktı dosyasının kaydedileceği bulut depolama hizmetinin adı. Belirtilmezse, Aspose.Cells hesabına yapılandırılmış varsayılan depolama kullanılır.               |
| fontsLocation  | Dize    | Sorgu      | İsteğe Bağlı | Elektronik tablo tarafından gereken özel yazı tiplerini içeren klasörün yolu.standart olmayan yazı tiplerini kullanan hücrelerin doğru şekilde gösterilmesini sağlar. |
| region         | Dize    | Sorgu      | İsteğe Bağlı | Elektronik tablonun bölge/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı formatlama, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler.                |
| password       | Dize    | Sorgu      | İsteğe Bağlı | Şifreli elektronik tabloları açmak için kullanılan şifre. Dosya şifreliyse ve şifre eksik veya yanlışsa 400/401 hatası döndürülür.                                |

### **Yanıt**

Başarılı durumda API, `Content-Type: application/octet-stream` başlığıyla **HTTP 200** (veya asenkron işlem için **202**) döndürür. Yanıt gövdesi, oluşturulan CSV dosyasını ikili akış olarak içerir.

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

| Kod | Anlamı                 | Açıklama                                                           |
| --- | ---------------------- | ------------------------------------------------------------------ |
| 200 | Tamam                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.     |
| 400 | Geçersiz İstek         | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Yetkisiz               | Geçersiz veya eksik JWT belirteci.                                 |
| 413 | Yük Çok Büyük          | Yüklenen dosya boyut sınırını aşıyor.                              |
| 500 | Sunucu İç Hatası       | Beklenmeyen sunucu hatası.                                         |

## Elektronik Tabloyu CSV'ye Dönüştür API Nerede Kullanılmalı?

- **Raporlama Sistemleri İçin Veri Dışa Aktarma** – Elektronik tabloya dayalı raporlardan CSV dışa aktarmaları oluşturun; böylece BI araçlarına veya veri ambarlarına manuel dosya işlemesi olmadan aktarabilirsiniz.
- **Otomatik Toplu İşlem** – Yerel olarak depolanan büyük sayıdaki elektronik tabloyu sunucu tarafında bir işte CSV'ye dönüştürün, ardından sonuçları doğrudan aşağı akış hizmetlerine akış olarak gönderin.
- **Dosya Yükleme İçeren Web Uygulamaları** – Son kullanıcıların Excel dosyası yüklemesine izin verin ve daha fazla analiz veya diğer platformlara içe aktarma amacıyla anında CSV sürümünü alın.
- **Eski Sistem Entegrasyonu** – Yalnızca düz metin sınırlayıcı dosyaları kabul eden sistemler için eski elektronik tablo formatlarını CSV’ye dönüştürün.

## Elektronik Tabloyu CSV'ye Dönüştür API Neden Kullanılmalı?

- **Sıfır-Yükleme Mimarisi** – Kaynak dosyanın bulut depolama alanına yüklenmesine gerek yoktur; dönüşüm doğrudan yüklenen akıştan yapılır, bu da zaman ve depolama maliyetlerini tasarruf sağlar.
- **Yüksek Performanslı Bulut İşleme** – Ölçeklenebilir bulut sunucularında Aspose.Cells’in optimize edilmiş dönüştürme motorundan yararlanır; büyük çalışma kitapları için bile hızlı CSV çıktısı verir.
- **Basit Entegrasyon** – İsteğe bağlı sorgu parametreleriyle tek bir PUT isteği; CSV’yi hemen indirilebilir ikili akış olarak döndürür, böylece ek işlem adımlarını ortadan kaldırır.
- **Tam Özellik Desteği** – Şifreli dosyaları, özel yazı tiplerini ve yerel ayara özgü ayarları işler, böylece karmaşık elektronik tablolar için doğru dönüştürme sağlar.

## SDK’lar ile Elektronik Tabloyu CSV'ye Dönüştür API Nasıl Kullanılır?

### Elektronik Tabloyu CSV'ye Dönüştür API Spesifikasyonu

[Elektronik Tabloyu CSV'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToCsv), web tarayıcısından doğrudan REST etkileşimlerini gerçekleştirmek için genel olarak erişilebilir bir programlama arayüzü sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca ulaşabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json?outPath=/output/result.json" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@myWorkbook.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak kısa kodla elektronik tablolarla çalışmanıza izin vererek en hızlı geliştime yöntemidir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın. Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetleriyle nasıl etkileşime girileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToCsv.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToCsv.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToCsv.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToCsv.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToCsv.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToCsv.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToCsv.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToCsv.go" >}}
{{</tab>}}
{{< /tabs >}}