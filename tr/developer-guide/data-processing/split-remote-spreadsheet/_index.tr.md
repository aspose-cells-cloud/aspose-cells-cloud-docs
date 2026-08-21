---
title: "Aspose.Cells Cloud Elektronik Tablo Bölücü Web API'si - Excel Çalışma Kitabını 30'dan Fazla Formatta Çoklu Dosyalara Bölün"
second_title: "Doküman"
ArticleTitle: "Excel Dosyasını Bulutta Birden Fazla Dosyaya Ayırın ve 30'dan Fazla Formata Dışa Aktarın"
linktitle: "Buluttaki Uzak Elektronik Tabloyu Bölün"
type: docs
url: /split-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, Excel çalışma kitabını bölme, elektronik tablo bölücü, bulut API'si, PDF'e dışa aktar, CSV'ye dışa aktar, JSON'a dışa aktar, çoklu format dışa aktarımı, bulut elektronik tablo işleme"
description: "Aspose.Cells Cloud API'sini kullanarak bulut depolama alanında saklanan bir Excel çalışma kitabını ayrı çalışma sayfalarına bölün ve her birini PDF, CSV, JSON, XLSX, HTML, ODS ve XPS gibi 30'dan fazla forma dışa aktarın."
weight: 100
---

Bulutta saklanan büyük bir Excel çalışma kitabını çalışma sayfalarına göre ayrı dosyalara bölün ve her birini PDF, CSV, JSON, ODS ve XPS gibi 30'dan fazla çıktı formatına dışa aktarın.

## **Uzak Elektronik Tabloyu Bölme API'si**

### Web API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/split/spreadsheet
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı   | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                           |
| :-------------- | :------ | :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| name            | String  | Yol                         | Bölünecek çalıştırma kitaplığı dosyasının adı (örneğin, `data.xlsx`), belirtilen bulut depolama klasöründe bulunur.               |
| folder          | String  | Sorgu                       | Kaynak çalışma kitabının bulunduğu bulut depolama klasör yolu.                                                                    |
| from            | Integer | Sorgu                       | Bölme işlemi için başlangıç çalışma sayfası indeksi (0‑tabanlı). Örneğin, `0` ilk çalışma sayfasını belirtir.                      |
| to              | Integer | Sorgu                       | Bölme işlemi için bitiş çalışma sayfası indeksi (0‑tabanlı). Örneğin, `2` 0., 1. ve 2. çalışma sayfalarını böler.                 |
| outFormat       | String  | Sorgu                       | Bölünmüş dosyaların çıktı dosya formatı. Desteklenen formatlar arasında `XLSX`, `PDF`, `CSV`, `JSON`, `HTML` ve 30'dan fazlası yer alır. |
| storageName     | String  | Sorgu                       | _(İsteğe bağlı)_ Kaynak çalışma kitabının bulunduğu bulut depolamanın adı. Atlanırsa varsayılan bulut depolama kullanılır.        |
| outPath         | String  | Sorgu                       | _(İsteğe bağlı)_ Bölünmüş dosyaların kaydedileceği hedef bulut klasör yolu. Atlanırsa dosyalar kaynak klasörde kaydedilir.        |
| outStorageName  | String  | Sorgu                       | Çıktı bölünmüş dosyaların saklanacağı bulut depolamanın adı.                                                                      |
| fontsLocation   | String  | Sorgu                       | _(İsteğe bağlı)_ PDF/görüntü çıktılarında düzgün metin gösterimi için yazı tipi dosyalarını içeren özel bir bulut klasör yolu belirtir. |
| region          | String  | Sorgu                       | _(İsteğe bağlı)_ Çıktı dosyalarındaki sayıların, tarihlerin ve para birimlerinin yerel ayarını belirler (örneğin, `"en-US"`, `"zh-CN"`, `"de-DE"`). |
| password        | String  | Sorgu                       | _(İsteğe bağlı)_ Kaynak çalışma kitabısı şifreliyse, dosyayı açmak için şifreyi sağlayın.                                          |

## **Yanıt**

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

