---
title: "Tabloyu Dışa Aktar – Aspose.Cells Cloud API | Excel’i PDF, PNG, CSV’ye Dönüştür"
second_title: "Belge"
ArticleTitle: "Uzak Bir Elektronik Tablo Tablosunu Başka Bir Formata Dışa Aktarma: Adım Adım Kılavuz"
linktype: "Tabloyu Belirli Bir Formata Dışa Aktar"
type: docs
url: /export-table-as-format/
keywords: "Aspose.Cells, Tabloyu Dışa Aktar, Excel’den PDF’ye, Bulut API’si, REST"
description: "Aspose.Cells Cloud API kullanarak uzak bir Excel tablosunu PDF, PNG, CSV, JSON veya diğer formatlara dışa aktarın. JWT kimlik doğrulamalı güvenli HTTPS uç noktası ve SDK örnekleri."
weight: 100
---

Bulutta saklanan bir elektronik tablo (Excel) tablosunu başka bir format dosyasına dönüştürün.

## **Tabloyu Formata Dışa Aktar API’si**

### Web API’si

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/tables/{tableName}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

```bash
-H "Authorization: Bearer {access_token}"
```

### **İstek Parametreleri:**

| Parametre Adı   | Tür     | Yol/Sorgu Dizisi/HTTPBody | Açıklama                                                                                                                                            |
| :-------------- | :------ | :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| name            | String  | Yol                       | **Gerekli.** Alınacak çalışma kitapğı dosyasının adı.                                                                                               |
| worksheet       | String  | Yol                       | Çalışma sayfasının adı.                                                                                                                             |
| tableName       | String  | Yol                       | Tablonun adı.                                                                                                                                       |
| format          | String  | Sorgu                     | **Gerekli.** İstenen çıktı formatı (örn. “png”, “pdf”, “svg”).                                                                                     |
| folder          | String  | Sorgu                     | İsteğe bağlı. Çalışma kitabının saklandığı klasör yolu. Varsayılan `null`’dır.                                                                     |
| storageName     | String  | Sorgu                     | İsteğe bağlı. Özel bulut depolama kullanılıyorsa depolama adı. Atlanırsa varsayılan depolama kullanılır.                                           |
| outPath         | String  | Sorgu                     | İsteğe bağlı. Çıktı depolama için klasör yolu. Varsayılan `null`’dır.                                                                              |
| outStorageName  | String  | Sorgu                     | İsteğe bağlı. Çıktı dosyasının depolandığı depolama adı.                                                                                            |
| fontsLocation   | String  | Sorgu                     | İsteğe bağlı. Özel yazı tiplerinin bulunduğu konum.                                                                                                 |
| region          | String  | Sorgu                     | İsteğe bağlı. Elektronik tablonun bölge/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özel davranışları etkiler. |
| password        | String  | Sorgu                     | İsteğe bağlı. Elektronik tablo dosyasını açmak için parola.                                                                                         |

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

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Hatalı İstek          | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü).|
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                        |

## **Tabloyu Başka Bir Formata Dışa Aktar API’si Nerede Kullanılmalı?**

- **Eski Sistem Geçişi**: Modern sistemler için binlerce eski XLS dosyasını XLSX’e dönüştürün.
- **Arşiv Standardizasyonu**: Arşivleme amacıyla çeşitli elektronik tablo formatlarını (XLS, XLSM, ODS, CSV) tek bir formata dönüştürün.
- **Ofis Uygulamaları Arası Uyumluluk**: Excel dosyalarını LibreOffice, Google Sheets veya Apple Numbers ile uyumlu formatlara dönüştürün.
- **Veri Kaynağı Standardizasyonu**: Veritabanı için elektronik tablo verilerini CSV veya JSON formatına dönüştürün.
- **Web Yayınlama**: Finansal modelleri web gösterimi için HTML’e dönüştürün.

## **Tabloyu Başka Bir Formata Dışa Aktar API’si Neden Kullanılmalı?**

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı dokümantasyonla birlikte gelir. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında, geliştirme iş yükünü önemli ölçüde azaltır.
- **Düşük İş Gücü Maliyeti**: Belge birleştirme için personel ayırmaya olan ihtiyacı azaltır.
- **Kullanım Ücretli**: Ön ödeme gerektirmez; sadece kullanılan API çağrıları için ödeme yaparsınız.
- **Sıfır Bakım Maliyeti**: Sunucu bakımı yapmaya, yazılım güncellemeleri yapmaya veya uyumluluk sorunlarıyla uğraşmaya gerek yoktur.
- **API, çalışma kitabının stilini içermeyen yalnızca ham tablo verilerini döndürür.**

## **Elektronik Tablo Tablosunu Format Olarak Dışa Aktar API’si SDK’larla Nasıl Kullanılır?**

### Tabloyu Formata Dışa Aktar API’si Özellikleri

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportTableAsFormat" target="_blank" rel="noopener noreferrer">Tabloyu Formata Dışa Aktar API’si Özellikleri</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/tables/Table1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64 kodlu)",
  "contentType": "MIME türü",
  "fileDownloadName": "isteğe bağlı dosya adı"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye detayları soyutlayarak elektronik tablo tablosunu format dosyasına dönüştürmek için kısa kodla hızlı geliştirme yapmanın en hızlı yoludur. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportTableAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportTableAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportTableAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportTableAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportTableAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportTableAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportTableAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportTableAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}