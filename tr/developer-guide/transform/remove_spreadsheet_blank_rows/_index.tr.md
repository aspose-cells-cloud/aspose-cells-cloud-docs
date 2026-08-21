---
title: "Hesap Tablosu Boş Satırlarını Kaldırma"
ArticleTitle: "Hesap Tablosu Boş Satırlarını Kaldırma – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "Hesap Tablosu Boş Satırlarını Kaldırma"
type: docs
url: /cells/remove/blank-rows
aliases: []
keywords: "Aspose.Cells, boş satırları kaldırma, hesap tablosu, API"
description: "Bir hesap tablosu dosyasından tüm boş satırları siler."
weight: 100
---

## Aspose.Cells Cloud Web Hizmetlerinin Hesap Tablosu Boş Satırlarını Kaldırma

Bu yöntem, içinde hiçbir veri veya nesne bulunmayan tamamen boş olan satırları bir hesap tablosundan kaldırır. Tüm sayfaları tarayarak her hücrenin boş olduğu satırları belirler. İşlem doğrudan hesap tablosu üzerinde gerçekleştirilir ve yalnızca içeriği olmayan satırların silindiğinden emin olunur. Bu, hesap tablosunu temizlemeye ve gereksiz boş satırları kaldırmaya yardımcı olur; böylece veriler daha düzenli hale gelir ve yönetimi kolaylaşır. Kullanıcılar, silinen satırların geri alınamayacağından bu işlemi gerçekleştirmeden önce hesap tablosunun yedeğini almalıdır.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/blank-rows
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|---------------|-------|-------------------------------|----------|
| Spreadsheet   | Dosya | FormData                      | Hesap tablosu dosyasını yükleyin. |
| outPath       | Dize  | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null’dır. |
| outStorageName| Dize  | Sorgu                         | Çıktı dosyası için depo adı. |
| region        | Dize  | Sorgu                         | Hesap tablosu bölgesi/dil ayarı (örn. `tr-TR`, `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password      | Dize  | Sorgu                         | Hesap tablosu dosyasını açmak için parola. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | --- | -------- |
| Spreadsheet    | Dosya | Hesap tablosu dosyasını yükleyin. |

### **Yanıt**

```json
{
  "ResponseFile": "ikili dosya akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | Tamam | Boş satırları kaldırılmış işlenmiş hesap tablosu dosyası döndürülür. |
| 400 | Geçersiz İstek | Geçersiz URL veya istek parametreleri. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgileri sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemiyor. |
| 413 | İçerik Çok Büyük | İstek içeriği izin verilen boyutu aşıyor. |
| 500 | İç Sunucu Hatası | Hesap tablosu veri alınırken bir anomaliyle karşılaştı. |

## SDK’lar ile Hesap Tablosu Boş Satırlarını Kaldırma Nasıl Kullanılır?

### Hesap Tablosu Boş Satırlarını Kaldırma Spesifikasyonu

[Hesap Tablosu Boş Satırlarını Kaldırma API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankRows), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek gönderileceğini göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}
{< tab tabNum="1" >}
```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/remove/blank-rows?outPath=outputFolder&outStorageName=MyStorage&region=tr-TR&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "ikili dosya akışı"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak projenizin görevlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose Cells Cloud web hizmetlerine nasıl istek gönderileceğini göstermektedir:
`[TBD]`