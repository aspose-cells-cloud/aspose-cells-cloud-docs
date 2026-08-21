---
title: "Aspose.Cells Cloud Add Text API – Birden Fazla Excel Hücresine Aynı Anda Metin Ekleme – Önek, Sonek ve Etiketler Ekleme"
secondtitle: "Belge"
ArticleTitle: "Excel için Toplu Metin Ekleme – Önek, Sonek ve Özel Metinleri Hücrelere Ekleme – Adım Adım Rehber"
linktype: "AddText"
type: docs
url: /add-text/
keywords: "Aspose Cells API, Excel metin ekleme, toplu metin ekleme, Excel önek sonek, spreadsheet metin değiştirme, Excel otomasyonu, bulut spreadsheet API"
description: "Aspose.Cells Cloud ile önekler, sonekler veya özel etiketleri tek bir çağrıda birçok Excel hücresine ekleyin. Başlangıç, bitiş veya herhangi bir metinden önce/sonra seçeneğini kullanın. Aralık, çalışma sayfası ve boş hücre işleme desteğini sağlar."
weight: 100
---

Birden fazla Excel hücresine tek bir işlemde metin ekleyin. Aspose.Cells API kullanarak hücrelerin başlangıcına, sonuna veya içindeki belirli bir metinden önce/sonra önekler, sonekler, etiketler veya özel karakterler ekleyin.

## Genel Bakış

Hedef aralıktaki her hücreye tek bir çağrıyla önek, sonek veya sabitlenmiş dizeleri ekleyin—formül veya yardımcı sütun gerekmez.

- Her hücre içinde **herhangi bir konumda** özel metin ekleme

| Değer              | Açıklama                                                                          |
| ------------------ | --------------------------------------------------------------------------------- |
| `None`             | Orijinal içeriği değiştir                                                         |
| `AtTheBeginning`   | Başlangıca ekle (ön ek)                                                            |
| `AtTheEnd`         | Sonuna ekle (son ek)                                                              |
| `BeforeText`       | `selectText`’in **ilk** oluşumundan **önce** ekle; bulunamazsa atla              |
| `AfterText`        | `selectText`’in **ilk** oluşumundan **sonra** ekle; bulunamazsa atla             |

- Dört konum modu: önek, sonek, alt metinden önce/sonra.
- Gereksiz doluluğu önlemek için boş hücreleri atla.
- API yalnızca **metin türü** değerleriyle çalışır; sayılar, boolean’lar ve formüller önce metne dönüştürülür.
- **Boş hücreler**
  - `skipEmptyCells = true` → boş hücreler atlanır.
  - `skipEmptyCells = false` → boş hücrelere metin eklenir (hücre metin türü olur).

- **Bağlayıcı metin bulunamadı**: `position = BeforeText | AfterText` ve `selectText` **yoksa**, hücre değeri değişmeden kalır.

### **Web API**

```http
PUT https://api.aspose.cloud/v4.0/cells/content/add/text
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **AddText** API’sinin istek parametreleri şunlardır:

| Parametre Adı   | Tür      | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                                                                                                                                   | Gerekli |
| :-------------- | :------- | :--------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------- | :------ |
| Spreadsheet     | Dosya    | FormData                     | İşlenecek spreadsheet dosyası. Desteklenen formatlar: XLSX, XLS, ODS, CSV vb.                                                                            | Evet    |
| text            | Dize     | Sorgu                        | Spreadsheet’te belirtilen hücrelere eklenecek metin içeriği.                                                                                              | Evet    |
| position        | Dize     | Sorgu                        | Mevcut hücre içeriğine göre metnin nereye ekleneceğini belirtir. Seçenekler: `AtTheBeginning`, `AtTheEnd`, `BeforeText`, `AfterText`, `None`.           | Evet    |
| selectText      | Dize     | Sorgu                        | _(İsteğe bağlı)_ Sağlanırsa, metin yalnızca bu tam alt dizesini içeren hücrelere eklenir. `position` parametresiyle birlikte kullanılır.                 | Hayır   |
| skipEmptyCells  | Boolean  | Sorgu                        | `true` ise boş hücreler atlanır; `false` ise boş hücrelere metin eklenir.                                                                                 | Hayır   |
| worksheet       | Dize     | Sorgu                        | _(İsteğe bağlı)_ Metin eklenecek çalışma sayfasının adı. Atlanırsa, işlem varsayılan olarak ilk çalışma sayfasına uygulanır.                               | Hayır   |
| range           | Dize     | Sorgu                        | _(İsteğe bağlı)_ Metin eklenecek hücre aralığı (örn. `"A1:C10"`). Atlanırsa, işlem belirtilen çalışma sayfasındaki tüm kullanılan hücrelere uygulanır.     | Hayır   |
| outPath         | Dize     | Sorgu                        | _(İsteğe bağlı)_ İşlenmiş defterin kaydedileceği bulut depolama klasör yolu. Atlanırsa, dosya kaynak klasörde kaydedilir.                                 | Hayır   |
| outStorageName  | Dize     | Sorgu                        | Çıktı dosyasının saklanacağı bulut depolamanın adı.                                                                                                        | Hayır   |
| region          | Dize     | Sorgu                        | _(İsteğe bağlı)_ Çıktı dosyasında sayıları, tarihleri ve parabirimlerini Biçimlendirmek için yerel ayar (örn. `"en-US"`, `"zh-CN"`, `"de-DE"`).              | Hayır   |
| password        | Dize     | Sorgu                        | _(İsteğe bağlı)_ Yüklenen spreadsheet şifreliyse, dosyayı açmak ve işlemek için şifreyi sağlayın.                                                          | Hayır   |

**cURL Örneği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/content/add/text?text=Rapor&position=AtTheBeginning&skipEmptyCells=true" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/workbook.xlsx" \
  -F "outPath=output/workbook_modified.xlsx"
```

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

