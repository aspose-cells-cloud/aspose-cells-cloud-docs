---
title: "Excel'den Karakterleri Kaldır – Aspose.Cells Cloud API (POST /cells/removecharacters)"
second_title: "Belge"
linktitle: "Karakterleri Kaldır"
type: docs
url: /tr/excel-remove-characters/
keywords: "karakterleri kaldır, Aspose.Cells, Excel API, metin işleme, bulut"
description: "Aspose.Cells Cloud API kullanarak Excel çalışma sayfalarından karakterleri, karakter kümelerini veya alt dizeleri nasıl kaldıracağınızı öğrenin. İstek şemasını, cURL örneğini, SDK kodunu ve hata işleme içerir."
weight: 100
ArticleTitle: "Excel'den Karakterleri Kaldır – Aspose.Cells Cloud API (POST /cells/removecharacters)"
---

## Excel Web API’sinden Karakterleri Kaldır

Seçili hücrelerdeki metin içeriğini temizlemek için kapsamlı bir araç seti. API, belirli karakterleri, önceden tanımlanmış karakter kümelerini veya alt dizeleri kaldırır ve çalışma sayfası metninin standart hale getirilmesini ve istenmeyen sembollerden arındırılmasını sağlar.

**Ön Gereksinimler**

- Aktif bir Aspose Cloud hesabı.  
- Doğrulama kılavuzunda açıklanan şekilde alınmış geçerli bir JWT erişim belirteci.  
- Bu uç noktayı çağırmadan önce Excel dosyasının depoya yüklenmiş olması gerekir.  
- Desteklenen dosya formatları şunları içerir: `.xlsx`, `.xls`, `.xlsm` ve diğer yaygın Excel türleri.

```http
POST https://api.aspose.cloud/v3.0/cells/removecharacters
```

### **Güvenlik ve Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı doğrulama</a> gerektirir.

### Fonksiyon Açıklaması

- **Özel karakterleri kaldır** – Silmek istediğiniz karakterleri belirtin. Her bir karakteri _Özel karakterleri kaldır_ alanına girin; API, seçilen hücrelerdeki bu karakterlerin tüm örneklerini siler.  
- **Karakter kümelerini kaldır** – Önceden tanımlanmış kümelerden birini seçin:  
  - **Yazdırılmayan karakterler** – Satır sonlarını ve ilk 32 yazdırılmayan ASCII karakterini (0‑31) ile ek kodları (127, 129, 141, 143, 144, 157) siler.  
  - **Metin karakterleri** – Tüm harfleri kaldırır.  
  - **Sayısal karakterler** – Tüm rakamları siler.  
  - **Semboller** – Matematiksel, geometrik, teknik, para birimi sembollerini ve “?”, “1”, “™” gibi harf benzeri sembolleri kaldırır.  
  - **Noktalama işaretleri** – Tüm noktalama işaretlerini kaldırır.  
- **Alt dizgiyi kaldır** – Seçilen hücrelerden belirtilen alt dizgiyi (örneğin bir kelimeyi) siler.

### İstek Parametreleri

| Parametre Adı           | Tür   | Konum  | Açıklama                                                                       |
| ------------------------| ----- | ------ | ------------------------------------------------------------------------------ |
| removeCharactersOptions | Sınıf | Gövde  | Hangi karakterlerin, karakter kümelerinin veya alt dizgilerin kaldırılacağını tanımlayan seçenekler. |

**`removeCharactersOptions` Şeması**

| Özellik          | Tür     | Zorunlu | Açıklama                                                                                                       |
| ---------------- | ------- | ------- | -------------------------------------------------------------------------------------------------------------- |
| Range            | string  | Evet    | İşlenecek hücreleri belirten A‑1 gösterimi veya adlandırılmış aralık (örneğin `"A1:C10"`).                      |
| CustomCharacters | string  | Hayır   | Silinecek her bir özel karakteri içeren dize (örneğin `"@#$"`).                                                |
| CharacterSet     | string  | Hayır   | Önceden tanımlanmış bir küme belirten numaralandırma değeri (`"NonPrinting"`, `"Text"`, `"Numeric"`, `"Symbols"`, `"Punctuation"`). |
| Substring        | string  | Hayır   | Kaldırılacak tam alt dizgi (örneğin `"USD"`).                                                                 |
| IgnoreCase       | boolean | Hayır   | `true` ise, karakter kaldırma işlemi büyük/küçük harf duyarlılığından bağımsız çalışır.                        |

**Örnek JSON istek gövdesi**

```json
{
  "Range": "A1:B20",
  "CustomCharacters": "@#$",
  "CharacterSet": "NonPrinting",
  "Substring": "USD",
  "IgnoreCase": true
}
```

**Örnek cURL isteği**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/removecharacters" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "Range": "A1:B20",
           "CustomCharacters": "@#$",
           "CharacterSet": "NonPrinting",
           "Substring": "USD",
           "IgnoreCase": true
         }'
```

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[birleştirilmiş dosya adı]",
    "Filesize" : [dosya boyutu],
    "FileContent" : "[Base64Dizesi]"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                        | Açıklama                                              |
|-----|------------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                   | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)   | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)      | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |
## SDK’larla PostRemoveCharacters API’sini Nasıl Kullanılır

### PostRemoveCharacters API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/TextProcessingController/PostRemoveCharacters" rel="noopener noreferrer">PostRemoveCharacters uç noktası için tam OpenAPI spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub Deposu</a>’na göz atın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:  
---