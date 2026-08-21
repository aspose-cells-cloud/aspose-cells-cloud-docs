---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Çalışma Sayfasını PDF'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, Çalışma Sayfasını PDF'ye Dönüştür, API"
description: "Aspose.Cells Cloud kullanarak bir elektronik tablo dosyasının çalışma sayfasını PDF dosyasına dönüştürür."
weight: 10
---

## Aspose.Cells Cloud Web Servislerinin ConvertWorksheetToPdf Yöntemi

Bu yöntem, yerel dosya sisteminden bir elektronik tablo dosyasını okur, çalışma sayfasını bir PDF dosyasına dönüştürür ve dönüştürülen sonucu döndürür. Kaynak dosya yolu ve hedef format doğru şekilde belirtilmelidir. Kaynak dosyayı okumak ve gerekli durumlarda dönüştürülen dosyayı yazmak için gerekli izinlerin mevcut olduğundan emin olun. Dönüştürme işlemi tamamen bulut sunucusunda gerçekleşir; bu da herhangi bir bulut depolama veya dış indirmeye gerek kalmaz.

Önemli özellikler arasında bulut-aşın dönüştürme, bulut kaynak yükünün azaltılması ve basitleştirilmiş iş akışı yer alır.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                                            |
|------------------|---------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin.                                                                                                |
| worksheet        | Dize    | Sorgu                         | Elektronik tablonun çalışma sayfası adı.                                                                                            |
| outPath          | Dize    | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır.                                                 |
| outStorageName   | Dize    | Sorgu                         | Çıktı dosyası için depo adı.                                                                                                         |
| fontsLocation    | Dize    | Sorgu                         | Özel yazı tiplerini kullanın.                                                                                                        |
| AutoRowsFit      | Boole   | Sorgu                         | (İsteğe bağlı) Tüm satırları çalışma sayfalarında otomatik olarak sığdırır.                                                          |
| AutoColumnsFit   | Boole   | Sorgu                         | (İsteğe bağlı) Tüm sütunları çalışma sayfalarında otomatik olarak sığdırır.                                                          |
| region           | Dize    | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örn. `tr-TR`, `fr-FR`). SayıBiçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password         | Dize    | Sorgu                         | Elektronik tablo dosyasını açmak için şifre.                                                                                        |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| [TBD]          |      |             |

### **Yanıt**

```json
{
  "file": "<oluşturulan PDF'in ikili akışı>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|-------|----------|
| 200 | Tamam | Çalışma sayfası başarıyla PDF'ye dönüştürüldü ve dosya akışı olarak döndürüldü. |
| 400 | Geçersiz İstek | Geçersiz istek parametreleri veya bozuk URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemiyor. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Elektronik tablo dönüştürme sırasında bir sorunla karşılaştı. |

## ConvertWorksheetToPdf SDK ile Nasıl Kullanılır

### ConvertWorksheetToPdf Spesifikasyonu

[ConvertWorksheetToPdf API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine istek nasıl atılacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Sayfa1&outPath=çıktı%2Fklasör&outStorageName=MyStorage&fontsLocation=%2Fözel%2Fyazıtipleri&AutoRowsFit=true&AutoColumnsFit=true&region=tr-TR&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@örnek.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<oluşturulan PDF'in ikili akışı>"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirmeyi hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye ayrıntıları soyutlayarak projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web servislerini nasıl çağıracağınızı göstermektedir:
`[TBD]`
---