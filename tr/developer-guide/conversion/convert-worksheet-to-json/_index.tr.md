---
title: "Aspose.Cells Cloud Web API – Çalışma Sayfasını JSON'a Dönüştürme"
second_title: "Doküman"
ArticleTitle: "Aspose.Cells Cloud API ile Bir Hesaplama Tablosu Çalışma Sayfasını JSON'a Nasıl Dönüştürülür"
linktitle: "Çalışma Sayfasını JSON'a Dönüştür"
type: docs
url: /convert-worksheet-to-json/
keywords: "Aspose.Cells, çalışma sayfası JSON'a, Excel dönüştürme, bulut API, API v4, veri dışa aktarma"
description: "Aspose.Cells Cloud API ile bir Excel çalışma sayfasını JSON'a dönüştürme adımlı kılavuzu; istek parametreleri, yanıt işleme, hata kodları ve SDK örnekleri içerir."
weight: 100
---

**ConvertWorksheetToJson** uç noktası, yerel dosya sisteminden bir hesaplama tablosu dosyasını okur, belirtilen çalışma sayfasını çıkarır ve içeriğini bir JSON dosyası olarak döndürür. Dönüştürme, tamamen Aspose.Cells Cloud sunucularında gerçekleştirilir; bu nedenle ara yükleme veya depolama gerekmez. Şifreli çalışma kitaplarını, özel yazı tipi konumlarını ve bölgesel ayarları destekler ve aşağı akış işlemek amacıyla çalışma sayfası verilerini JSON'a dışa aktarmak için hızlı, bulut-tabanlı bir çözüm sunar.

## **Çalışma Sayfasını JSON'a Dönüştür API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/json
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı   | Tür     | Konum      | Gerekli / Opsiyonel | Açıklama                                                                                                                                                                                      |
| :-------------- | :------ | :--------- | :------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet     | dosya   | FormData   | Gerekli             | İşlenecek Excel çalışma kitabı. Desteklenen bir formatta olmalıdır (xls, xlsx, csv vb.). multipart/form-data olarak gönderilir. Örnek: `Spreadsheet=@C:\Docs\Sample.xlsx`.                   |
| worksheet       | string  | Query      | Gerekli             | Dönüştürülecek çalışma sayfasının tam adı (büyük/küçük harfe duyarlı). Atlanırsa veya bulunamazsa API bir hata döndürür. Örnek: `worksheet=Sheet1`.                                           |
| outPath         | string  | Query      | Opsiyonel           | Oluşturulan JSON dosyasının kaydedileceği yapılandırılmış bulut depolama alanındaki hedef klasör. Belirtilmezse JSON doğrudan yanıt akışında döndürülür. Örnek: `outPath=/converted/`.         |
| outStorageName  | string  | Query      | Opsiyonel           | `outPath` içeren hedef depolamanın adı (örneğin "MyStorage"). Atlandığında varsayılan depo kullanılır.                                                                                      |
| fontsLocation   | string  | Query      | Opsiyonel           | Çalışma sayfasındaki metnin doğru şekilde işlenmesi için gerekli özel yazı tiplerini içeren sunucu tarafı klasör. Örnek: `fontsLocation=/fonts/custom/`.                                  |
| region          | string  | Query      | Opsiyonel           | Oluşturulan JSON'da sayı, tarih ve para birimi formatlamasını etkileyen kültürel/bölgesel tanımlayıcı (örneğin `en-US`, `fr-FR`).                                                             |
| password        | string  | Query      | Opsiyonel           | Şifrelenmiş bir çalışma kitabını açmak için kullanılan şifre. Çalışma kitabı şifre korumalı değilse bu parametre atlanır.                                                                     |

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

| Kod | Anlamı                | Açıklama                                                       |
| --- | --------------------- | -------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek          | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                             |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut limitini aşıyor.                          |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                     |

## Çalışma Sayfasını JSON'a Dönüştür API'si nerede kullanılmalı?

- **Web panoları** – Çalışma sayfası verilerini istemci tarafı grafik kütüphaneleri (örneğin Chart.js, D3.js) için JSON'a dışa aktarın.
- **Veri taşıma** – Eski Excel verilerini JSON alanını tüketen NoSQL veritabanlarına veya REST servislerine taşıyın.
- **Mobil veya çevrimdışı uygulamalar** – Sunucu tarafında çalışma sayfası içeriğini JSON'a dönüştürün ve hafif yükü mobil cihazlara senkronize edin.
- **Raporlama süreçleri** – Çalışma sayfası verilerini doğrudan JSON girdisi alan analitik motorlara besleyin, ara adımda CSV kullanmadan.

## Neden Çalışma Sayfasını JSON'a Dönüştür API'sini kullanmalısınız?

- **Yüklemeye gerek yok** – Önce depolama alanına yüklemek yerine yerel dosyaları bulutta işleyin; bant genişliği ve depolama maliyetlerinden tasarruf sağlayın.
- **Tam özellikli dönüştürme** – Doğru veri temsili için şifreli çalışma kitaplarını, özel yazı tiplerini ve bölgesel formatlamayı destekler.
- **Hızlı ve ölçeklenebilir çalıştırma** – Bulut altyapısında yüksek performanslı Aspose.Cells motorunu kullanır; büyük çalışma sayfalarını verimli şekilde işler.
- **Basit entegrasyon** – Tek bir PUT çağrısı, hemen kullanıma hazır bir JSON dosyası döndürür veya doğrudan depolar; istemci uygulamalarındaki kod karmaşıklığını azaltır.

## SDK'lar ile Çalışma Sayfasını JSON'a Dönüştür API'sini Nasıl Kullanılır

### Çalışma Sayfasını JSON'a Dönüştür API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToJson" rel="noopener noreferrer">Çalışma Sayfasını JSON'a Dönüştür API Spesifikasyonu</a>, web tarayıcısından doğrudan REST etkileşimlerini gerçekleştirmek için erişilebilir bir programlama arayüzü sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye nasıl istek atılacağını göstermektedir.

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
  "fileDownloadName": "opsiyonel dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak ve hesaplama tablosuyla kısa ve net kod kullanarak çalışmanıza izin vererek hızlı geliştime sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.  
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web servisleriyle nasıl etkileşim kurulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertWorksheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertWorksheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertWorksheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertWorksheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertWorksheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertWorksheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertWorksheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertWorksheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}