Dosya doğrudan `outPath` tarafından belirtilen konumdan indirilebilir veya oraya kaydedilebilir.

**Başarılı yanıt detayları**

| Durum Kodu | İçerik Türü                | Açıklama                                     |
| ---------- | -------------------------- | -------------------------------------------- |
| 200 OK     | `application/octet-stream` | Birleştirilmiş çalışma kitabı dosyasının ikili akışı. |

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.     |
| 400 | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)   | Geçersiz veya eksik JWT token.                                   |
| 413 | Payload Too Large (Ağır Yük) | Yüklenen dosya boyut sınırını aşıyor.                              |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                        |

## **Uzak Elektronik Tabloyu Bölme API'si nerede kullanılmalıdır?**

- **Bölüm Verisi Dağıtımı**: Birden fazla bölümden gelen verileri içeren tek bir çalışma kitabını bölümlere özel dosyalara bölün.
- **Bölgesel Rapor Dağıtımı**: Ulusal satış raporlarını bölgeye göre ayrı bölgesel rapor dosyalarına bölün.
- **Müşteri Verisi Maskeleme Dağıtımı**: Hassas bilgiler içeren bir çalışma kitabını özel bir müşteri görünüm dosyasına bölün.
- **Periyodik Rapor Bölme**: Özet raporları aylık olarak otomatik olarak haftalık veya günlük raporlara bölün.
- **Çoklu Format Dağıtımı**: Tek bir Excel dosyasını PDF, CSV, JSON vb. gibi birden fazla format sürümüne aynı anda bölün.
- **Şablon Tabanlı Bölme**: Veri dosyalarını önceden tanımlanmış şablonlara göre standartlaştırılmış çıktı dosyalarına bölün.
- **Veri Kaynağı Ön İşleme**: Veritabanına yüklenmeden önce Excel dosyasını standartlaştırılmış bir CSV dosyasına bölün.
- **API Verisi Hazırlama**: Büyük veri setlerini API aktarımı için uygun daha küçük parçalara bölün.
- **Mikroservis Verisi Dağıtımı**: Merkezi veri dosyasını her mikroservisin gerektirdiği ayrı veri dosyalarına bölün.

## **Uzak Elektronik Tabloyu Bölme API'si neden kullanılmalıdır?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunarak hızlı geliştirme yapmayı sağlar ve kapsamlı dokümantasyonla birlikte gelir. Özel grafik oluşturma çözümleri oluşturmak yerine, bu işlem geliştirme yükünü önemli ölçüde azaltır.
- **İşçilik Maliyetlerini Azaltma**: Doküman birleştirme konusunda özel görevlendirilmiş pozisyonlara olan ihtiyacı azaltır.
- **Ödeme-yap-kullan**: Ön ödeme gerektirmez; yalnızca gerçekten kullanılan API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti**: Sunucuları bakım yapmaya, yazılımları güncellemeye veya uyumluluk sorunlarıyla uğraşmaya gerek yoktur.
- **Karmaşık Excel formatlamasını evrensel olarak erişilebilir PDF formatında korur.**

## **Uzak Elektronik Tabloyu Bölme API'sini SDK'lar ile Nasıl Kullanılır?**

### Uzak Elektronik Tabloyu Bölme API Spesifikasyonu

[Uzak Elektronik Tabloyu Bölme API Spesifikasyonu](https://reference.aspose.cloud/cells/#/DataProcessingController/SplitRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek atacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Report.xlsx/split/spreadsheet?folder=Input&outFormat=PDF&from=0&to=2" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
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

### Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, düşük seviye detayları soyutlayarak bulutta saklanan elektronik tabloyu kısa kodla ayrı dosyalara bölmenizi sağlayan en hızlı geliştirme yoludur.  
Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.  
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl istek atacağınızı göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SplitFileInRemote.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SplitFileInRemote.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SplitFileInRemote.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SplitFileInRemote.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SplitFileInRemote.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SplitFileInRemote.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SplitFileInRemote.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SplitFileInRemote.go" >}}
{{</tab>}}
{{< /tabs >}}