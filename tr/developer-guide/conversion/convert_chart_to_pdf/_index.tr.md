---
title: "Grafiği PDF'ye Dönüştür"
ArticleTitle: "Grafiği PDF'ye Dönüştür – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "ConvertChartToPdf"
type: docs
url: /cells/convert/chart/pdf
aliases: []
keywords: "GrafiğiPDF'yeDönüştür, Aspose.Cells, PDF, grafik dönüştürme"
description: "Yerel bir sürücüdeki bir elektronik tablo grafiğini PDF'ye dönüştürür."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin Grafiği PDF'ye Dönüştürme Özelliği

Bu yöntem, yerel dosya yüklemesi yoluyla sağlanan bir elektronik tablo dosyasından bir grafik okur, onu PDF formatına dönüştürür ve dönüştürülmüş sonucu döndürür. Tamamen bulut sunucusunda çalışır, bu nedenle ara depolama gerekmez. Kaynak dosya yolu ve hedef format doğru olmalı ve kaynak dosyayı okumak için uygun izinlere sahip olunmalıdır. Eksik dosyalar, erişim sorunları veya dönüştürme hataları gibi hatalar uygun HTTP hata yanıtlarına neden olur.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|------------------|---------|-------------------------------|----------|
| Spreadsheet      | Dosya   | FormData                      | Elektronik tablo dosyasını yükleyin. |
| worksheet        | String  | Sorgu                         | Elektronik tablonun çalışma sayfası adı. |
| chartIndex       | Integer | Sorgu                         | Çalışma sayfasının grafik indeksi. |
| outPath          | String  | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır. |
| outStorageName   | String  | Sorgu                         | Çıktı dosyası için depo adı. |
| fontsLocation    | String  | Sorgu                         | Özel yazı tiplerini kullanın. |
| region           | String  | Sorgu                         | Elektronik tablonun bölge/dil ayarı (örn., `en-US`, `fr-FR`). Sayı biçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password         | String  | Sorgu                         | Elektronik tablo dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür  | Açıklama                  |
|---------------|------|---------------------------|
| Spreadsheet   | Dosya | Elektronik tablo dosyasını yükleyin. |

### **Yanıt**

```json
{
  "ResponseFile": "ikili PDF dosyası akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | Tamam | Grafik başarıyla PDF'ye dönüştürüldü; ikili PDF dosyası döndürüldü. |
| 400 | Geçersiz İstek | Geçersiz istek parametreleri veya hatalı URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 404 | Bulunamadı | Kaynak dosyaya erişilemedi. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Sunucu İç Hatası | Dönüştürme işlemi sırasında bir hata oluştu. |

## SDK’larla Grafiği PDF'ye Dönüştürme Nasıl Kullanılır

### Grafiği PDF'ye Dönüştürme Spesifikasyonu

[Grafiği PDF'ye Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPdf), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}
{< tab tabNum="1" >}
```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/convert/chart/pdf?worksheet={worksheet}&chartIndex={chartIndex}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/pdf" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "ResponseFile": "ikili PDF dosyası akışı"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanıza olanak sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose Cells Cloud web servislerinin nasıl çağrılacağını göstermektedir:
`[TBD]`
---