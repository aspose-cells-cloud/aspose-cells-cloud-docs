---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Belge"
linktype: "docs"
url: /cells/flip
aliases: []
keywords: "FlipData, Dönüştürme, Aspose.Cells"
description: "Bir hesaplama tablosu dosyasında belirtilen veri aralığını transpoze eder."
weight: 100
---

## Aspose.Cells Cloud Web Servislerinin FlipData Özelliği

Bu API, verilen bir veri matrisinin yönünü çevirir. Örneğin, 3x2 bir aralık (3 satır, 2 sütun), çıktıda 2x3 bir aralığa (2 satır, 3 sütun) dönüşür. Genellikle farklı grafikler, raporlar veya veri modellerinin giriş gereksinimlerini karşılamak amacıyla verileri yeniden yapılandırmak için kullanılır.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür     | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|---------------|---------|-------------------------------|----------|
| Spreadsheet   | Dosya   | FormData                      | Hesaplama tablosu dosyasını yükleyin. |
| worksheet     | String  | Sorgu                         | Çalışma sayfası adı. |
| cellArea      | String  | Sorgu                         | Belirtilen veri aralığı. |
| Horizontal    | Boolean | Sorgu                         | Yatay/Dikey Çevirme. Varsayılan: true |
| outPath       | String  | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan: null |
| outStorageName| String  | Sorgu                         | Çıkış dosyası için depo adı. |
| region        | String  | Sorgu                         | Hesaplama tablosu bölgesi/dil ayarı (örn. `tr-TR`, `fr-FR`). Sayı biçimlendirme, tarih çözümlemesi ve yerel ayara özgü davranışları etkiler. |
| password      | String  | Sorgu                         | Hesaplama tablosu dosyasını açmak için şifre. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | --- | -------- |
| *Yok*          | *N/A* | *Ek bir JSON gövdesi gerekmez; dosya multipart/form-data olarak gönderilir.* |

### **Yanıt**

```json
{
  "File": "<dönüştürülmüş çalışma kitabının ikili akışı>"
}
```

**Yanıt Durum Kodları**

| Kod | Anlamı | Açıklama |
|-----|--------|----------|
| 200 | OK (Tamam) | İşlem başarıyla tamamlandı ve dönüştürülmüş hesaplama tablosu dosyası döndürüldü. |
| 400 | Bad Request (Hatalı İstek) | Gerekli parametrelerden bir veya daha fazlası eksik veya geçersiz. |
| 401 | Unauthorized (Yetkisiz) | Kimlik doğrulama başarısız – eksik veya geçersiz JWT belirteci. |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Sunucuda beklenmeyen bir hata oluştu. |

## SDK’larla FlipData Nasıl Kullanılır

### FlipData Belirtimi

[FlipData API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells Cloud web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt belirteci>" \
  -F "Spreadsheet=@örnek.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<dönüştürülmüş çalışma kitabının ikili akışı>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose Cells Cloud web servislerinin nasıl çağrılacağını göstermektedir:
 `[TBD]`
---