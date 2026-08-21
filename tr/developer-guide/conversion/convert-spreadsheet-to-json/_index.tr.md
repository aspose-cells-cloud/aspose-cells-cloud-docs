---
title: "Aspose.Cells Cloud Web API – Elektronik Tabloyu JSON'ye Dönüştür"
second_title: "Belge"
ArticleTitle: "Yerel Elektronik Tabloyu Aspose.Cells Cloud API Kullanarak JSON'ye Nasıl Dönüştürürüz?"
linktitle: "Elektronik Tabloyu JSON'ye Dönüştür"
type: docs
url: /tr/convert-spreadsheet-to-json/
keywords: "Aspose Cells Cloud, Elektronik Tabloyu JSON'ye Dönüştür, Excel'den JSON'ye API, Aspose.Cells Cloud API, REST API, elektronik tablo dönüştürme"
description: "Aspose.Cells Cloud API ile yerel Excel dosyalarını JSON’a dönüştürmeyi öğrenin. Entegrasyonu sorunsuz gerçekleştirmek için uç nokta, parametreler, örnek kod ve hata yönetimi içerir."
weight: 100
---

**ConvertSpreadsheetToJson** uç noktası, yerel bir sürücüde depolanan bir elektronik tabloyu tamamen Aspose.Cells Cloud sunucusunda JSON dosyasına dönüştürür. Elektronik tabloyu `multipart/form-data` olarak göndererek hizmet, indirme veya daha fazla işlem için hazır bir JSON akışı döndürür. Bu bulut tabanlı dönüştürme, dosyanın önce depoya yüklenmesini gerektirmez, depolama maliyetlerini azaltır ve analiz, raporlama veya veri değişimi amacıyla elektronik tablo verilerini JSON formatında gerektiren uygulamaların iş akışını basitleştirir.

**Ön Gereksinimler**: Aspose Cloud hesabı, geçerli bir JWT erişim belirteci ve yapılandırılmış Aspose.Cells Cloud SDK veya API anahtarına sahip olmanız gerekir.

**Arka Plan**: Elektronik tabloyu JSON’a dönüştürmek, Excel verilerini web hizmetleri, NoSQL veritabanları veya istemci tarafı JavaScript uygulamalarıyla entegre ederken yaygın bir adımdır. Elektronik Tabloyu JSON'ye Dönüştür API’si, orijinal dosyayı depolamadan hızlı bir şekilde sunucu tarafında dönüştürme sağlar.

## Elektronik Tabloyu JSON'ye Dönüştür API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/spreadsheet/json
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür                        | Konum     | Gerekli/İsteğe Bağlı | Açıklama                                                                                                                                                                     |
| :------------- | :------------------------- | :-------- | :------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | Dosya (multipart/form-data) | FormData  | Gerekli             | Kaynak elektronik tablo dosyası (örn. .xls, .xlsx, .xlsm). Örnek: `curl -F "Spreadsheet=@myfile.xlsx"`                                                                        |
| outPath        | Dize                       | Sorgu     | İsteğe Bağlı        | Dönüştürülmüş JSON dosyasının kaydedileceği bulut depolama alanındaki hedef klasör yolu. Atlanırsa, JSON doğrudan yanıt akışında döndürülür. Örnek: `outPath=/output/`.          |
| outStorageName | Dize                       | Sorgu     | İsteğe Bağlı        | Çıktı dosyasının yazılacağı bulut depolama adı (örn. Amazon S3, Azure Blob). Yalnızca `outPath` varsayılan olmayan bir depolama ile kullanıldığında gerekli.                 |
| fontsLocation  | Dize                       | Sorgu     | İsteğe Bağlı        | Sunucudaki özel yazı tipi klasörüne yol. Elektronik tablo, varsayılan kütüphanede bulunmayan yazı tiplerini başvuruyorsa bunu kullanın.                                        |
| region         | Dize                       | Sorgu     | İsteğe Bağlı        | Elektronik tablonun bölge/dil ayarı (örn. `en-US`, `fr-FR`). Dönüştürme sırasında sayı, tarih ve para birimi formatlamasını etkiler.                                           |
| password       | Dize                       | Sorgu     | İsteğe Bağlı        | Şifre korumalı bir elektronik tabloyu açmak için şifre. Şifresiz dosyalar için atlayın.                                                                                       |

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

| Kod | Anlamı                | Açıklama                                                         |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir.  |
| 400  | Hatalı İstek          | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                               |
| 413  | Yük Çok Büyük         | Yüklenecek dosya boyut sınırını aşıyor.                          |
| 500  | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                       |

## Elektronik Tabloyu JSON'ye Dönüştür API’si nerede kullanılmalı?

- **Veri taşıma hattı** – Eski Excel raporlarını JSON’a dönüştürerek modern NoSQL veritabanlarına veya veri göllarına entegrasyonu sağlayın.
- **Mobil veya web uygulamaları** – Kullanıcıların yüklediği elektronik tabloları, orijinal dosyayı bulutta depolamadan hızlıca JSON’a dönüştürün ve istemci tarafında işleyin.
- **Otomatik raporlama** – Aşağı akış analiz hizmetleri (örn. Power BI, Tableau) için JSON yüklerini doğrudan elektronik tablo girdilerinden oluşturun.
- **Sunucusuz işlevler** – Geçici depolama yönetimi olmadan AWS Lambda veya Azure Functions içinde API’yi kullanarak anlık dönüştürme yapın.

## Elektronik Tabloyu JSON'ye Dönüştür API’si neden kullanılmalı?

- Bulut tabanlı dönüştürme, büyük dosyaların işlem öncesinde depoya yüklenmesini ortadan kaldırır; gecikmeyi ve depolama maliyetlerini azaltır.
- Tek istekli iş akışı: Elektronik tabloyu yükleyin ve aynı HTTP çağrısı içinde JSON’u alın; entegrasyon mantığını basitleştirir.
- Şifre korumalı ve bölgeye özel elektronik tabloları destekler; yerel ayarlara doğru veri temsili sağlar.
- Aspose’un altyapısında ölçeklenebilir; kendi sunucu kaynaklarınızı etkilemeden büyük çalışma kitaplarını ve karmaşık formülleri işler.

## Elektronik Tabloyu JSON'ye Dönüştür API’sini SDK’larla Nasıl Kullanırız?

### Elektronik Tabloyu JSON'ye Dönüştür API Spesifikasyonu

[Elektronik Tabloyu JSON'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertSpreadsheetToJson), web tarayıcısından doğrudan REST etkileşimleri gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek yapmayı göstermektedir.

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

SDK kullanmak, düşük seviye detayları gizleyip elektronik tabloyu birkaç satır kodla JSON’a dönüştürmenizi sağlayan en hızlı gelişim yöntemidir.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.  
Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetleriyle nasıl etkileşime gireceğinizi göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v40_ConvertSpreadsheetToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v40_ConvertSpreadsheetToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v40_ConvertSpreadsheetToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v40_ConvertSpreadsheetToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v40_ConvertSpreadsheetToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v40_ConvertSpreadsheetToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v40_ConvertSpreadsheetToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v40_ConvertSpreadsheetToJson.go" >}}
{{</tab>}}
{{< /tabs >}}