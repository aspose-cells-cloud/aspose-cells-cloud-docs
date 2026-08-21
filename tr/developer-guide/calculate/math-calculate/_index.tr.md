---
title: "Aspose.Cells Cloud – Matematik Hesaplama API'si (Topla, Çıkar, Çarp, Böl, %)"
second_title: "Belge"
ArticleTitle: "Elektronik Tablolarda/Excel'de Toplama, Çıkarma, Çarpma, Bölme ve Yüzde İşlemleri"
linktitle: "Matematik Hesaplama"
type: docs
url: /tr/math-calculate/
keywords: "Matematik Hesaplama API'si, Aspose.Cells Cloud, Excel hesaplamaları, Topla, Çıkar, Çarp, Böl, Yüzde, Toplu Excel işleme, REST API"
description: "Aspose.Cells Cloud Matematik Hesaplama API'si ile Excel aralıklarında toplama, çıkarma, çarpma, bölme veya yüzde işlemlerini toplu olarak nasıl uygulayacağınızı öğrenin. İstek formatını, örnek kodu ve hata işleme içerir."
weight: 100
---

## **Giriş**: Elektronik Tablo Hızlı Hesaplama – Tek Çalışan API ile Toplama, Çarpma, Çıkarma, Bölme ve Yüzde Formülleri

_Bir formül yazmadan tüm sütunları, satırları veya tabloları kapsayacak şekilde toplu hesaplama yapın._

- **Temel matematik**: bir aralıktaki her hücreyi herhangi bir sayı ile toplayın, çıkarın, çarpın veya bölün
- **Yüzdelik değerler**: % cinsinden artırma/azaltma yapın veya bir sayının belirli bir yüzdesini hesaplayın (örneğin +15%, -8%, %20’si…)
- **Toplu**: binlerce hücreyi anında işlemek için—sürükle ve doldur, dizi formülü veya VBA’ye gerek yoktur

| **Hesaplama İşlemi** | Açıklama |
| :------------------- | :------- |
| **Topla**            | +        |
| **Çıkar**            | -        |
| **Çarp**             | \*       |
| **Böl**              | /        |
| **Yüzde**            | %        |

## **Matematik Hesaplama API'si**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri:**

| Parametre Adı | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Açıklama                                                                           |
| :------------ | :----- | :--------------------------- | :--------------------------------------------------------------------------------- |
| Spreadsheet   | Dosya  | FormData                     | İşlem yapılacak elektronik tablo dosyasını yükleyin.                               |
| operation     | Dize   | Sorgu                        | Gerçekleştirilecek matematiksel işlem (Topla, Çıkar, Çarp, Böl ve Yüzde).         |
| value         | Dize   | Sorgu                        | Uygulanabilirse hesaplama için kullanılacak değer.                                 |
| worksheet     | Dize   | Sorgu                        | İşlem yapılacak çalışma sayfasının adı.                                           |
| range         | Dize   | Sorgu                        | Hesaplamaya dahil edilecek hücre aralığı.                                         |
| region        | Dize   | Sorgu                        | Elektronik tablo bölgesi ayarı.                                                    |
| password      | Dize   | Sorgu                        | Korunuyorsa elektronik tablo dosyasını açmak için gerekli şifre.                   |

### **Yanıt**

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

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                          |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | Tamam (OK)            | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.    |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                |
| 413 | İçerik Çok Büyük      | Yüklenen dosya boyutu sınırları aşıyor.                           |
| 500 | İç Sunucu Hatası      | Beklenmeyen sunucu hatası.                                        |

## Matematik Hesaplama API'si Nerede Kullanılmalı?

- **Finans**: Tüm satın alma fiyatları sütununa %13 KDV ekleyin.
- **Envanter**: kg sütununu 2.2046 ile çarpıp toplu olarak pound’a dönüştürün.
- **Maaş bordrosu**: Tüm personelin prim sütununa 1.000 sabit prim ekleyin.
- **Döviz dönüşümü**: Satış sütununu güncel döviz kuru ile bölüp USD tutarlarını alın.
- **Notlandırma**: Her öğrenci puanından devamsızlık cezası olarak 5 puan çıkarın.
- **E-ticaret**: Ürün fiyatlarını tek tıkla %15 kampanya indirimiyle düşürün.

## Matematik Hesaplama API'si Neden Kullanılmalı?

- **Hızlı Excel hesaplamaları** – Ay sonu raporlarını saniyeler içinde tamamlayın.
- **Toplu yüzde artırma Excel** – Fiyatları, tahminleri, komisyonları tek tıkla güncelleyin.
- **Tüm sütuna aynı sayıyı ekle** – Envanter, para birimi dönüşümü, birim dönüşümü.
- **Formülsüz Excel** – Teknik olmayan kullanıcılar basitlikten memnun kalır.
- Mevcut SDK’lar aracılığıyla geliştirme hızlıca tamamlanabilir.

**Notlar**  
Desteklenen maksimum dosya boyutu 200 MB’tır. `range` parametresi geçerli bir Excel adresi olmalıdır (örneğin, A1:B10). Çok büyük çalışma sayfaları ek işlem süresi gerektirebilir.

## Matematik Hesaplama API'si Nasıl SDK’larla Kullanılır?

### Matematik Hesaplama API Spesifikasyonu

[Math Calculate Specification](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) ortak bir programlama arayüzü tanımlar ve geliştiricilerin web tarayıcısından doğrudan API ile etkileşime girmesini sağlar.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanımı, düşük seviyeli ayrıntıları soyutlayarak hücre bazlı matematik hesaplamalarını kısa kodla gerçekleştirmenize izin verdiğinden en hızlı geliştirme yöntemidir.  
Aspose.Cells Cloud SDK’larının tam listesi için lütfen [Aspose.Cells Cloud SDK’ları GitHub repositoriesine](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istekte bulunulacağını göstermektedir:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}