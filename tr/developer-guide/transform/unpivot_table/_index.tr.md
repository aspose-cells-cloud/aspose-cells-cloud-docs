---
title: "Tabloyu Unpivot Et"
ArticleTitle: "Tabloyu Unpivot Et – Aspose.Cells Cloud API"
second_title: "Belge"
linktype: "Unpivot Table"
type: docs
url: /tr/cells/unpivot/table
aliases: []
keywords: "Aspose.Cells, Unpivot, Dönüştürme"
description: "Elektronik tabloda satır ve sütunları değiştirin."
weight: 1
---

## Aspose.Cells Cloud Web Hizmetlerinin Unpivot Tablosu

Elektronik tabloda satır ve sütunları değiştirin.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/unpivot/table
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür      | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                                                         |
|------------------|----------|-------------------------------|------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Dosya    | FormData                      | Elektronik tablo dosyasını yükleyin.                                                                             |
| worksheet        | Metin    | Sorgu                         | Çalışma sayfası adı.                                                                                             |
| index            | Tamsayı  | Sorgu                         | Belirli bir veri aralığı.                                                                                        |
| skipEmptyValue   | Boole    | Sorgu                         | Boş değerleri atla (varsayılan: true).                                                                           |
| outPath          | Metin    | Sorgu                         | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null'dır.                            |
| outStorageName   | Metin    | Sorgu                         | Çıktı dosyası için Depo Adı.                                                                                      |
| region           | Metin    | Sorgu                         | Elektronik tablo bölgesi/dil ayarı (örneğin, `tr-TR`, `en-US`, `fr-FR`). SayıBiçimlendirme, tarih çözümlemesi ve yerel ayara özgü davranışları etkiler. |
| password         | Metin    | Sorgu                         | Elektronik tablo dosyasını açmak için parola.                                                                     |

### Gövde İstek Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | --- | -------- |
| Yok            | Yok | Gövde istek parametresi yoktur. |

### **Yanıt**

```json
{
  "File": "unpivot edilmiş elektronik tablonun ikili akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | Başarılı | Unpivot edilmiş elektronik tablo dosyası döndürülür. |
| 400 | Geçersiz İstek | Geçersiz istek parametreleri. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Yük Çok Büyük | Yüklenen dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Beklenmeyen sunucu hatası. |

## Unpivot Tablosunu SDK’larla Nasıl Kullanılır

### Unpivot Tablosu Spesifikasyonu

[Unpivot Table API Specification](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4# /Transform/UnpivotTable), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/unpivot/table?worksheet={worksheet}&index={index}&skipEmptyValue={skipEmptyValue}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "unpivot edilmiş elektronik tablonun ikili akışı"
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviyeli detayları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek yapıldığını göstermektedir:
 `[TBD]`
---