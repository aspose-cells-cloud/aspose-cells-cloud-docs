---
title: "Hücre Değeri Belirleme – Aspose.Cells Cloud API Referansı (v3.0)"  
type: docs  
url: /tr/set-value-of-a-cell-in-a-worksheet/  
weight: 70  
keywords: "Aspose Cells API hücre değeri ayarlama, Excel hücre güncelleme REST, Aspose.Cells Cloud cURL örneği"  
description: "Aspose.Cells Cloud REST API ile bir Excel çalışma sayfasındaki belirli bir hücrenin değerini nasıl ayarlayacağınızı öğrenin. İsteğin sözdizimi, parametreleri, HTTPS cURL örneği ve SDK kod örnekleri içerir."  
---  

Bu REST API, bir Excel dosyasındaki **hücre değerini** ayarlar.

## REST API  

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}
```  

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) ihtiyaç duyar.

**İstek Parametreleri**

| Ad            | Tür    | Konum | Açıklama                                           |
|---------------|--------|-------|----------------------------------------------------|
| name          | string | path  | Excel belgesinin adı (uzantı dahil).               |
| sheetName     | string | path  | Çalışma sayfasının adı (büyük/küçük harfe duyarlı). |
| cellName      | string | path  | Hedef hücrenin A1 tarzı adresi (örn. `A1`).        |
| value         | string | query | Hücreye atanacak değer.                            |
| type          | string | query | Değerin veri türü (`int`, `string`, `float`, vb.). |
| formula       | string | query | Hücreye uygulanacak formül (isteğe bağlı).         |
| folder        | string | query | Belgenin bulunduğu klasör (isteğe bağlı).          |
| storageName   | string | query | Dosyanın bulunduğu depo adı (isteğe bağlı).        |

## **Yanıt**

CellResponse döner.

- **Yanıt Alanları Genel Bakış**

| Alan            | Tür     | Açıklama                                               |
| --------------- | ------- | ------------------------------------------------------ |
| `Name`          | string  | Hücrenin adresi (örn. `F341`).                         |
| `Row`           | integer | Sıfır tabanlı satır indeksi.                           |
| `Column`        | integer | Sıfır tabanlı sütun indeksi.                           |
| `Value`         | string  | Hücrenin gösterilen değeri.                            |
| `Type`          | string  | Hücrenin veri türü (örn. `IsString`).                 |
| `Formula`       | string  | Hücre bir formül içeriyorsa formül metni.             |
| `IsFormula`     | bool    | Hücrenin bir formül içerip içermediğini gösterir.      |
| `IsMerged`      | bool    | Hücrenin birleştirilmiş bir aralıkta olup olmadığını gösterir. |
| `IsArrayHeader` | bool    | Hücrenin bir dizi başlığı olup olmadığını gösterir.    |
| `IsInArray`     | bool    | Hücrenin bir dizide olup olmadığını gösterir.         |
| `IsErrorValue`  | bool    | Hücrenin bir hata değeri içerip içermediğini gösterir. |
| `IsInTable`     | bool    | Hücrenin bir tablonun içinde olup olmadığını gösterir. |
| `IsStyleSet`    | bool    | Hücreye bir stil uygulanıp uygulanmadığını gösterir.   |
| `HtmlString`    | string  | Hücre değerinin HTML ile kodlanmış gösterimi.          |
| `Style.link`    | object  | Stil kaynağına olan bağlantı.                         |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                              |
|------|-----------------------------|-------------------------------------------------------|
| 200  | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                   |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırını aşıyor.              |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                         |

## SDK’larla PostWorksheetCellSetValue API Nasıl Kullanılır

### PostWorksheetCellSetValue API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetCellSetValue), geliştiricilerin REST uç noktalarına doğrudan tarayıcıdan veya herhangi bir HTTP istemcisinden erişmesine olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

Aspose.Cells web hizmetlerini çağırmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bir hücre değerinin nasıl ayarlanacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?value=1234&type=int" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Cell":{
    "Name":"A3",
    "Row": 2,
    "Column":0,
    "Value": "",
    "Type":"String",
    "Formula" : "=Sum(A2:A15)",
    ...
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, düşük seviye ayrıntıları ele alarak projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’larla Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellSetValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellSetValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellSetValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellSetValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellSetValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellSetValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellSetValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellSetValue.go" >}}

{{< /tab >}}

{{< /tabs >}}