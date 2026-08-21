---
title: "Aspose.Cells Cloud Web API - Uzak Excel Çalışma Sayfasını Diğer Formatlara Dışa Aktarma - Ücretsiz Çevrimiçi Araç"
secondtitle: "Belge"
articletitle: "Uzak Elektronik Tablo Çalışma Sayfasını Diğer Formatlara Dışa Aktarma: Adım Adım Rehber"
linktitle: "Elektronik Tabloyu Format Olarak Dışa Aktar"
type: docs
url: /tr/export-spreadsheet-as-format/
keywords: "Aspose.Cells, elektronik tablo dönüştürme, API, dışa aktar, PDF, CSV, JSON, XLSX"
description: "Aspose Cloud’da depolanan Excel çalışma kitaplarını tek bir REST uç noktası aracılığıyla PDF, XLSX, CSV, JSON veya HTML formatına dönüştürün. İstek sözdizimini, parametreleri öğrenin ve C#, Java, Python ve daha fazlası dillerinde SDK örneklerini görün."
weight: 100
---

Bulut üzerindeki (Excel) elektronik tabloyu başka bir dosya formatına dönüştürün.

## **Elektronik Tabloyu Format Olarak Dışa Aktar API**

### Web API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı  | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                                           |
| :------------- | :----- | :-------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Yol                         | (Zorunlu) Getirilecek çalışma kitapı dosyasının adı.                                                                                              |
| format         | String | Sorgu                       | (Zorunlu) İstenen çıktı formatı (örn. “Xlsx”, “PDF”, “CSV”).                                                                                      |
| folder         | String | Sorgu                       | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null’dır.                                                              |
| storageName    | String | Sorgu                       | (İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama adı. Atlanırsa varsayılan depolama kullanılır.                                         |
| outPath        | String | Sorgu                       | (İsteğe bağlı) Çalışma kitabının depolanacağı klasör yolu. Varsayılan değer null’dır.                                                              |
| outStorageName | String | Sorgu                       | (İsteğe bağlı) Çıktı dosyasının depolandığı depolama adı.                                                                                          |
| fontsLocation  | String | Sorgu                       | (İsteğe bağlı) Özel yazı tipi konumu.                                                                                                              |
| region         | String | Sorgu                       | (İsteğe bağlı) Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı formatlamayı, tarih çözümlemeyi ve yerel ayara özgü davranışı etkiler. |
| password       | String | Sorgu                       | (İsteğe bağlı) Elektronik tablo dosyasını açmak için kullanılan şifre.                                                                             |

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

Yanıt, dönüştürülmüş dosya akışını temsil eden tek bir nesne içerir.

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400  | Geçersiz İstek        | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413  | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                             |
| 500  | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                        |

## Elektronik Tabloyu Başka Bir Format Olarak Dışa Aktar API’sini Nerede Kullanmalısınız?

- **Eski Sistem Geçişi**: Modern sistemler için binlerce eski XLS dosyasını XLSX’e dönüştürün.
- **Arşiv Standartlaştırma**: Farklı elektronik tablo formatlarını (XLS, XLSM, ODS, CSV) arşivleme amacıyla tek bir formata dönüştürün.
- **Ofis Uygulama Uyumluluğu**: Excel dosyalarını LibreOffice, Google Sheets veya Apple Numbers ile uyumlu formatlara dönüştürün.
- **Veri Kaynağı Standardizasyonu**: Farklı elektronik tablo formatlarını veritabanı içine almak için CSV veya JSON’a dönüştürün.
- **Web Yayınlama**: Finansal modelleri web gösterimi için HTML formatına dönüştürün.

## Elektronik Tabloyu Başka Bir Format Olarak Dışa Aktar API’sini Neden Kullanmalısınız?

- **Geliştirici Dostu**: Aspose.Cells Cloud, birden fazla dilde SDK kütüphaneleri sunar ve hızlı geliştirme sağlar; ayrıca kapsamlı dokümantasyonla birlikte gelir. Özel grafik oluşturma çözümleri oluşturmakla karşılaştırıldığında geliştirme iş yükünü önemli ölçüde azaltır.
- **Düşük İşgücü Maliyeti**: Belge birleştirme işi için ayrılmış personel gereksinimini azaltır.
- **Kullanım Üzerine Ödeme**: Ön ödemeye gerek yoktur; yalnızca gerçekten kullanılan API çağrıları için ödeme yaparsınız.
- **Sunucu tarafında bakım gerekmez**: Sunucuları bakım yapmaya, yazılımları güncellemeye veya uyumluluk sorunlarıyla uğraşmaya gerek yoktur.
- **Kapsamlı Format Desteği**: 20’dan fazla elektronik tablo formatı arasında dönüştürme yapın.
- **Veri Sadakati ve Biçimlendirmeyi Koruma**: Dönüştürme sırasında orijinal düzeni, formülleri ve stilleri korur.

## Elektronik Tabloyu Format Olarak Dışa Aktar API’sini SDK’larla Nasıl Kullanılır?

### Elektronik Tabloyu Format Olarak Dışa Aktar API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">Elektronik Tabloyu Format Olarak Dışa Aktar API Spesifikasyonu</a>, REST etkileşimlerini sorunsuz bir şekilde gerçekleştirmek için herkese açık bir programlama arayüzü sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, düşük seviye ayrıntıları soyutlayarak elektronik tabloyu bir format dosyasına kısa kodla dışa aktarmanıza olanak tanıyan en hızlı geliştirme yoludur.  
API’yi çağırmadan önce bir OAuth 2.0 erişim belirteci edinin ve `Authorization: Bearer <token>` başlığına ekleyin.

Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetleriyle çeşitli SDK’lar aracılığıyla nasıl etkileşime geçileceğini göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}