### Hata Kodları

| Kod | Açıklama |
|-----|----------|
| **400** Bad Request | Geçersiz Aspose.Cells Cloud API URI’si veya eksik gerekli parametreler. |
| **401** Unauthorized | Geçersiz erişim belirteci veya geçersiz istemci kimliği ve gizli anahtarı. |
| **404** Not Found | Spreadsheet dosyasına erişilemiyor. |
| **500** Server Error | Spreadsheet, hesaplama verilerini alırken bir anomaliyle karşılaştı. |

## Add Text for Spreadsheet API’i nerede kullanmalıyız?

- **Dinamik Rapor Etiketleme**: Otomatik olarak oluşturulan finansal raporlar ve satış raporlarına dinamik başlıklar, tarih etiketleri veya notlar ekleyin.
- **Toplu Dosya Filigranlama**: Excel dosyalarının bir kümesine şirket logoları, gizlilik filigranları veya sürüm bilgileri ekleyin.
- **Şablon Veri Doldurma**: Sözleşme veya fatura şablonlarında önceden tanımlanmış konumlara müşteri adlarını, tutarları ve diğer metinleri otomatik doldurun.
- **Veri Sınıflandırma Etiketleme**: Analiz sonuçlarına dayanarak veri satırlarına sınıflandırma etiketleri veya durum etiketleri (örn. “İnceleniyor”, “Onaylandı”) ekleyin.
- **Veri Kalitesi Açıklaması**: Veri temizleme sırasında sorunlu veriler için notlar ekleyin.
- **Toplu Metin Biçimlendirme**: Ürün adlarını veya müşteri adlarını tek bir formatta önek veya sonek ekleyerek standartlaştırın.

## Neden Add Text for Spreadsheet API’i kullanmalısınız?

- **Toplu Metin Ekleme**: Elle çalışmaktan %95’e kadar zaman kazandırarak, yüzlerce hücreye veya dosyaya aynı anda metin ekleyin.
- **Kesin Konum Kontrolü**: Başlangıç, bitiş veya hücre içinde belirli metinden önce/sonra gibi altı konumda metin eklemeyi destekler.
- **Akıllı Koşullu İşleme**: Boş bir hücrede veya belirli metni içeren bir hücrede metin ekleme kararını verin.
- **Çok Konumlu Strateji Desteği**:
  - `AtTheBeginning`: Tüm seçili hücrelerin içeriğinden önce aynı metni ekleyin.
  - `AtTheEnd`: Tüm seçili hücrelerin içeriğinden sonra metin ekleyin.
  - `BeforeText` / `AfterText`: Belirli metni içeren hücrelerin başına veya sonuna metin ekleyin.
  - `None`: Orijinal içeriği değiştirin.
- **Kesin Aralık Kontrolü**: İşlem için belirli çalışma sayfalarını veya hücre aralıklarını belirlemeyi sağlar.
- **Koşullu Atlama Seçeneği**: Gereksiz metin eklemesini önlemek için boş hücreleri atlamayı destekler.
- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar; hızlı geliştirme sağlar ve kapsamlı dokümantasyonla birlikte gelir. Özel grafik oluşturma çözümleri oluşturmaya göre geliştirme yükünü önemli ölçüde azaltır.
- **Maliyet Etkin**: Öncelikle defteri yüklemeye gerek kalmadan hücreye metin ekleyebilirsiniz; bu, depolama alanını tasarruf eder ve maliyetleri düşürür.

## OpenAPI Specification

[OpenAPI Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/AddText), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. SDK, altta yatan ayrıntıları yönetir, böylece hücrelere Add Text için minimum kodla uygulama yapabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddText.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddText.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddText.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddText.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddText.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddText.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddText.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddText.go" >}}
{{</tab>}}
{{< /tabs >}}
---