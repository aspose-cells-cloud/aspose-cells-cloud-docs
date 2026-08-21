---
title: "Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır"
ArticleTitle: "Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır"
type: docs
url: /tr/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
aliases: []
keywords: "Aspose.Cells, Yineleyen Alt Dizgileri Kaldır, API"
description: "Çalışma kitabında belirtilen bir aralık içindeki hücrelerde tekrarlayan alt dizgileri bulup kaldırmak için API."
weight: 1
---

## Aspose.Cells Cloud Web Hizmetlerinin Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır Özelliği

Seçilen aralıktaki her bir hücre içinde yineleyen alt dizgileri bulur ve kaldırır. Kullanıcı tanımlı veya önceden tanımlı ayraç karakterleri kullanılır; formüller, biçimlendirme ve veri doğrulama ise korunur.

**Yinelemelerin nasıl algılandığı**  
1. Her hücre değeri, seçilen ayraç(lar) kullanılarak alt dizgilerine ayrılır.  
2. Araç, **aynı hücre içindeki** alt dizgileri karşılaştırır ve her yinelemeden yalnızca **ilk oluşumunu** tutar.  
3. Temizlenmiş alt dizgiler, aynı ayraç(lar)la yeniden birleştirilir ve hücreye geri yazılır.  

**Ayraç seçenekleri**  
- Önceden tanımlı liste: virgül, noktalı virgül, boşluk, sekme, satır sonu  
- `Özel` – herhangi bir karakter(ler) girilebilir; birden fazla karakter tek bir bileşik ayraç olarak kabul edilir  
- `YanYanaAyraçlarıBirTutar` – bitişik ayraçları tek bir ayırıcıya dönüştürür  

Sadece dize türü hücreler işlenir; sayılar, boolean değerler ve formüller önce dizeye dönüştürülür (formüller atılır). Temizlenen hücre sayısı ve güncellenmiş çalışma kitaplığı akışı döndürülür.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/duplicate-substrings
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamaya</a> gerek duyar.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama |
|---------------|-----|------------------------------|----------|
| name | string | Yol | (Gerekli) Alınacak çalışma kitaplığı dosyasının adı. |
| worksheet | string | Yol | Elektronik tablonun çalışma sayfasını belirtin. |
| range | string | Yol | Elektronik tablonun çalışma sayfası aralığını belirtin. |
| delimiters | string | Sorgu | Hücre değerlerini ayırmak için kullanılacak ayraç(lar) (örn., virgül, noktalı virgül, boşluk, sekme, satır sonu). Gerekli. |
| treatConsecutiveDelimitersAsOne | boolean | Sorgu | Bitişik ayraçları tek bir ayırıcıya dönüştürür. Varsayılan: true. İsteğe bağlı. |
| caseSensitive | boolean | Sorgu | Yinelemeleri algıarken büyük/küçük harf duyarlı karşılaştırma yapar. İsteğe bağlı. |
| folder | string | Sorgu | (İsteğe bağlı) Çalışma kitabının bulunduğu klasör yolu. Varsayılan: null. |
| storageName | string | Sorgu | (İsteğe bağlı) Özel bulut depolama kullanılıyorsa depolama adı. |
| region | string | Sorgu | Elektronik tablo bölgesi/dil ayarı (örn., `en-US`, `fr-FR`). İsteğe bağlı. |
| password | string | Sorgu | Elektronik tablo dosyasını açmak için parola. İsteğe bağlı. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| - | - | Bu işlem için istek gövdesi gerekli değildir. |

### **Yanıt**

```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-kodlanmış çalışma kitaplığı akışı"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|-----|-------|----------|
| 200 | OK | İşlem başarılı; temizlenen hücre sayısı ve güncellenmiş çalışma kitaplığı akışı döndürülür. |
| 400 | Bad Request | Bir veya daha fazla istek parametresi eksik veya geçersiz. |
| 401 | Unauthorized | Kimlik doğrulama başarısız oldu veya JWT belirteci eksik/geçersiz. |
| 413 | Payload Too Large | İstek izin verilen boyut sınırlarını aşıyor. |
| 500 | Internal Server Error | Sunucuda beklenmeyen bir hata oluştu. |

## SDK’larla Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır Nasıl Kullanılır

### Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır Spesifikasyonu

[Uzak Elektronik Tabloda Yineleyen Alt Dizgileri Kaldır API Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveDuplicateSubstringsInRemoteSpreadsheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye istek nasıl yapıldığını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}
{< tab tabNum="1" >}
```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/range/A1:C10/content/remove/duplicate-substrings?delimiters=comma%2Csemicolon&treatConsecutiveDelimitersAsOne=true&caseSensitive=false" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "code": 200,
  "status": "OK",
  "cellsCount": 123,
  "file": "base64-kodlanmış çalışma kitaplığı akışı"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini en hızlı şekilde hızlandıran yoldur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose Cells Cloud web hizmetlerine nasıl istek yapıldığını göstermektedir:
`[TBD]`
---