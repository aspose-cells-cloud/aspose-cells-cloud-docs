---
title: " Yinelenenleri Kaldır "
ArticleTitle: "Yinelenenleri Kaldır – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Yinelenenleri Kaldır"
type: docs
url: /tr/cells/remove/duplicates
aliases: []
keywords: "Aspose.Cells, Yinelenenleri Kaldır, API"
description: "Çalışma sayfasında, aralıkta veya tabloda yinelenen değerleri kaldırır."
weight: 1000
---

## Aspose.Cells Cloud Web Servislerinin Yinelenenleri Kaldırma Özelliği

Çalışma sayfasında, aralıkta veya tabloda yinelenen değerleri kaldırır. Bu yöntem, belirtilen sütunlarda aynı değerlere sahip satırları içeren hedef kapsama göz atar. Yinelenenlerin her seti için ilk oluşum hariç tüm yinelenenler kaldırılır. Karşılaştırma genellikle büyük/küçük harfe duyarlıdır ve doğrudan hücre değerini eşleştirir.

### Web API Uç Noktası

```http
PUT https://api.aspose.cloud/v4.0/cells/remove/duplicates
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama |
|----------------|--------|-----------------------------|-------------|
| Spreadsheet | Dosya | FormData | Yüklenecek hesap tablosu dosyası. |
| worksheet | Dize | Sorgu | Çalışma sayfası adı. (isteğe bağlı) |
| range | Dize | Sorgu | Yinelenenlerin kaldırılacağı aralık adı. (isteğe bağlı) |
| table | Dize | Sorgu | Yinelenenlerin kaldırılacağı tablo adı. (isteğe bağlı) |
| outPath | Dize | Sorgu | (İsteğe bağlı) Çalışma kitabının depolandığı klasör yolu. Varsayılan değer null’dır. |
| outStorageName | Dize | Sorgu | Çıkış dosyası depo adı. |
| region | Dize | Sorgu | Hesap tablosu bölgesi/dil ayarı (örneğin, `en-US`, `fr-FR`). SayıBiçimlendirme, tarih ayrıştırma ve yerel ayara özgü davranışları etkiler. |
| password | Dize | Sorgu | Hesap tablosu dosyasını açmak için parola. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama |
| -------------- | ---- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Yanıt**

```json
{
  "File": "sonuç olarak elde edilen hesap tablosunun ikili akışı (örneğin, .xlsx)"
}
```

**Yanıt Durum Kodları**

| Kod | Anlam | Açıklama |
|------|---------|-------------|
| 200 | Tamam | Yinelenenlerin kaldırıldığı sonuç hesap tablosu bir dosya akışı olarak döndürülür. |
| 400 | Hatalı İstek | Geçersiz istek parametreleri veya bozuk URL. |
| 401 | Yetkisiz | Kimlik doğrulama başarısız oldu veya kimlik bilgisi sağlanmadı. |
| 413 | Yük Çok Büyük | Yüklenecek dosya izin verilen boyut sınırını aşıyor. |
| 500 | İç Sunucu Hatası | Hesap tablosu veri alma veya diğer sunucu tarafı hata konusunda bir sorunla karşılaştı. |

## SDK’lar ile Yinelenenleri Kaldırma Nasıl Kullanılır?

### Yinelenenleri Kaldırma Belirtimi

[Yinelenenleri Kaldır API Belirtimi](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{RemoveDuplicates}), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek atılacağını göstermektedir.

{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}
{< tab tabNum="1" >}
```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v4.0/cells/remove/duplicates?worksheet=Sheet1&range=A1:C10&table=MyTable&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@example.xlsx'
```
{< /tab >}
{< tab tabNum="2" >}
```json
{
  "File": "sonuç olarak elde edilen hesap tablosunun ikili akışı (örneğin, .xlsx)"
}
```
{< /tab >}
{< /tabs >}

### Aspose Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en hızlı yoldur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose Cells Cloud web servislerinin nasıl çağrılacağını göstermektedir:

```csharp
// C# için SDK örnek kodu
var config = new Configuration
{
    AccessToken = "<jwt token>"
};
var apiInstance = new TransformApi(config);
var file = File.ReadAllBytes("example.xlsx");
var result = apiInstance.RemoveDuplicates(
    file,
    worksheet: "Sheet1",
    range: "A1:C10",
    table: "MyTable",
    outPath: "output/folder",
    outStorageName: "MyStorage",
    region: "en-US",
    password: "MyPassword"
);
File.WriteAllBytes("result.xlsx", result);
```

```java
// Java için SDK örnek kodu
ApiClient client = new ApiClient();
client.setAccessToken("<jwt token>");
TransformApi api = new TransformApi(client);
byte[] file = Files.readAllBytes(Paths.get("example.xlsx"));
byte[] result = api.removeDuplicates(
    file,
    "Sheet1",
    "A1:C10",
    "MyTable",
    "output/folder",
    "MyStorage",
    "en-US",
    "MyPassword"
);
Files.write(Paths.get("result.xlsx"), result);
```

```python
# Python için SDK örnek kodu
import asposecellscloud
from asposecellscloud.rest import ApiException

configuration = asposecellscloud.Configuration()
configuration.access_token = "<jwt token>"
api_instance = asposecellscloud.TransformApi(asposecellscloud.ApiClient(configuration))

with open('example.xlsx', 'rb') as f:
    file_bytes = f.read()

try:
    result = api_instance.remove_duplicates(
        file=file_bytes,
        worksheet='Sheet1',
        range='A1:C10',
        table='MyTable',
        out_path='output/folder',
        out_storage_name='MyStorage',
        region='en-US',
        password='MyPassword'
    )
    with open('result.xlsx', 'wb') as out_f:
        out_f.write(result)
except ApiException as e:
    print("Exception when calling TransformApi->remove_duplicates: %s\\n" % e)
```

`[TBD]`
---