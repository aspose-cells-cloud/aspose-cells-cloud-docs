---
title: Aspose.Cells Cloud Web API - Elektronik Tablo/Excel aralığında toplama, çıkarma, çarpma, bölme ve yüzde hesaplama
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Matematik Hesaplama
type: docs
url: /tr/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: API elektronik tablolarında hesaplamalar yapmak için Math Calculate API'i kullanmaya yönelik kapsamlı kılavuz
weight: 100
kwords: Matematik hesaplaması, Cloud REST API, Toplama, Çıkarma, Çarpma, Bölme, Yüzde, Office Cloud, Aspose.Cells
---
Geliştiriciler, belirtilen aralıktaki elektronik tablolarda toplama, çıkarma, çarpma, bölme ve yüzde hesaplamaları yapmak için bu API'i kullanabilirler.

|**Hesaplama İşlemi** | Tanım|
|:- |:- |
|**Eklemek** |+ |
|**Eksi** |-  |
|**Çarpmak** |*  |
|**Bölmek** |/ |
|**Yüzde** |% |

## **Matematik Hesaplama API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **İstek Parametreleri:**

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTP Gövdesi| Tanım|
|:- |:- |:- |:- |
| Elektronik tablo| Dosya| FormVerileri| İşlem için elektronik tablo dosyasını yükleyin.|
| operasyon| Sicim| Sorgu| Yapılacak matematiksel işlem (Toplama, Çıkarma, Çarpma, Bölme ve Yüzde).|
| değer| Sicim| Sorgu| Hesaplamada kullanılacak bir değer (uygulanabilirse).|
| çalışma sayfası| Sicim| Sorgu| Üzerinde işlem yapılacak çalışma sayfasının adı.|
| menzil| Sicim| Sorgu| Hesaplamaya dahil edilecek hücre aralığı.|
| bölge| Sicim| Sorgu|E-tablonun belirli bölgesini tanımlar.|
| şifre| Sicim| Sorgu| Eğer korumalı ise, elektronik tablo dosyasını açmak için şifre.|

### **Cevap**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Hata Kodları

- **400 Kötü İstek**: Geçersiz Apose.Cells Bulut API URI.
- **401 Yetkisiz**: Geçersiz erişim belirteci. Veya geçersiz istemci kimliği ve sırrı.
- **404 Bulunamadı**: E-tablo dosyasına erişilemiyor.
- **500 Sunucu Hatası**: Hesaplama verilerinin alınmasında elektronik tabloda bir anormallik tespit edildi.

## Matematik Hesaplama API'i nerede kullanmalıyız?

API numaralı matematik hesaplaması elektronik tablolarda toplu hesaplamalar için uygundur.

## Neden Matematik Hesaplama API'i kullanmalısınız?

- Toplu matematik hesaplamaları yapın.
- Mevcut SDK üzerinden geliştirme hızlı bir şekilde tamamlanabilir.

## SDK'larla API Matematiksel Hesaplama Nasıl Kullanılır

### Matematik Hesaplama API Spesifikasyonu

 The[Matematik Hesaplama Spesifikasyonu](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) Geliştiricilerin API ile doğrudan bir web tarayıcısı üzerinden etkileşime girmesine olanak tanıyan, herkese açık bir programlama arayüzü tanımlar.

### Aspose.Cells Bulut SDK'larını kullanın

SDK'yı kullanmak, düşük seviyeli ayrıntıları soyutlayarak, sadece kısa bir kodla hücre bazında matematiksel hesaplamalar yapmanıza olanak sağladığı için geliştirmenin en hızlı yoludur.
 Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
