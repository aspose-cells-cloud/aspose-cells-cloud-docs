---
title: "Uzak Elektronik Tabloda Metni Dönüştür"
ArticleTitle: "Uzak Elektronik Tabloda Metni Dönüştür – Aspose.Cells Cloud"
second_title: "Belge"
linktitle: "Uzak Elektronik Tabloda Metni Dönüştür"
type: docs
url: /tr/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
aliases: []
keywords: "Aspose.Cells, Metin Dönüştürme, API"
description: "Bir çalışma sayfasının belirli bir aralığında bulunan metni dönüştürür; sayma dönüşümü, karakter değiştirme, satır sonu işleme ve aksanlı karakterlerin normalleştirilmesini içerir."
weight: 1000
---

## Aspose.Cells Cloud Web Hizmetlerinin Uzak Elektronik Tabloda Metni Dönüştürme Özelliği

Metin olarak saklanan sayıların doğru sayı formatına dönüştürülmesini, istenmeyen karakterleri ve satır sonlarını istenen karakterlerle değiştirmeyi ve aksanlı karakterleri aksansız eşdeğer karakterlerine dönüştürmeyi belirtir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|------------------|--------|-------------------------------|----------|
| name             | string | Yol | (Gerekli) Alınacak çalışma kitabının dosya adı. |
| worksheet        | string | Yol | Elektronik tablonun çalışma sayfasını belirtin. |
| range            | string | Yol | Elektronik tablonun çalışma sayfası aralığını belirtin. |
| convertTextType  | string | Sorgu | Metin türü dönüştürmesini belirtir. (Gerekli) |
| sourceCharacters | string | Sorgu | Kaynak karakterleri belirtir. (İsteğe bağlı) |
| targetCharacters | string | Sorgu | Hedef karakterleri belirtir. (İsteğe bağlı) |
| folder           | string | Sorgu | (İsteğe bağlı) Çalışma kitabının bulunduğu klasör yolu. Varsayılan değer null'dır. |
| storageName      | string | Sorgu | (İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama adı. Atlanırsa varsayılan depolama kullanılır. |
| region           | string | Sorgu | Elektronik tablonun bölge/dil ayarı (örn. `tr-TR`, `fr-FR`). Sayı formatlamayı, tarih ayrıştırmayı ve yerel ayara özgü davranışları etkiler. (İsteğe bağlı) |
| password         | string | Sorgu | Elektronik tablo dosyasını açmak için şifre. (İsteğe bağlı) |

### Gövde Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| - | - | - |

### **Yanıt**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Metin dönüştürme başarıyla tamamlandı.",
  "Data": {
    // Buraya güncellenen hücre sayısı gibi dönüştürme sonucu detayları eklenebilir.
  }
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK | Metin dönüştürme işlemi başarıyla tamamlandı. |
| 400 | Bad Request | İstek hatalı biçimlendirilmiş veya gerekli parametreler eksik. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Payload Too Large | İstek gövdesi izin verilen boyut sınırını aşıyor. |
| 500 | Internal Server Error | Sunucuda beklenmedik bir hata oluştu. |

## Uzak Elektronik Tabloda Metni Dönüştür'ü SDK'lar ile Nasıl Kullanılır

### Uzak Elektronik Tabloda Metni Dönüştür Spesifikasyonu

[Uzak Elektronik Tabloda Metni Dönüştür API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/{ConvertTextInRemoteSpreadsheet}), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose Cells Cloud web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}

{< tab tabNum="1" >}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/convert/text?convertTextType={convertTextType}&sourceCharacters={sourceCharacters}&targetCharacters={targetCharacters}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Metin dönüştürme başarıyla tamamlandı.",
  "Data": {
    "UpdatedCellsCount": 124,
    "Details": "Sayılar dönüştürüldü, karakterler değiştirildi, satır sonları normalleştirildi."
  }
}
```

{< /tab >}

{< /tabs >}

### Aspose Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek atıldığını göstermektedir:
 `[TBD]`
---