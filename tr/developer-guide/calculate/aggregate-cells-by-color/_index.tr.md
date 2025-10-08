---
title: Aspose.Cells Cloud Web API - E-Tablo/Exce'de renge göre Toplam, Sayım, Ortalama Değer vb.
second_title: Documen
ArticleTitle: Sum, Count, Average Value, etc by color in Spreadsheet/Exce
LinkTitle: Aggregate Cells by Colo
type: docs
url: /tr/aggregate-cells-by-color/
keywords: Sum, Count, Average Value, Max Value, Min Value, Excel REST API, Spreadsheet Operations, Aspose.Cells, Excel Cloud AP
description: Aspose.Cells Cloud Web API(Excel Cloud API) veri hesaplamaları, toplama ve ortalama işlemlerini gerçekleştirebilir ve ayrıca hücrelerin dolgu veya yazı tipi rengine göre Excel elektronik tablosundaki maksimum ve minimum değerleri bulabilir
weight: 100
kwords: Toplam, Sayım, Ortalama Değer, Maksimum Değer, Minimum Değer, Excel REST API, Elektronik Tablo İşlemleri, Aspose.Cells, Excel Bulut API
---
API, veri hesaplamaları, toplama ve ortalama işlemlerini gerçekleştirebilir ve ayrıca hücrelerin dolgu veya yazı tipi rengine göre Excel elektronik tablosundaki maksimum ve minimum değerleri bulabilir.

| Hesaplama İşlemi| Tanım|
|:- |:- |
| Saymak| Aynı renkteki hücre sayısını belirleyin.|
| Toplam| Aynı renkteki hücrelerin toplam değerini hesaplayın.|
| Maksimum Değer| Aynı renkteki hücreler arasında en yüksek değeri belirleyin.|
| Minimum Değer| Aynı renkteki hücreler arasında en düşük değeri bulun.|
|Ortalama Değer| Aynı renkteki hücrelerin ortalama değerini hesaplayın.|

## **Cells'i Renk API'e Göre Toplama**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/aggregate/color
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| E-tablo dosyasını yükleyin.|
| Çalışma sayfası| Sicim| Sorgu| Çalışma sayfasını belirtir.|
| Menzil| Sicim| Sorgu| Aralığı belirtir.|
| Operasyon| Sicim| Sorgu| Toplam, Sayım, Ortalama, Min ve Maks dahil olmak üzere hesaplama işlem yöntemlerini belirtin.|
| RenkPozisyonu| Sicim| Sorgu| Arka plan rengine ve/veya yazı tipi rengine göre toplanacak ve sayılacak içeriği belirtir.|
| Bölge| Sicim| Sorgu| E-tablo bölge ayarı.|
| Şifre| Sicim| Sorgu| E-tablo dosyasını açmak için şifre.|

### **Cevap**

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
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Aggregate by Color API'i nerede kullanmalıyız?

Bir elektronik tabloda, farklı kategorilere ait veriler farklı renklerde gösterilir ve toplama, sayma, ortalamaları hesaplama, renge göre maksimum ve minimum değerleri bulma gibi işlemlere olanak sağlar.

## Neden Aggregate by Color API'i kullanmalısınız?

- Renk verilerinin analizine yönelik yöntemler sağlayın.
- Veri analizi için temel verileri sağlamak amacıyla verileri renge göre sınıflandırın ve hesaplayın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla Aggregate by Color API Nasıl Kullanılır

### Renk API Spesifikasyonuna Göre Toplam

 The[Renk API Spesifikasyonuna Göre Toplam](https://reference.aspose.cloud/cells/#/CalculateController/AggregateCellsByColor) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, yalnızca kısa bir kod parçasıyla hücre rengine göre hesaplamaları toplamanıza olanak tanıdığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AggregateCellsByColor.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AggregateCellsByColor.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AggregateCellsByColor.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AggregateCellsByColor.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AggregateCellsByColor.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AggregateCellsByColor.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AggregateCellsByColor.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AggregateCellsByColor.go" >}}
{{< /tab >}}
{{< /tabs >}}
