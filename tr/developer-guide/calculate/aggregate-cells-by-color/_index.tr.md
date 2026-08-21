---
title: "Aspose.Cells Cloud Web API – Excel'de Renge Göre Toplama ve Sayma"
second_title: "Doküman"
ArticleTitle: "Elektronik Tablo/Excel'de Renge Göre Topla, Say, Ortalama, En Yüksek ve En Düşük Değerleri Bul"
LinkTitle: "Renklerine Göre Hücreleri Toplu İşlem Yap"
type: docs
url: /tr/aggregate-cells-by-color/
keywords: "Aspose, Cells, Excel, API, aggregate, color, sum, count, average, min, max"
description: "Aspose.Cells Cloud API ile Excel hücrelerini dolgu veya yazı tipi rengine göre toplama, sayma, ortalama, en düşük ve en yüksek değerleri bulma gibi toplu işlemler yapın. Uç noktayı, parametreleri, kimlik doğrulamayı ve SDK örneklerini öğrenin."
weight: 100
---

## Genel Bakış

API, hücre **renklerine** göre veri hesaplamaları gerçekleştirebilir. Excel elektronik tablosunda hücrelerin dolgu veya yazı tipi rengine göre toplama, sayma, ortalama ve aynı zamanda en yüksek ile en düşük değerleri bulabilir.

| Hesaplama İşlemi | Açıklama                                                     |
| :---------------- | :----------------------------------------------------------- |
| Say (Count)       | Aynı renkteki hücre sayısını belirle.                        |
| Topla (Sum)       | Aynı renkteki hücrelerin toplam değerini hesapla.           |
| En Yüksek Değer (Max) | Aynı renkteki hücreler arasında en yüksek değeri bul.     |
| En Düşük Değer (Min) | Aynı renkteki hücreler arasında en düşük değeri bul.      |
| Ortalama (Average) | Aynı renkteki hücrelerin ortalama değerini hesapla.        |

## Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür     | Konum      | Açıklama                                                         |
| :------------ | :------ | :--------- | :--------------------------------------------------------------- |
| Spreadsheet   | Dosya   | FormData   | İşlenecek Excel çalışma kitabını belirtir.                       |
| Worksheet     | String  | Sorgu      | Aralığın bulunduğu çalışma sayfasının adı.                        |
| Range         | String  | Sorgu      | A‑1 stili aralık (örneğin `A1:B10`).                            |
| Operation     | String  | Sorgu      | Hesaplama yöntemi – `Sum`, `Count`, `Average`, `Min`, veya `Max`. |
| ColorPosition | String  | Sorgu      | Değerlendirilecek rengi belirler – `Background`, `Font`.        |
| Region        | String  | Sorgu      | Elektronik tablo bölgesi ayarı (örneğin `us-east-1`).            |
| Password      | String  | Sorgu      | Korumalı bir çalışma kitabını açmak için şifre (isteğe bağlı).    |

#### Enumerasyonlar

- **ColorPosition**

  | Değer      | Anlam                         |
  | :--------- | :---------------------------- |
  | Background | Hücrenin dolgu rengini kullan. |
  | Font       | Hücrenin yazı tipi rengini kullan. |

**Örnek multipart/form‑data isteği**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/calculate/aggregate/color?Worksheet=Sheet1&Range=A1:B10&Operation=Sum&ColorPosition=Background" \
  -H "Authorization: Bearer <access_token>" \
  -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### Yanıt

Aşağıdaki şema, yanıt nesnesini tanımlar. Somut bir örnek şemanın hemen ardından verilmiştir.

```json
{
  "Name": "AggregateResultByColorResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "AggregateResults",
      "DataType": {
        "Identifier": "Array",
        "Reference": "AggregateResultByColor",
        "ElementDataType": {
          "Reference": "AggregateResultByColor"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": { "Identifier": "Integer" }
    },
    {
      "Name": "Status",
      "DataType": { "Identifier": "String" }
    }
  ]
}
```

**Örnek yanıt (gerçek dünya değerleri)**

```json
{
  "Code": 200,
  "Status": "OK",
  "AggregateResults": [
    {
      "Color": "#FF0000",
      "Count": 12,
      "Sum": 345.67,
      "Average": 28.8,
      "Min": 5.0,
      "Max": 80.0
    },
    {
      "Color": "#00FF00",
      "Count": 7,
      "Sum": 210.0,
      "Average": 30.0,
      "Min": 10.0,
      "Max": 50.0
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                 | Açıklama                                                         |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK (Tamam)            | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.     |
| 400  | Bad Request (Hatalı İstek) | Eksik veya geçersiz parametreler (örneğin desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz) | Geçersiz veya eksik JWT belirteci.                               |
| 413  | Payload Too Large (İstek Gövdesi Çok Büyük) | Yüklenecek dosya boyut sınırını aşıyor.                     |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                                     |

## Renge Göre Toplu İşlem API'si Nerede Kullanılmalı?

Bir elektronik tabloda, farklı kategorilerden gelen veriler genellikle renk kodlanmıştır. Bu API sayesinde her renk grubu için toplama, sayma, ortalama veya en düşük ve en yüksek değerleri bulabilir, renk tabanlı veri analizini basitleştirebilirsiniz.

## Renge Göre Toplu İşlem API'si Neden Kullanılmalı?

API, özel ayrıştırma mantığı yazmadan renk tabanlı hesaplamaları hızlı ve güvenilir bir şekilde gerçekleştirmenizi sağlar. Aspose.Cells Cloud SDK’larıyla sorunsuz entegre olur ve geliştiricilerin renk tabanlı toplama işlemlerini birkaç satır kodla yapmasını sağlar.

## Renge Göre Toplu İşlem API'si Nasıl SDK’lar ile Kullanılır?

### Renge Göre Toplu İşlem API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/AggregateCellsByColor" rel="noopener noreferrer">Renge Göre Toplu İşlem API Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenizi sağlar.

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, düşük seviye detayları soyutlayarak yalnızca birkaç satır kodla hücre rengine göre toplama işlemlerini yapmanızı sağlayan en hızlı geliştirme yoludur.  
Tüm Aspose.Cells Cloud SDK listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{</tab>}}
{{< /tabs >}}

**Notlar:**

- Korumalı çalışma kitaplarıyla çalışırken, isteğin başarısız olup 401 hatası vermemesi için isteğe bağlı `Password` sorgu parametresini ekleyin.
- `Spreadsheet` dosyası için maksimum istek boyutu 100 MB’tır. Daha büyük dosyaları işlemek gerekiyorsa, önce çalışma kitabını Aspose Cloud deposuna yükleyip `Path` parametresiyle referans almayı düşünün (burada gösterilmemiştir).